# Criteria File Update Prompt

Paste this entire prompt into Claude.ai or ChatGPT (with web search enabled) to generate a complete replacement CRITERIA.md file.

---

## ROLE AND TASK

You are updating a portfolio analysis criteria file that feeds a rules-based investment analyzer tool. The analyzer compares user portfolios against five frameworks: Ray Dalio, Jamie Dimon, Warren Buffett, Olivier Blanchard, and Howard Marks.

Search the web for current information and generate a complete replacement CRITERIA.md file — not just the updated sections. The file must include every section listed below. Do not omit any section.

The static sections (framework philosophy, target allocations, correlation assumptions, time horizon specification, liquidity tiering, currency exposure methodology, drawdown scenario models, rebalancing framework, position sizing floor, tax treatment overlay, scoring thresholds, AI analysis prompt) should be carried forward accurately from the prior version. Only the dynamic sections require fresh research.

Output the entire file as a single continuous markdown document, ready to save and use immediately. Do not include any preamble, explanation, or commentary before or after the file. Start the output with the line: `# Portfolio Alignment Criteria File`. End with: `*End of Portfolio Alignment Criteria File. Generated [TODAY'S DATE].*`

---

## BEFORE YOU BEGIN — REVIEW THE PRIOR WATCH LIST

Before searching for new information, review the Watch List from the prior CRITERIA.md. For each item on that list:

1. Note whether it has resolved, is still pending, or has escalated
2. If resolved: briefly state the outcome and whether it changed any framework scoring
3. If pending: carry it forward with updated status
4. If escalated: flag it as a priority update for the relevant macro subsection

This review should inform which macro subsections require the most urgent updates.

---

## INSTRUCTIONS BY SECTION

---

### SECTION 1 — FILE HEADER (static, update dates only)

Output exactly:

```
# Portfolio Alignment Criteria File

*Version: [TODAY'S DATE]*
*Last full refresh: [TODAY'S DATE]*
*Next scheduled refresh: [DATE ONE MONTH FROM TODAY]*
```

---

### SECTION 2 — CHANGE LOG (update with new row)

Carry forward all prior rows. Add one new row for this refresh using the format:

```
| [TODAY'S DATE] | [TODAY'S DATE] | [Brief description of what changed in this refresh] |
```

---

### SECTION 3 — HOW TO UPDATE THIS FILE (static, copy exactly from prior version)

Copy this section verbatim.

---

### SECTION 4 — CURRENT MACRO ENVIRONMENT (dynamic — search and update all subsections)

Search for current news (within the last 30 days) on each subsection below. For each subsection, include the date of the data point where possible. Add `*Last updated: [TODAY'S DATE]*` and `*Confidence: [High/Medium/Low]*` below the main heading. If you cannot find recent information for a subsection, say so explicitly — do not fabricate or use stale data.

Output under heading `## CURRENT MACRO ENVIRONMENT` with the following subheadings:

**### US Fiscal Position**
Search: US national debt current level, FY deficit projection, CBO baseline, interest payments on debt, Treasury auction demand, debt-to-GDP trajectory.

**### Trade and Geopolitics**
Search: current US tariff status (IEEPA ruling aftermath, Section 122, Section 301 investigations), active trade negotiations, geopolitical conflicts affecting markets (Middle East, Ukraine, China-Taiwan), sanctions developments.

**### Private Credit Stress**
Search: private credit fund redemption requests, fund gates or suspensions, default rates in direct lending, software/SaaS loan stress, regulatory attention to private credit, comparisons to prior credit cycles.

**### Regulatory Watch**
Search: regulatory developments affecting private credit (Congressional hearings, SEC/Treasury actions), stablecoin legislation progress, crypto regulatory actions from SEC or CFTC, any new rules affecting fund liquidity or redemption structures. Flag any development that materially changes how holdings in these categories should be scored.

**### AI Capital Expenditure**
Search: hyperscaler capex announcements for current year (Amazon, Alphabet, Meta, Microsoft, Oracle), AI infrastructure spending projections, capex-to-revenue ratios, debt issuance to fund AI buildout, AI revenue versus investment gap, bubble risk assessments.

**### Inflation Trajectory**
Search: most recent CPI release, core CPI, PCE, Fed SEP inflation projections, inflation drivers (energy, shelter, tariffs), Fed communications on inflation path.

**### Labor Market**
Search: most recent unemployment rate, FOMC SEP unemployment projections, Fed dual-mandate tension, recent payrolls data, labor market fragility signals.

**### Market Performance YTD**
Search: S&P 500 current level and YTD return, Dow, Nasdaq, Russell 2000, VIX, major international indices (DAX, FTSE, Nikkei, Hang Seng), factor performance (value vs. growth, low-vol vs. high-vol), emerging markets performance.

**### Dollar and Reserve Currency**
Search: DXY current level and trend, gold price current level and YTD return, central bank gold purchases, foreign holdings of US Treasuries (TIC data), dollar share of global FX reserves, gold price forecasts from major banks.

**### De-Dollarization Mechanics**
Search: mBridge CBDC platform developments and new members, CIPS volume, BRICS+ bilateral currency settlements, sanctions architecture developments, alternative reserve currency progress.

**### China and Emerging Markets**
Search: China GDP growth most recent quarter, China property sector developments, Chinese consumer and deflation risk, China energy exposure to Middle East, MSCI EM performance, India/Vietnam supply chain developments.

**### Europe and Japan**
Search: Germany fiscal expansion and debt brake status, EU defense spending trajectory, European equity performance vs. US, BOJ policy normalization, yen direction, Japan fiscal framework changes, carry trade unwind risk.

**### Housing and Commercial Real Estate**
Search: US shelter inflation current rate, residential transaction volumes, commercial real estate refinancing stress, office CRE conditions, regional bank CRE exposure, data center and industrial CRE performance.

**### Cryptocurrency and Digital Assets**
Search: Bitcoin price and institutional adoption developments, spot ETF flows, stablecoin market cap and Treasury bill demand, regulatory developments.

**### Demographics and Entitlement Trajectory**
Search: Social Security and Medicare trust fund projections, mandatory spending trajectory, CBO long-term fiscal projections, entitlement reform prospects.

**### Climate and Physical Risk**
Search: insurance market repricing in climate-exposed regions, insurer withdrawals from high-risk markets, agricultural commodity volatility from weather, infrastructure resilience spending.

---

### SECTION 5 — CORRELATION ASSUMPTIONS (partially dynamic)

Copy the static framework descriptions verbatim from the prior version. Then update the **Current regime assessment** line at the bottom of the section based on your macro research. State: current regime, primary risk scenario regime, and which two frameworks are best suited to current conditions.

---

### SECTION 6 — TIME HORIZON SPECIFICATION (static, copy exactly from prior version)

Copy this section verbatim.

---

### SECTION 7 — LIQUIDITY TIERING (static, copy exactly from prior version)

Copy this section verbatim, including the tier definitions table and all five framework liquidity thresholds.

---

### SECTION 8 — CURRENCY EXPOSURE METHODOLOGY (static, copy exactly from prior version)

Copy this section verbatim, including all classification rules and dollar concentration thresholds.

---

### SECTION 9 — DRAWDOWN SCENARIO MODELS (static, copy exactly from prior version)

Copy all three scenarios verbatim. Update only the **Relevance to [current year]** line for each scenario based on your macro research — specifically whether the scenario's relevance has increased, decreased, or stayed the same since the last refresh.

---

### SECTION 10 — REBALANCING FRAMEWORK (static, copy exactly from prior version)

Copy this section verbatim.

---

### SECTION 11 — POSITION SIZING FLOOR (static, copy exactly from prior version)

Copy this section verbatim.

---

### SECTION 12 — TAX TREATMENT OVERLAY (static, copy exactly from prior version)

Copy this section verbatim, including the account type definitions, optimal asset location rules table, tax mislocation flag instructions, and note on international users.

---

### SECTION 13 — FRAMEWORK 1: RAY DALIO (partially dynamic)

**Static subsections — copy accurately:**
- Who He Is
- Investment Philosophy — All Weather framework, risk parity, 15 uncorrelated streams
- Target Allocation (All Weather) — US Equities 15%, Intl Equities 15%, Long-Term Bonds 20%, Gold/Hard Assets 20%, Commodities 10%, Alternatives/Macro 10%, Cash/Short-Term 10%
- Red Flags
- Green Flags

**Dynamic subsections — search and update:**

*Current Thesis (current year)* — Search for Dalio's most recent public statements, LinkedIn posts, X posts, Bridgewater research, interviews, or conference appearances in the last 60 days. Summarize in 3–5 sentences. Include source and date. Flag if his stated position has changed materially from the prior version.

*Recent Commentary* — 2–3 sentences on his most recent specific warnings or recommendations. Include source and date.

Add `*Source: [sources used]*` and `*Confidence: [High/Medium/Low]*` below the heading.

---

### SECTION 14 — FRAMEWORK 2: JAMIE DIMON (partially dynamic)

**Static subsections — copy accurately:**
- Who He Is
- Investment Philosophy
- Target Allocation (Fortress Balance Sheet)
- Red Flags
- Green Flags

**Dynamic subsections — search and update:**

*Current Thesis (current year)* — Search for Dimon's most recent statements, JPMorgan earnings calls, CNBC or Bloomberg interviews, and annual shareholder letter (typically released in April). Summarize in 3–5 sentences.

*JPMorgan Credit Book as Leading Indicator* — Search for JPMorgan's most recent earnings call commentary on consumer credit (card charge-offs, delinquencies), auto loan stress, and commercial real estate reserve builds. Summarize in 3–4 sentences.

*Recent Commentary* — 2–3 sentences on his most recent specific warnings. Include source and date.

Add `*Source: [sources used]*` and `*Confidence: [High/Medium/Low]*` below the heading.

---

### SECTION 15 — FRAMEWORK 3: WARREN BUFFETT (partially dynamic)

**Static subsections — copy accurately:**
- Who He Is
- Investment Philosophy
- Target Allocation (Berkshire Model)
- Red Flags
- Green Flags

**Dynamic subsections — search and update:**

*Current Thesis (current year) — Buffett vs. Abel Divergence* — Search for Berkshire 13F filings, Greg Abel commentary, Buffett public statements, Berkshire cash position updates, significant purchases or sales. Note explicitly where Abel's approach may be diverging from Buffett's historical pattern. Summarize in 3–5 sentences.

*Recent Commentary* — 2–3 sentences on most recent Buffett or Abel commentary. Include source and date.

Add `*Source: [sources used]*` and `*Confidence: [High/Medium/Low]*` below the heading.

---

### SECTION 16 — FRAMEWORK 4: OLIVIER BLANCHARD (partially dynamic)

**Static subsections — copy accurately:**
- Who He Is
- Investment Philosophy
- Target Allocation (Fiscal Stress Resilience)
- Red Flags
- Green Flags

**Dynamic subsections — search and update:**

*Current Thesis (current year)* — Search for Blanchard publications, Peterson Institute papers, IMF commentary, media appearances in last 90 days. Summarize in 3–5 sentences.

*Recent Commentary* — 2–3 sentences on most recent specific warnings or publications. Include source and date.

Add `*Source: [sources used]*` and `*Confidence: [High/Medium/Low]*` below the heading.

---

### SECTION 17 — FRAMEWORK 5 (SUPPLEMENTARY): HOWARD MARKS (partially dynamic)

**Static subsections — copy accurately:**
- Who He Is
- Investment Philosophy
- Target Allocation Bias (Cycle-Aware Credit)
- Red Flags
- Green Flags

**Dynamic subsections — search and update:**

*Current Thesis (current year)* — Search for Oaktree memos, Marks public interviews, Bloomberg or CNBC appearances in last 90 days. Summarize his current cycle-stage assessment and credit vs. equity view in 3–5 sentences.

*Recent Commentary* — 2–3 sentences on most recent specific observations. Include source and date.

Add `*Source: [sources used]*` and `*Confidence: [High/Medium/Low]*` below the heading.

**Additional check:** If any framework thinker has materially changed their public position since the last refresh (e.g., Dalio turns bullish on US equities, Marks turns negative on all credit), flag this prominently at the top of that framework section and note that the static philosophy sections may need manual review.

---

### SECTION 18 — CONSENSUS SIGNALS (dynamic — update based on research above)

Output under heading `## CONSENSUS SIGNALS` with note `*Where multiple frameworks agree, confidence is highest*`

Carry forward the existing 14-row table. Update any cell only where your research provides clear evidence of a framework position change — do not change cells speculatively. Add a note below any changed cell explaining the basis for the change.

| Signal | Dalio | Dimon | Buffett | Blanchard | Marks |
|---|---|---|---|---|---|
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

Add `*Last updated: [TODAY'S DATE]*` below the table.

Legend: ✓ = recommends / warns in alignment with this signal, ⚠ = warns against or diverges, — = not a primary view

After the table, identify the highest-confidence signals (4+ framework agreement) and note any that have changed since the last refresh.

---

### SECTION 19 — CURRENT EVENTS WATCH LIST (dynamic — update based on research)

Output under heading `## CURRENT EVENTS WATCH LIST` with note `*Items to monitor and update in the next criteria refresh*`
*Format for each item: Item description — Monitor category — Action trigger*

Review the prior Watch List. For items that have resolved, replace them with new items. For items still pending, update their status. For new items surfaced by your research, add them.

Maintain 15–20 items covering all of the following monitor categories where currently relevant:

- **Criteria refresh** — triggers a full monthly CRITERIA.md update
- **Immediate watch** — triggers an out-of-cycle criteria update if the event occurs
- **Regulatory watch** — tracks legislation and regulatory developments affecting private credit, crypto, stablecoins, or fund structures

Include items across: Fed meetings and data releases, Fed personnel, Berkshire/Abel developments, tariff and trade litigation, geopolitical conflicts, private credit stress, fiscal legislation, election positioning, China macro, Japan BOJ and fiscal, Europe defense spending, CRE refinancing, entitlement reports, hurricane season, de-dollarization and stablecoin developments.

---

### SECTION 20 — SCORING THRESHOLDS (static, copy exactly from prior version)

Copy this section verbatim, including all five tier definitions, scoring weights, and all three score caps (critical red flag cap at 50%, horizon mismatch cap at 60%, single-holding concentration above 25% cap at 70%).

---

### SECTION 21 — AI DEEP ANALYSIS PROMPT (static, copy exactly from prior version)

Copy this section verbatim. This is the embedded quick-use prompt for users who do not have the standalone PORTFOLIO_ANALYSIS_PROMPT.md file. It must cover all eleven steps.

---

### SECTION 22 — FILE FOOTER (static)

End the file with exactly:

```
*End of Portfolio Alignment Criteria File. Generated [TODAY'S DATE].*
```

---

## OUTPUT REQUIREMENTS

- Output the entire CRITERIA.md file as one continuous markdown document
- Do not include any preamble, explanation, or commentary before or after the file
- Do not summarize what you did — just output the file
- Start the output with `# Portfolio Alignment Criteria File`
- End the output with the footer line above
- Every section listed above must be present and complete
- If you cannot find recent information for a dynamic subsection, say so explicitly — do not fabricate or use stale data
- Include confidence levels (High / Medium / Low) for each dynamic section
- Only change Consensus Signal table cells when research provides clear evidence — note the basis for any change
- Add a row to the Change Log describing what changed in this refresh
- Update the Watch List with resolved items removed, pending items updated, and new items added

---

*End of Criteria File Update Prompt.*
