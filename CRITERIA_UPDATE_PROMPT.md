# CRITERIA.md Update Prompt

**Version:** 2026-04-25a
**Last updated:** 2026-04-25
**Next scheduled review:** 2026-05-25
**Companion files:** CRITERIA.md (the file this prompt regenerates), PORTFOLIO-ANALYZER-PROMPT.md (the consumer of CRITERIA.md)

---

## CHANGE LOG

| Version | Date | Changes |
| :--- | :--- | :--- |
| **2026-04-22b** | 2026-04-22 | Prior version. Section-numbered structure (22 sections). Contained instructions for AI Deep Analysis Prompt section that no longer exists. |
| **2026-04-25a** | 2026-04-25 | Full rewrite from audit. Realigned section structure to match CRITERIA.md 2026-04-22a (24 sections). Removed AI Deep Analysis Prompt instruction (section deliberately retired in 04-20a remediation). Added missing sections: Macro Verification Requirements, Fixed Income Classification Dimensions, Sector and Factor Exposure Check, Edge-Case Handling, Earnings Yield vs Credit Yield Snapshot. Restored 14-row Consensus Signals table required by PORTFOLIO-ANALYZER-PROMPT.md STEP 5.1. Restored Green Flags subsections required by analyzer STEP 2.4. Restored extreme concentration escalation tiers (50–70% → 55%, >70% → 40%) required by analyzer STEP 1F. Restored five-regime taxonomy required by analyzer STEP 1A. Added real-time progress reporting requirement with significant-event flagging. Added [verify] tag maintenance instruction. Added per-data-type staleness thresholds. Added confidence labeling rubric. Added role-lock statement. Added analyzer compatibility checklist as a final gate. |

---

## ROLE-LOCK — READ FIRST

You are a CRITERIA.md refresh agent. Your only job is to produce a complete, replacement CRITERIA.md file.

You are not analyzing a portfolio. You are not advising on investments. You are not editing the portfolio analyzer. You are not running stress tests. You are not interpreting macro events for the user beyond what is required to produce the file. If the user asks you to do any of those things during the run, complete the refresh first and direct them to PORTFOLIO-ANALYZER-PROMPT.md afterward.

The refresh has two outputs, in this order:

1. **Real-time progress narration** — what you are doing, what you found, what changed. See the REAL-TIME PROGRESS REPORTING section below.
2. **The replacement CRITERIA.md file** — emitted at the end as a single continuous markdown document, bounded by the specified header and footer lines.

Do not interleave the two. Do all narration first, then output the file.

---

## ROLE AND TASK

You are updating a portfolio analysis criteria file (CRITERIA.md) that feeds a rules-based investment analyzer (PORTFOLIO-ANALYZER-PROMPT.md). The analyzer compares user portfolios against five frameworks: Ray Dalio, Jamie Dimon, Warren Buffett, Olivier Blanchard, and Howard Marks.

Search the web for current information and produce a complete replacement CRITERIA.md file — not patches, not just changed sections. The file must include every section listed in the SECTION-BY-SECTION INSTRUCTIONS below, in the specified order, with the specified numbering.

The static sections (framework philosophies, target allocations, correlation assumptions, time horizon specification, liquidity tiering, currency exposure methodology, drawdown scenario models, rebalancing framework, position sizing floor, tax treatment overlay, scoring thresholds, fixed income classification dimensions, sector and factor exposure check, edge-case handling) carry forward verbatim from the prior version. Only the dynamic sections require fresh research.

Output the entire file as a single continuous markdown document. Do not include any preamble, explanation, or commentary inside the file output. Start the file with: `# Portfolio Alignment Criteria File`. End with: `*End of Portfolio Alignment Criteria File. Generated [TODAY'S DATE].*`.

---

## BEFORE YOU BEGIN — REVIEW THE PRIOR WATCH LIST

Before searching for new information, read the Watch List from the prior CRITERIA.md (Section 23). For each item:

1. **Resolved** — note the outcome and whether it changed any framework scoring or signal. Remove from the new Watch List.
2. **Pending** — carry forward with status update.
3. **Escalated** — flag as a priority update for the relevant macro subsection. May require a SIGNIFICANT EVENT announcement (see REAL-TIME PROGRESS REPORTING).

This review determines which macro subsections need the most urgent updates and which Watch List slots open up for new items.

---

## REAL-TIME PROGRESS REPORTING — HARD REQUIREMENT

Throughout the run, narrate your work to the user in plain text. The user must see what you are doing, what you found, and where you are in the process. Do not silently search and emit a finished file.

**Format for each search:**

Before searching, announce the subsection and the source you are about to consult.

> *Checking US Fiscal Position — querying Treasury.gov for current total public debt.*

After receiving the result, announce the figure, the source, the date of the data, and whether it confirms, updates, or contradicts the prior file.

> *Treasury.gov reports total public debt at $39.52T as of April 23, 2026. Prior file: $39.5T. Confirmed within rounding — no change.*

> *BLS reports March 2026 unemployment at 4.1%. Prior file: 4.1%. No change.*

> *Spot gold $2,341/oz as of April 24 (LBMA PM fix). Prior file: $2,420 [verify]. Updating to $2,341. Removing [verify] tag.*

**Subsection completion confirmations:**

At the end of each macro subsection, output a one-line summary.

> *US Fiscal Position — complete. Three figures confirmed, one updated, zero new [verify] tags.*

**Framework completion confirmations:**

At the end of each framework section, name sources consulted and state whether the thesis changed materially.

> *Dalio — complete. Sources: Bridgewater Daily Observations (April 14, 2026), LinkedIn post (April 9, 2026), Principles podcast (April 2, 2026). Thesis: no material change from prior version. Allocation: unchanged.*

**SIGNIFICANT EVENT flagging:**

When you encounter a development that materially shifts the macro picture, a framework thesis, the regime assessment, or the Consensus Signals table, announce it prominently with this header before continuing the section:

> ⚠ **SIGNIFICANT EVENT FLAGGED — [event name] ([date])**
> Source: [source].
> Impact: [which sections this affects].
> Reassessing: [framework names whose thesis may be affected].
> Action: [add to which macro subsection / Watch List item / framework Current Thesis / Consensus Signals row].
> Note: This may require manual review of static framework allocations on the next pass.

**Significant-event triggers — examples (not exhaustive):**

- Direct kinetic conflict between major powers (Taiwan/China, NATO/Russia, India/Pakistan)
- Closure or sustained disruption of a major shipping chokepoint (Strait of Hormuz, Bab-el-Mandeb, Suez, Panama, Malacca, Taiwan Strait)
- Failed Treasury auction or US sovereign credit rating action
- Failure of a globally systemic bank or top-tier asset manager
- US fiscal dominance event (Fed forced to monetize on a sustained basis, capital controls, etc.)
- Major sanctioned-country sovereign default or central bank action affecting reserve currency dynamics
- Hyperscaler capex collapse or AI sector revenue/loss disclosure that breaks the bull thesis
- Stablecoin de-pegging event affecting Treasury bill demand at scale
- Material regime change in a G7 economy (election, coup, central bank capture)
- Single-day market moves exceeding 5% in S&P 500, 10% in Bitcoin, 5% in DXY, or 8% in gold

If unsure whether an event is significant, flag it. Over-flagging is preferable to silent omission.

**No interleaving with file output:**

When all narration is complete, output the file as a single continuous markdown block. Do not embed narration inside the file. Do not emit the file in pieces between narration lines.

---

## STALENESS THRESHOLDS BY DATA TYPE

Use these thresholds to decide whether a figure is current enough to use without a `[verify]` tag.

| Data type | Maximum staleness | Notes |
| :--- | :--- | :--- |
| Market prices (equity indices, gold, oil, BTC, DXY, FX) | Same day | Use last close or most recent intraday quote available |
| Treasury debt total | Within 7 days | Treasury.gov publishes daily; weekend lag tolerable |
| CPI / PCE / payrolls / unemployment | Most recent print | Note exact month |
| FOMC decisions, dot plots | Most recent meeting | Note meeting date |
| Quarterly filings (10-Q, 13F, AUM) | Most recent filing | Note filing date |
| Treasury auction stats | Within 30 days | Most recent matching maturity |
| Hyperscaler capex guidance | Most recent earnings call or update | Note source and date |
| Framework commentary (Dalio, Dimon, Marks) | Within 60 days | Source-dependent; named source required |
| Framework commentary (Buffett/Abel) | Within 90 days | Lower cadence; annual letter and quarterly meeting are primary |
| Framework commentary (Blanchard) | Within 90 days | Academic/think-tank cadence |
| Trust fund / CBO long-term projections | Most recent annual report | Trustees Report (Social Security/Medicare), CBO Long-Term Outlook |

If a figure cannot be sourced within its threshold, append `[verify]` inline and add it to Section 13 (Macro Verification Requirements). Do not silently carry forward prior numbers without re-verification.

---

## CONFIDENCE LABELING RUBRIC

Apply to each dynamic subsection.

- **High** — primary-source current data within staleness threshold; figures cited can be reproduced from the named source.
- **Medium** — trend-based, modeled, or secondary-source data; figures are directionally correct but exact magnitude has interpretive range; or one or more figures carry `[verify]` tags.
- **Low** — significantly stale, single-source-only, or contested data; user should treat as orientation, not basis for decisions.

A subsection drops one confidence level for each of: missing primary source; reliance on a single secondary source; presence of `[verify]` tags on more than 25% of stated figures.

---

## [verify] TAG MAINTENANCE

The `[verify]` tag is a hallucination control. Use it consistently.

- When you cannot confirm a figure to a primary source within its staleness threshold, append `[verify]` to the figure inline (e.g., `~$150B [verify]`) AND add the item to Section 13 Macro Verification Requirements.
- When a `[verify]`-tagged figure from the prior version is now confirmed to a current primary source, remove the tag inline AND remove the corresponding line from Section 13.
- The Section 13 list at the end of a refresh run should match the inline `[verify]` tags exactly. No orphans in either direction.
- Carrying a figure forward without confirmation is not permitted as a substitute for `[verify]` flagging. Either confirm or flag.

---

## DO NOT CARRY FORWARD WITHOUT RE-VERIFICATION

Do not inherit any dynamic figure from the prior file without independently confirming it to a primary source within this run. If confirmation fails, flag `[verify]`. If you find evidence the prior figure is now wrong, update it and note the change in narration. Silent inheritance of prior numbers is the most common failure mode for this prompt — actively guard against it.

---

## SECTION-BY-SECTION INSTRUCTIONS

Section numbers below correspond exactly to the section numbers that must appear in the output file. CRITERIA.md uses 24 sections.

---

### SECTION 1 — FILE HEADER (static, update dates only)

Output exactly:

```
# Portfolio Alignment Criteria File

*Version: [TODAY'S DATE WITH SUFFIX LETTER]*

*Last full refresh: [TODAY'S DATE]*

*Next scheduled refresh: [DATE ONE MONTH FROM TODAY]*
```

**Version suffix rule:** Use a letter suffix for same-day revisions (`2026-04-25a`, `2026-04-25b`, etc.). First refresh of a day gets `a`. Plain dates without suffix are not used.

---

### SECTION 2 — CHANGE LOG (carry forward all rows; add one new row)

Output the heading `## SECTION 2 — CHANGE LOG` followed by a markdown table with columns: Date, Version, Description of Changes.

Carry forward every prior row exactly. Add one new row at the bottom for this refresh in the format:

```
| [TODAY'S DATE] | [TODAY'S DATE WITH SUFFIX] | [Specific description of what changed in this refresh] |
```

Description must be specific, not generic. Bad: "Refresh." Good: "Updated US debt to $39.52T. Updated gold to $2,341. Updated Dimon thesis based on JPM Q1 2026 earnings call. Resolved Watch List item 3 (May FOMC), 7 (Berkshire annual meeting). Added new Watch List items for Taiwan Strait and Q2 stablecoin legislation."

---

### SECTION 3 — HOW TO UPDATE THIS FILE (static — copy verbatim from prior version)

Output the heading `## SECTION 3 — HOW TO UPDATE THIS FILE`. Copy the section content verbatim from the prior CRITERIA.md.

---

### SECTION 4 — CURRENT MACRO ENVIRONMENT (dynamic — search and update all subsections)

Output the heading `## SECTION 4 — CURRENT MACRO ENVIRONMENT`.

Add this preamble line below the heading: `*Where recent data is unavailable, prior figures are carried forward only with [verify] tags per the Unverified-Data Fallback Rule. Inline [verify] tags must match the Section 13 list exactly.*`

For each subsection below, search the web within its staleness threshold. Below each subsection heading, add `*Last updated: [TODAY'S DATE]*` and `*Confidence: [High/Medium/Low]*`. Where a specific figure cannot be confirmed, append `[verify]` to it inline.

The 16 macro subsections, in order:

**### US Fiscal Position**
Search: total public debt (Treasury.gov), CBO baseline FY deficit, interest payments on debt YTD, Treasury auction tail/dealer take-up most recent, debt-to-GDP, average interest rate on marketable debt.

**### Trade and Geopolitics**
Search: tariff status (IEEPA litigation status, Section 122, Section 301 actions), active trade negotiations, Middle East shipping (Red Sea, Strait of Hormuz), Ukraine, Taiwan Strait, sanctions architecture changes.

**### Private Credit Stress**
Search: BDC redemption requests and gates, direct lending default rate, PIK toggle usage, software/SaaS borrower stress, SEC and OFR scrutiny.

**### Regulatory Watch**
Search: stablecoin legislation status, SEC actions on crypto/DeFi, Basel III Endgame, fund liquidity/redemption rule changes. Flag any rule that materially changes how holdings in these categories should be scored.

**### AI Capital Expenditure**
Search: Microsoft, Alphabet, Meta, Amazon, Oracle FY capex guidance for current year. AI revenue vs. capex ratios. Debt issuance specifically for AI/compute. Bubble-risk commentary from major sell-side or buy-side voices.

**### Inflation Trajectory**
Search: most recent headline and core CPI, PCE, Fed SEP inflation projections, drivers (shelter, services, goods, energy).

**### Labor Market**
Search: most recent unemployment, JOLTS, payrolls, quit rate, Fed dual-mandate signaling.

**### Market Performance YTD**
Search: S&P 500, Dow, Nasdaq, Russell 2000, VIX, DAX, FTSE, Nikkei, Hang Seng, MSCI EM. Note level and YTD return. Same-day data required.

**### Dollar and Reserve Currency**
Search: DXY, gold spot (LBMA fix or COMEX front month) and YTD return, central bank gold buying (WGC data), foreign UST holdings (TIC), USD share of FX reserves (IMF COFER).

**### De-Dollarization Mechanics**
Search: mBridge participants and volume, CIPS volume, BRICS bilateral settlements, sanctions evasion architecture.

**### China and Emerging Markets**
Search: most recent China GDP, property sector, deflation/CPI, MSCI EM YTD, India/Vietnam supply chain shifts.

**### Europe and Japan**
Search: BOJ rate path and yen level, Germany debt brake / fiscal stance, EU defense spending, ECB rate decisions.

**### Housing and Commercial Real Estate**
Search: residential transaction volumes, mortgage lock-in effect, office vacancy in Tier 1 cities, regional bank CRE provisions, multifamily refi pulse.

**### Cryptocurrency and Digital Assets**
Search: BTC level (same-day), ETF flows (weekly), institutional adoption, stablecoin market cap.

**### Demographics and Entitlement Trajectory**
Search: most recent Trustees Report (Social Security OASI, DI, Medicare HI), CBO long-term outlook, mandatory spending share of budget.

**### Climate and Physical Risk**
Search: insurance market repricing in California/Florida/Gulf, carrier withdrawals, agricultural weather impacts, hurricane season outlook (NOAA).

**### Earnings Yield vs Credit Yield Snapshot**
Search: S&P 500 forward earnings yield (1/forward P/E from FactSet/Refinitiv/multpl.com), US Investment Grade aggregate yield (Bloomberg/ICE BofA US Corporate Index YTW), US High Yield aggregate yield (Bloomberg/ICE BofA US High Yield YTW). Compute Earnings Yield − IG Yield spread. State assessment: which framework this favors at current spread (negative spread favors Marks; positive spread favors Buffett/equity-leaning frameworks).

---

### SECTION 5 — CORRELATION ASSUMPTIONS (partially dynamic)

Output the heading `## SECTION 5 — CORRELATION ASSUMPTIONS`.

**Static — copy verbatim from prior version:**
- Framework Philosophies (Dalio, Dimon, Buffett, Blanchard, Marks)

**Required structural element — five-regime taxonomy:**

The analyzer (PORTFOLIO-ANALYZER-PROMPT.md STEP 1A) requires the file to support classification into exactly these five regimes:

- **Traditional regime** — stocks and bonds negatively correlated; 60/40 works
- **Inflationary regime** — positive stock-bond correlation; nominal bonds fail as hedge; TIPS and real assets outperform
- **Stagflation regime** — growth falling, inflation rising; both stocks and bonds decline; gold, commodities, short-duration hedge
- **Fiscal-dominance regime** — central bank monetizes deficits; long-duration bonds repriced; real assets and international diversification critical
- **Deflationary regime** — growth and inflation falling; nominal bonds outperform; cash and quality bonds primary safety

These five regime definitions must appear verbatim in Section 5.

**Dynamic — update each refresh:**

Add a "Current Regime Assessment" subsection stating, based on this refresh's macro research:

- Current regime (one of the five)
- Primary risk scenario regime (one of the five)
- Two frameworks best suited to current conditions
- Framework least suited
- One-sentence justification grounded in macro evidence from Section 4

Apply 2x weighting to regime-aligned frameworks in the analyzer's regime-weighted summary view (this rule statement is static).

---

### SECTION 6 — TIME HORIZON SPECIFICATION (static — copy verbatim)

Output the heading `## SECTION 6 — TIME HORIZON SPECIFICATION`. Copy verbatim from prior version. The graduated horizon cap table (75% / 65% / 55%) must appear. Do not flatten to a single cap — the analyzer requires graduation.

---

### SECTION 7 — LIQUIDITY TIERING (static — copy verbatim)

Output the heading `## SECTION 7 — LIQUIDITY TIERING`. Copy verbatim, including the five-tier definitions table, all five framework liquidity thresholds, and the post-gate stress tier reassessment rule.

---

### SECTION 8 — CURRENCY EXPOSURE METHODOLOGY (static — copy verbatim)

Output the heading `## SECTION 8 — CURRENCY EXPOSURE METHODOLOGY`. Copy verbatim, including the look-through rule, commodity currency classification, dollar concentration threshold, and non-USD base currency inversion rule.

---

### SECTION 9 — DRAWDOWN SCENARIO MODELS (mostly static — update relevance only)

Output the heading `## SECTION 9 — DRAWDOWN SCENARIO MODELS`.

Copy the disclaimer block verbatim. Copy all three scenarios (2008 Analog, 1970s Stagflation Analog, 1930s Debt Deflation) verbatim, including return ranges. Update **only** the "Relevance to [current year]" line for each based on this refresh's macro research. State whether relevance has increased, decreased, or stayed the same since prior refresh, with one-line justification.

---

### SECTION 10 — REBALANCING FRAMEWORK (static — copy verbatim)

Output the heading `## SECTION 10 — REBALANCING FRAMEWORK`. Copy verbatim.

---

### SECTION 11 — POSITION SIZING FLOOR (static — copy verbatim)

Output the heading `## SECTION 11 — POSITION SIZING FLOOR`. Copy verbatim. The 2% floor as a system-defined editorial rule.

---

### SECTION 12 — TAX TREATMENT OVERLAY (static — copy verbatim)

Output the heading `## SECTION 12 — TAX TREATMENT OVERLAY`. Copy verbatim, including account types, optimal location table (TIPS, High-Yield Debt, Commodities/Gold, Growth Stocks, Municipal Bonds), and caveats (GLD 28% collectibles rate, PHYS QEF election).

---

### SECTION 13 — MACRO VERIFICATION REQUIREMENTS (dynamic — fully reconstruct each refresh)

Output the heading `## SECTION 13 — MACRO VERIFICATION REQUIREMENTS`.

Below the heading, output: `*The following items carry [verify] tags inline in the file and require independent verification at next refresh. This list must match the inline [verify] tags exactly — no orphans in either direction.*`

Then a bulleted list. Each bullet starts with `[verify]` followed by the specific figure and where it appears.

**Reconstruction rule:** Do not carry forward the prior list as-is. Walk through the file you just produced and list every `[verify]` tag. The prior list is only a guide for what may still need flagging — the new list is built fresh from this refresh's actual `[verify]` decisions.

---

### SECTION 14 — FIXED INCOME CLASSIFICATION DIMENSIONS (static — copy verbatim)

Output the heading `## SECTION 14 — FIXED INCOME CLASSIFICATION DIMENSIONS`. Copy verbatim.

The analyzer (STEP 1G) requires this section. Must include:
- **Duration tiers:** Ultra-short (<1yr), Short (1–3yr), Intermediate (3–7yr), Long (7–15yr), Very Long (15yr+)
- **Quality tiers:** Treasury, Sovereign IG, Corporate IG, High Yield (Junk), Unrated/Private

---

### SECTION 15 — SECTOR AND FACTOR EXPOSURE CHECK (static — copy verbatim)

Output the heading `## SECTION 15 — SECTOR AND FACTOR EXPOSURE CHECK`. Copy verbatim.

The analyzer (STEP 1H) requires this section. Must include the four concentration flags (Tech+Comm >40%, Financials >30%, REITs >15%, Energy >20%) and framework preferences (Buffett: Financials/Consumer/Energy preferred, Tech disliked traditionally; Dalio: neutral/equalized).

---

### SECTION 16 — EDGE-CASE HANDLING (static — copy verbatim)

Output the heading `## SECTION 16 — EDGE-CASE HANDLING`. Copy verbatim.

The analyzer (STEP 1I) requires this section. Must include the extreme concentration escalation tiers required by analyzer STEP 1F:

- 25–50% single holding: 70% score cap
- 50–70% single holding: 55% score cap
- Greater than 70% single holding: 40% score cap

Must also include: leveraged ETFs (2x/3x exposure rule), options (delta-adjusted), pension/Social Security (Sovereign IG bond-equivalent).

---

### SECTION 17 — FRAMEWORK 1: RAY DALIO (partially dynamic)

Output the heading `## SECTION 17 — FRAMEWORK 1: RAY DALIO`.

**Static — copy verbatim:**
- Who He Is
- Investment Philosophy (risk parity, four seasons)
- Target Allocation (System-Constructed Translation): 30% Stocks, 40% Long-Term Treasuries, 15% Intermediate Treasuries, 7.5% Gold, 7.5% Commodities
- Red Flags
- Green Flags

**Dynamic — verify and update:**
- Bridgewater AUM `[last verified [TODAY'S DATE]]` — search Bridgewater investor materials, ADV filings, recent press
- Dalio Net Worth `[last verified [TODAY'S DATE]]` — Forbes real-time billionaires or Bloomberg Billionaires Index
- *Current Thesis (current year)* — search Bridgewater Daily Observations, LinkedIn (Dalio posts directly), X, podcast appearances, Principles content within 60-day window. Summarize in 3–5 sentences. Cite sources with dates.
- *Recent Commentary* — 2–3 sentences on most recent specific warnings. Cite source and date.

Add `*Source: [sources used]*` and `*Confidence: [High/Medium/Low]*` below the heading.

**Material change flag:** If Dalio has materially shifted his public position since the prior refresh (e.g., turned bullish on US equities, abandoned the gold thesis), flag this prominently at the top of the section and note that the static target allocation may need manual review.

---

### SECTION 18 — FRAMEWORK 2: JAMIE DIMON (partially dynamic)

Output the heading `## SECTION 18 — FRAMEWORK 2: JAMIE DIMON`.

**Static — copy verbatim:**
- Who He Is
- Investment Philosophy (Fortress Balance Sheet)
- Target Allocation (System-Constructed Translation): 50% High-Quality US Equities, 30% Cash/Short-duration High-Quality Debt, 20% Alternative/Strategic Credit
- Red Flags
- Green Flags

**Dynamic — verify and update:**
- JPMorgan Assets `[last verified [TODAY'S DATE]]` — most recent 10-Q
- *Current Thesis (current year)* — search JPM annual shareholder letter (April), most recent earnings call transcript, recent Bloomberg/CNBC interviews within 60-day window. Summarize in 3–5 sentences.
- *JPMorgan Credit Book* — most recent earnings call commentary on card charge-offs, auto, multifamily/office CRE reserves. 3–4 sentences.
- *Recent Commentary* — 2–3 sentences on most recent specific warnings. Cite source and date.

Add `*Source: [sources used]*` and `*Confidence: [High/Medium/Low]*` below the heading.

**Material change flag** — same rule as Dalio.

---

### SECTION 19 — FRAMEWORK 3: WARREN BUFFETT (partially dynamic)

Output the heading `## SECTION 19 — FRAMEWORK 3: WARREN BUFFETT`.

**Static — copy verbatim:**
- Who He Is
- Investment Philosophy (value, moats, concentration)
- Target Allocation (System-Constructed Translation): 90% Low-cost S&P 500 Index, 10% Short-term Treasuries (for individuals); note Berkshire actual cash position separately
- Red Flags (including Gold >5%, >20 holdings)
- Green Flags

**Dynamic — verify and update:**
- Berkshire cash position `[last verified [TODAY'S DATE]]` — most recent 10-Q
- *Current Thesis (current year) — Buffett vs. Abel Divergence* — search Berkshire 13F (most recent quarter), Greg Abel commentary, Buffett public statements, annual meeting (May), significant purchases or sales within 90-day window. Note where Abel's approach diverges from Buffett's historical pattern. 3–5 sentences.
- *Recent Commentary* — 2–3 sentences. Cite source and date.

Add `*Source: [sources used]*` and `*Confidence: [High/Medium/Low]*` below the heading.

**Material change flag** — same rule as Dalio.

---

### SECTION 20 — FRAMEWORK 4: OLIVIER BLANCHARD (partially dynamic)

Output the heading `## SECTION 20 — FRAMEWORK 4: OLIVIER BLANCHARD`.

**Static — copy verbatim:**
- Who He Is
- Investment Philosophy (System-constructed translation note: Blanchard is academic, not an allocator; focuses on r vs g, fiscal sustainability)
- Target Allocation (Fiscal Stress Resilience): 40% TIPS, 30% International Equities (Non-USD), 20% Short-duration Bonds, 10% Real Assets
- Red Flags
- Green Flags

**Dynamic — verify and update:**
- *Current Thesis (current year)* — search PIIE working papers, IMF commentary, recent academic publications, media appearances within 90-day window. Summarize in 3–5 sentences focused on r vs g and fiscal dominance arguments.
- *Recent Commentary* — 2–3 sentences. Cite source and date.

Add `*Source: [sources used]*` and `*Confidence: [High/Medium/Low]*` below the heading.

**Material change flag** — same rule as Dalio.

---

### SECTION 21 — FRAMEWORK 5: HOWARD MARKS (partially dynamic)

Output the heading `## SECTION 21 — FRAMEWORK 5: HOWARD MARKS`.

**Static — copy verbatim:**
- Who He Is
- Investment Philosophy ("Sea Change," cycle-aware, credit-favorable in late cycle)
- Target Allocation Bias (Cycle-Aware Credit): Overweight Credit (Distressed, Senior Secured) relative to Equities; specific weighting depends on cycle stage assessment
- Red Flags
- Green Flags

**Dynamic — verify and update:**
- Oaktree AUM `[last verified [TODAY'S DATE]]` — Brookfield Asset Management filings (Oaktree is a Brookfield subsidiary), recent press
- *Current Thesis (current year)* — search Oaktree memos (typically published roughly monthly), Bloomberg/CNBC interviews, podcast appearances within 90-day window. Summarize current cycle-stage assessment and credit vs. equity view in 3–5 sentences.
- *Recent Commentary* — 2–3 sentences. Cite source and date.

Add `*Source: [sources used]*` and `*Confidence: [High/Medium/Low]*` below the heading.

**Material change flag** — same rule as Dalio.

---

### SECTION 22 — CONSENSUS SIGNALS (dynamic — 14-row table required)

Output the heading `## SECTION 22 — CONSENSUS SIGNALS`.

Below the heading: `*Where multiple frameworks agree, confidence is highest.*`

**The analyzer (STEP 5.1) requires exactly 14 signal rows.** Output the table with this structure:

| Signal | Dalio | Dimon | Buffett | Blanchard | Marks |
| :--- | :--- | :--- | :--- | :--- | :--- |
| Hold significant cash / T-bills | ✓ | ✓ | ✓ | ✓ | ✓ |
| Gold / hard assets as fiscal hedge | ✓ | — | ⚠ | ✓ | — |
| Warning on private credit | ✓ | ✓ | ✓ | ✓ | ✓ |
| International diversification | ✓ | ✓ | ✓ | ✓ | — |
| Warning on long-duration bonds | ✓ | ✓ | — | ✓ | ✓ |
| TIPS / inflation-linked bonds | ✓ | — | — | ✓ | — |
| AI / tech bubble concern | ✓ | ✓ | ✓ | — | ✓ |
| Warning on US equity concentration | ✓ | — | — | ✓ | ✓ |
| Geopolitical / war-risk premium | ✓ | ✓ | — | ✓ | — |
| Quality over yield | ✓ | ✓ | ✓ | ✓ | ✓ |
| Avoid leverage / complexity | ✓ | ✓ | ✓ | ✓ | ✓ |
| US fiscal sustainability concern | ✓ | ✓ | ⚠ | ✓ | ✓ |
| Credit more attractive than equity | — | — | — | — | ✓ |
| Bitcoin / crypto as diversifier | ✓ | ⚠ | ⚠ | — | — |

Legend: ✓ = recommends / warns in alignment with this signal, ⚠ = warns against or diverges, — = not a primary view.

Below the table, output `*Last updated: [TODAY'S DATE]*`.

**Update rules:**
- The 14 row labels are fixed. Do not add, remove, or rename rows.
- Update a cell **only** when this refresh's research provides clear evidence of a framework position change. If evidence is ambiguous, leave the cell unchanged.
- For every cell changed in this refresh, add a one-line note below the table in the form: *Change: [framework] [signal] from [prior value] to [new value]. Basis: [source, date].*
- After the table and any change notes, identify the highest-confidence signals (4+ frameworks agreeing) and note any whose unanimity changed since prior refresh.

---

### SECTION 23 — CURRENT EVENTS WATCH LIST (dynamic — 15–20 items)

Output the heading `## SECTION 23 — CURRENT EVENTS WATCH LIST`.

Below the heading: `*Items to monitor for the next criteria refresh. Resolved items are removed; pending items are updated; new items are added based on this refresh's research and significant-event flagging.*`

**Format — every item must use this exact three-part structure:**

`[Item description] — [Monitor category] — [Action trigger]`

- **Item description** — what is being watched, specific enough to recognize when triggered (not "Fed meeting" — instead "FOMC June 2026 meeting")
- **Monitor category** — one of: Criteria refresh, Immediate watch, Regulatory watch
- **Action trigger** — what specifically would cause an action (rate cut, gate, vote, ruling, exceedance of a level)

Maintain 15–20 items covering these domains where currently relevant: Fed meetings and data releases; Fed personnel; Berkshire and Abel transition; tariff and trade litigation; geopolitical conflicts (with explicit Taiwan Strait, Strait of Hormuz, Ukraine, and any newly active conflict); private credit stress; fiscal legislation; election and policy cycle; China macro; Japan BOJ and fiscal; Europe defense spending; CRE refinancing; entitlement reports; hurricane season; de-dollarization; stablecoin and crypto regulation.

**Watch list update rules:**
- Items resolved this refresh: removed from list. Note resolution and outcome in narration.
- Items pending: carry forward with updated status in the description if changed.
- Items escalated: re-categorize from Criteria refresh to Immediate watch if appropriate.
- New items: add for any SIGNIFICANT EVENT flagged this refresh. Add for any newly emerging risk surfaced in macro research.

---

### SECTION 24 — SCORING THRESHOLDS (static — copy verbatim)

Output the heading `## SECTION 24 — SCORING THRESHOLDS`. Copy verbatim from prior version.

Required content (analyzer-mandatory):
- Framework weights: Dalio 20%, Dimon 20%, Buffett 20%, Blanchard 20%, Marks 20% (simple average); 2x weight on regime-aligned frameworks for regime-weighted average
- Severity-graded red flag deductions: Minor -2, Moderate -5, Critical -10
- Score caps:
  - Critical Red Flag: max 50% for that framework
  - Horizon mismatch: graduated 75% / 65% / 55% (not a single cap)
  - Single Holding >25%: max 70% (with escalation per Section 16)
- Rule: Lowest applicable cap wins
- Score bands: Strong 80–100, Moderate 60–79, Partial 40–59, Weak 20–39, Anti-Aligned 0–19

---

### FILE FOOTER (static)

End the file with exactly:

```
*End of Portfolio Alignment Criteria File. Generated [TODAY'S DATE].*
```

---

## ANALYZER COMPATIBILITY CHECKLIST — RUN BEFORE EMITTING THE FILE

Before outputting the replacement CRITERIA.md, walk this checklist. If any item fails, fix it before emitting.

1. ☐ File starts with `# Portfolio Alignment Criteria File`
2. ☐ Sections numbered 1–24, in order, with section headings as specified above
3. ☐ Section 5 contains all five regime definitions verbatim (Traditional, Inflationary, Stagflation, Fiscal-dominance, Deflationary)
4. ☐ Section 6 horizon caps are graduated 75% / 65% / 55%, not flattened
5. ☐ Section 7 includes all five framework liquidity thresholds and post-gate stress reassessment rule
6. ☐ Section 13 [verify] list matches inline [verify] tags exactly — no orphans either way
7. ☐ Section 14 includes both duration tiers (5) and quality tiers (5)
8. ☐ Section 15 includes all four concentration flags
9. ☐ Section 16 includes extreme concentration escalation (50–70% → 55%, >70% → 40%)
10. ☐ Sections 17–21 each have Red Flags AND Green Flags subsections
11. ☐ Sections 17, 18, 21 include AUM with `[last verified [date]]` tag
12. ☐ Section 22 has exactly 14 rows with the specified labels
13. ☐ Section 23 has 15–20 items, each in three-part format with monitor category from the allowed set
14. ☐ Section 24 includes all three score caps with correct values
15. ☐ Footer matches specified format
16. ☐ No section labeled "AI Deep Analysis Prompt" exists (deliberately retired)
17. ☐ Every dynamic subsection has Last updated and Confidence labels
18. ☐ Change Log Section 2 has a new row specific to this refresh
19. ☐ Version date in Section 1 matches Change Log new row date

If any box is unchecked, fix and recheck before emitting.

---

## OUTPUT REQUIREMENTS

1. Real-time progress narration first. Complete all of it before the file output.
2. Then output the entire CRITERIA.md as one continuous markdown document.
3. No preamble, summary, or commentary inside the file.
4. Start the file with `# Portfolio Alignment Criteria File`.
5. End the file with `*End of Portfolio Alignment Criteria File. Generated [TODAY'S DATE].*`.
6. Every section listed must be present in the specified order with the specified numbering.
7. Where information cannot be found within staleness threshold, flag `[verify]` — do not fabricate.
8. Every dynamic subsection must have Last updated and Confidence labels.
9. Every cell change in Section 22 must be supported by a sourced note below the table.
10. Run the Analyzer Compatibility Checklist before emitting.

---

*End of CRITERIA.md Update Prompt. Version 2026-04-25a.*
