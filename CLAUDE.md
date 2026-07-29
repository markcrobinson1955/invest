# invest — Portfolio Alignment Analyzer

Read this before editing anything. Two of the four files in this repo are load-bearing data
that other tools parse at runtime, and they do not look like it.

## What this project is

A portfolio analysis tool that runs **inside a general-purpose AI assistant** rather than as
an application. There is no backend, no build step, and no framework. The "program" is a pair
of large markdown prompts; the only executable code is a single static landing page.

A user visits the landing page, copies a bundle of prompt + data to their clipboard, pastes it
into Claude / ChatGPT / Gemini, and uploads a portfolio. The assistant then scores that
portfolio against five investing frameworks — Dalio, Dimon, Buffett, Blanchard, Marks.

## The four files

| File | Role |
| :--- | :--- |
| `index.html` | The entire web app. Static, self-contained, no build. Fetches the two prompt files at runtime and copies them to the clipboard. |
| `PORTFOLIO-ANALYZER-PROMPT.md` | The analyzer. Takes over the assistant's conversation on load, asks calibration questions, scores the uploaded portfolio. Consumes `CRITERIA.md`. |
| `CRITERIA.md` | The data file the analyzer reads: macro environment, five framework definitions, scoring algorithm, drawdown scenarios, benchmarks. Refreshed roughly monthly. |
| `CRITERIA_UPDATE_PROMPT.md` | The generator that rewrites `CRITERIA.md`. Run periodically; it web-searches for current data and emits a complete replacement file. |

How they relate:

```
CRITERIA_UPDATE_PROMPT.md  --(regenerates, ~monthly)-->  CRITERIA.md
                                                              |
                                                     (read as data by)
                                                              v
index.html  --(fetches + concatenates)-->  PORTFOLIO-ANALYZER-PROMPT.md
```

`CRITERIA.md` is the only file that changes on a schedule. The other three are stable.

## Runtime fetching — do not break these URLs

`index.html` hardcodes two GitHub **API** endpoints (not `raw.githubusercontent.com`):

```
https://api.github.com/repos/<owner>/invest/contents/PORTFOLIO-ANALYZER-PROMPT.md
https://api.github.com/repos/<owner>/invest/contents/CRITERIA.md
```

The API endpoint is deliberate — a prior version used the raw CDN and served stale content for
hours after a push. `CRITERIA_UPDATE_PROMPT.md` fetches its base from the same endpoint. This
has three consequences:

- **The repo must stay public.** The fetches are unauthenticated.
- **Do not rename these files or move them out of the repo root.** The paths are hardcoded in
  three places.
- **Changes must land on `main`** to take effect. There is no deploy step; `main` is production.

The API returns base64 with embedded newlines — `index.html` strips whitespace before `atob()`.
Keep that if you touch the decode path.

## Regenerating CRITERIA.md

This workflow is not obvious from reading the files, and getting it wrong has already caused one
silent two-month outage of the scoring definitions.

1. Open a fresh assistant conversation and paste `CRITERIA_UPDATE_PROMPT.md`.
2. It fetches the current `CRITERIA.md` from the API endpoint as its base, runs an integrity
   gate on it, web-searches for current macro data, and emits a complete replacement file.
3. Commit that output over `CRITERIA.md` and push to `main`.

Rules that matter:

- **It emits the whole file, every time.** Never patches, never "changed sections only."
  Most sections are marked *static — copy verbatim* and must survive byte-identical.
- **The base is always the committed repo copy** — never a pasted copy, a working file, or the
  previous run's output held in context. Truncation propagates: each run's base is the last
  run's output, so one dropped section becomes permanent.
- **The generator must HARD STOP rather than emit a partial file.** Pointers, TODOs, stubs and
  empty sections are banned outright. An aborted run costs one cycle; a file that looks complete
  and isn't gets silently scored against.
- After pushing, verify what the API actually serves — not the local copy. Check the version
  line, that `## SECTION` headings count 25 numbered 1–25, and that the file ends at Section 25.

### CRITERIA.md structure contract

The analyzer's structural check requires **Sections 1–25, sequential, no gaps**. Section 4 holds
the dynamic macro data (14 subsections). Sections 17–21 are the five framework definitions,
22 consensus signals, 23 watch list, 24 the pinned scoring algorithm, 25 benchmarks.

Section 24 must stay byte-identical across refreshes unless a scoring change is intended —
any drift silently makes scores incomparable between runs.

## Running / previewing

No build, no dependencies, no tests. Serve the repo root with any static file server and open
the page:

```
python3 -m http.server 8000
# then open http://localhost:8000
```

Opening `index.html` directly off disk renders correctly, but serve it over HTTP when testing
the clipboard and fetch paths so behaviour matches production. The page always fetches the
prompts from GitHub `main` — it never reads the local copies — so local edits to the markdown
files will not appear in the page until pushed.

## Conventions

- Files are LF in the repo. On Windows, `core.autocrlf` will show a conversion warning on
  commit; that is expected and the stored blob stays LF.
- Version strings live in the file header (`*Version: YYYY-MM-DDa*`) and must match the newest
  Change Log row inside the same file.
- Dates are `YYYY-MM-DD`.
- Each prompt file carries its own Change Log table — add a row when you change behaviour.

## Gotchas

**Markdown in these files is semantic, not cosmetic.** Red-flag thresholds are written inline as
text: `>20 distinct equity holdings`, `Private Credit >15% — Critical`, `Cash/T-bills <20%`.
Reformatting, re-wrapping, or "tidying" `CRITERIA.md` can change what the analyzer scores.
Treat it as data.

**Never round-trip `CRITERIA.md` through Google Docs or a rich-text editor.** This has already
corrupted the file once. Docs escapes markdown punctuation on export — `[verify]` tags come back
as `\[verify\]`, breaking the Section 13 reconciliation — and it reinterprets a `>` at the start
of list content as a blockquote. The red flag `* >20 distinct equity holdings` came back as
`>   * 20 distinct equity holdings`, silently converting "more than 20" into "20". If a refresh
must pass through Docs, export as markdown (not plain text), strip the backslash escapes, and
diff the threshold lines against the previous commit before committing.

**Don't trust "newest complete-looking version" when restoring from history.** Version
`2026-05-16b` has the expected section count but quietly dropped the Howard Marks framework
entirely. The last fully intact ancestor before the 2026-07-28a restore was `2026-05-08a`.
Verify framework sections by name, not by counting headings.

**A self-graded checklist decays.** `CRITERIA_UPDATE_PROMPT.md` carried a compatibility item
requiring "Sections numbered 1–25" while every file it had ever produced began at Section 2.
The check was wrong for months and every run still reported pass. Checklist items in that file
now require reporting measured numbers rather than ticking a box — keep it that way when adding
new ones.
