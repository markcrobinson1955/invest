Criteria File Update Prompt
Paste this entire prompt into Claude.ai or ChatGPT (with web search enabled) to generate a complete replacement CRITERIA.md file.

ROLE AND TASK
You are updating a portfolio analysis criteria file that feeds a rules-based investment analyzer tool. The analyzer compares user portfolios against five frameworks: Ray Dalio, Jamie Dimon, Warren Buffett, Olivier Blanchard, and Howard Marks.
Search the web for current information and generate a complete replacement CRITERIA.md file — not just the updated sections. The file must include every section listed below. Do not omit any section.
The static sections (framework philosophy, target allocations, correlation assumptions, time horizon specification, liquidity tiering, currency exposure methodology, drawdown scenario models, rebalancing framework, position sizing floor, tax treatment overlay, scoring thresholds, macro verification requirements, fixed income classification dimensions, sector and factor exposure check, edge-case handling) should be carried forward accurately from the prior version. Only the dynamic sections require fresh research.
Output the entire file as a single continuous markdown document, ready to save and use immediately. Do not include any preamble, explanation, or commentary before or after the file. Start the output with: # Portfolio Alignment Criteria File. End with: *End of Portfolio Alignment Criteria File. Generated [TODAY'S DATE].*

VERSION-INCREMENT RULE
Use the pattern YYYY-MM-DD + lowercase letter suffix starting at a. If the prior version was 2026-04-18e and today is a later date, the new version becomes [TODAY'S DATE]a. If a same-day revision is required, increment the letter: 2026-04-20a → 2026-04-20b. Never reuse a prior version string.

BEFORE YOU BEGIN — REVIEW THE PRIOR WATCH LIST
Before searching for new information, review the Watch List from the prior CRITERIA.md. For each item:
Resolved → briefly state outcome and whether it changed framework scoring
Pending → carry it forward with updated status
Escalated → flag as priority update for the relevant macro subsection
This review informs which macro subsections require the most urgent updates.

PRESERVATION OF PRIOR AUDIT CORRECTIONS
The following corrections introduced in prior audit passes must be preserved verbatim in every refresh. If any are missing from the prior version you are working from, restore them.
From version 2026-04-18d (hallucination audit):
Disclaimer blocks in Drawdown Scenario Models noting wide error bands on historical return ranges
Editorial-rule labels on the 25% concentration cap, 2% position sizing floor, and ±5% rebalancing band identifying them as system-defined rules, not framework-sourced
Last-verified date flags on specific AUM and net worth figures (Dalio ~$14B personal, Bridgewater ~$150B AUM, Oaktree ~$200B AUM, JPMorgan ~$4.3T assets)
Edge-case caveat on gold ETF tax treatment (28% collectibles rate for grantor-trust structures like GLD)
PHYS/QEF election caveat for Sprott physical gold trust under US taxation
Softening of "required reading" language in Marks and Buffett sections
Clarifying note on commodity currency classification rule
From version 2026-04-20a (audit remediation):
System-constructed translation labels on Dalio, Dimon, and Buffett target allocations
System-constructed translation label on the Blanchard target allocation (Blanchard is not a published portfolio allocator)
System-defined editorial rule labels on per-framework liquidity tier thresholds
Fabrication-risk tags [verify] on specific sourced statistics
Severity gradient on red flags (minor / moderate / critical)
Score cap interaction rule (lowest applicable cap wins)
Regime-weighting operationalization (2x weight on regime-aligned frameworks in summary view)
Graduated horizon mismatch caps (75% / 65% / 55% instead of binary 60%)
Buffett thresholds added to CRITERIA.md directly: gold above 5% flag, over-20-holdings flag
Do not strip these. If the updating AI cannot determine whether a correction is present, err on the side of restoring it.

UNVERIFIED-DATA FALLBACK RULE
If you cannot verify a statistic within the refresh cycle, state explicitly: [prior figure carried forward, last verified YYYY-MM-DD]. Do not fabricate. Do not silently update a number. Do not drop a number that was present in the prior version without replacement — either re-verify or flag as carried forward.
Apply this rule especially to AUM and net worth figures, specific sell-side research targets (bank price targets, macro forecasts), specific dated market statistics (auction take-up rates, fund flow numbers), and any statistic tagged [verify] in the Macro Verification Requirements section.

INSTRUCTIONS BY SECTION
SECTION 1 — FILE HEADER (static, update dates only)
Output exactly:
# Portfolio Alignment Criteria File

*Version: [TODAY'S DATE][letter suffix per version-increment rule]*

*Last full refresh: [TODAY'S DATE]*

*Next scheduled refresh: [DATE 30 DAYS FROM TODAY]*
Staleness threshold across the entire system is 30 days. Do not use any other threshold.
SECTION 2 — CHANGE LOG (update with new row)
Carry forward all prior rows. Add one new row:
| [TODAY'S DATE] | [VERSION] | [Specific description of what changed in this refresh, including which macro subsections were materially updated and any framework thinker position changes] |
SECTION 3 — HOW TO UPDATE THIS FILE (static, copy verbatim from prior version)
Copy verbatim.
SECTION 4 — CURRENT MACRO ENVIRONMENT (dynamic — search and update all subsections)
Search for current news (within the last 30 days) on each subsection. Date each data point. Below each subsection heading add *Last updated: [TODAY'S DATE]* and *Confidence: [High/Medium/Low]*. If recent information is unavailable for a subsection, say so explicitly — do not fabricate.
Output under heading ## CURRENT MACRO ENVIRONMENT with the following subheadings:
US Fiscal Position — Search: US national debt current level, FY deficit projection, CBO baseline, interest payments on debt, Treasury auction demand, debt-to-GDP trajectory, primary dealer take-up on recent auctions.
Trade and Geopolitics — Search: current US tariff status (IEEPA ruling aftermath, Section 122, Section 301 investigations), active trade negotiations, geopolitical conflicts (Middle East, Ukraine, China-Taiwan), sanctions developments.
Private Credit Stress — Search: private credit fund redemption requests, fund gates or suspensions, default rates in direct lending, software/SaaS loan stress, regulatory attention, comparisons to prior credit cycles.
Regulatory Watch — Search: regulatory developments affecting private credit (Congressional hearings, SEC/Treasury actions), stablecoin legislation progress, crypto regulatory actions from SEC or CFTC, new rules affecting fund liquidity or redemption structures. Flag any development that materially changes how holdings in these categories should be scored.
AI Capital Expenditure — Search: hyperscaler capex announcements for current year (Amazon, Alphabet, Meta, Microsoft, Oracle), AI infrastructure spending projections, capex-to-revenue ratios, debt issuance to fund AI buildout, AI revenue versus investment gap, bubble risk assessments.
Inflation Trajectory — Search: most recent CPI release, core CPI, PCE, Fed SEP inflation projections, inflation drivers (energy, shelter, tariffs), Fed communications on inflation path.
Labor Market — Search: most recent unemployment rate, FOMC SEP unemployment projections, Fed dual-mandate tension, recent payrolls data, labor market fragility signals.
Market Performance YTD — Search: S&P 500 current level and YTD return, Dow, Nasdaq, Russell 2000, VIX, major international indices (DAX, FTSE, Nikkei, Hang Seng), factor performance (value vs. growth, low-vol vs. high-vol), emerging markets performance.
Dollar and Reserve Currency — Search: DXY current level and trend, gold price current level and YTD return, central bank gold purchases, foreign holdings of US Treasuries (TIC data), dollar share of global FX reserves, gold price forecasts from major banks.
De-Dollarization Mechanics — Search: mBridge CBDC platform developments and new members, CIPS volume, BRICS+ bilateral currency settlements, sanctions architecture developments, alternative reserve currency progress.
China and Emerging Markets — Search: China GDP growth most recent quarter, China property sector developments, Chinese consumer and deflation risk, China energy exposure to Middle East, MSCI EM performance, India/Vietnam supply chain developments.
Europe and Japan — Search: Germany fiscal expansion and debt brake status, EU defense spending trajectory, European equity performance vs. US, BOJ policy normalization, yen direction, Japan fiscal framework changes, carry trade unwind risk.
Housing and Commercial Real Estate — Search: US shelter inflation current rate, residential transaction volumes, commercial real estate refinancing stress, office CRE conditions, regional bank CRE exposure, data center and industrial CRE performance.
Cryptocurrency and Digital Assets — Search: Bitcoin price and institutional adoption developments, spot ETF flows, stablecoin market cap and Treasury bill demand, regulatory developments.
Demographics and Entitlement Trajectory — Search: Social Security and Medicare trust fund projections, mandatory spending trajectory, CBO long-term fiscal projections, entitlement reform prospects.
Climate and Physical Risk — Search: insurance market repricing in climate-exposed regions, insurer withdrawals from high-risk markets, agricultural commodity volatility from weather, infrastructure resilience spending.
Earnings Yield vs Credit Yield Snapshot — Search: S&P 500 forward earnings yield (current), US investment-grade corporate yield (current), US high-yield corporate yield (current), spread between them. This subsection supports the Marks framework analysis directly — do not omit. State the earnings-yield-minus-IG-yield spread and flag whether credit or equity currently offers the higher yield. Tag any specific yield figure with [verify] if sourced from sell-side research rather than index provider data.
SECTION 5 — CORRELATION ASSUMPTIONS (partially dynamic)
Copy static framework descriptions verbatim. Update only the Current regime assessment line at the bottom based on your macro research. State: current regime, primary risk scenario regime, which two frameworks are best suited to current conditions, and which framework is least suited. Preserve the regime-weighting operationalization note (2x weight on regime-aligned frameworks in summary view).
SECTION 6 — TIME HORIZON SPECIFICATION (static, copy verbatim)
Copy verbatim including the graduated horizon cap rule (75% / 65% / 55%).
SECTION 7 — LIQUIDITY TIERING (static, copy verbatim)
Copy verbatim including tier definitions table, all five framework liquidity thresholds, the system-defined editorial rule labels on those thresholds, and the Post-Gate Stress Tier Reassessment subsection (Tier 3 holdings reclassify to effective Tier 5 under 2008 analog stress).
SECTION 8 — CURRENCY EXPOSURE METHODOLOGY (static, copy verbatim)
Copy verbatim including all classification rules, dollar concentration thresholds, and the Non-USD Base Currency Handling subsection.
SECTION 9 — DRAWDOWN SCENARIO MODELS (static, copy verbatim with relevance updates)
Copy all three scenarios verbatim including the wide-error-band disclaimer block. Update only the Relevance to [current year] line for each scenario based on macro research — specifically whether relevance has increased, decreased, or stayed the same since the last refresh.
SECTION 10 — REBALANCING FRAMEWORK (static, copy verbatim)
Copy verbatim.
SECTION 11 — POSITION SIZING FLOOR (static, copy verbatim)
Copy verbatim including the system-defined editorial rule label on the 2% floor.
SECTION 12 — TAX TREATMENT OVERLAY (static, copy verbatim)
Copy verbatim including account type definitions, optimal asset location rules table, tax mislocation flag instructions, the collectibles-rate caveat for GLD, the PHYS/QEF election caveat, and the note on international users.
SECTION 13 — MACRO VERIFICATION REQUIREMENTS (static structure, dynamic contents)
Copy the section structure verbatim. The specific enumerated items must be updated each refresh: as new unverified statistics are introduced into the macro environment, add them to the verification list with [verify] tags. As items are verified or removed, update the list accordingly. The list should enumerate every specific sourced statistic in the macro environment that carries fabrication risk, including:
Specific sell-side research targets (bank price targets, forecast numbers)
Specific dated market statistics (auction take-up, fund flow numbers)
Named executive compensation figures
Specific fund AUM and gate-status claims
Any narrative about specific geopolitical events within the last 12 months
SECTION 14 — FIXED INCOME CLASSIFICATION DIMENSIONS (static, copy verbatim)
Copy verbatim including duration tiers (ultra-short through very long) and credit quality tiers (Treasury/sovereign IG through unrated/private).
SECTION 15 — SECTOR AND FACTOR EXPOSURE CHECK (static, copy verbatim)
Copy verbatim including sector concentration flags (tech+comm >40%, financials >30%, REITs >15%, energy >20%), factor tilt identification, and framework-specific sector/factor preferences.
SECTION 16 — EDGE-CASE HANDLING (static, copy verbatim)
Copy verbatim covering leveraged ETFs, options positions, margin/negative cash, extreme concentration (50%+, 70%+), all-cash portfolios, foreign-currency base, cryptocurrency beyond Bitcoin, direct real estate, private business ownership, and pension/annuity/Social Security as bond-equivalent.
SECTION 17 — FRAMEWORK 1: RAY DALIO (partially dynamic)
Static subsections — copy accurately: Who He Is; Investment Philosophy; Target Allocation (All Weather) — 15/15/20/20/10/10/10 with system-constructed translation label; Red Flags (with severity gradient); Green Flags.
Preserve last-verified date flag on Bridgewater ~$150B AUM and Dalio ~$14B personal net worth figures. Re-verify during this refresh; if not verifiable, apply the unverified-data fallback rule.
Dynamic subsections — search and update:
Current Thesis (current year) — Search for Dalio's most recent public statements (LinkedIn, X, Bridgewater research, interviews, conferences) in the last 60 days. Summarize in 3–5 sentences with source and date. Flag prominently if his stated position has changed materially from the prior version — if so, note that the static philosophy sections may need manual review.
Recent Commentary — 2–3 sentences on most recent specific warnings or recommendations with source and date.
Add *Source: [sources used]* and *Confidence: [High/Medium/Low]* below the heading.
SECTION 18 — FRAMEWORK 2: JAMIE DIMON (partially dynamic)
Static subsections — copy accurately: Who He Is; Investment Philosophy; Target Allocation (Fortress Balance Sheet) with system-constructed translation label; Red Flags (with severity gradient); Green Flags.
Preserve last-verified date flag on JPMorgan ~$4.3T assets. Re-verify during this refresh.
Dynamic subsections — search and update:
Current Thesis (current year) — Search Dimon statements, JPMorgan earnings calls, CNBC/Bloomberg interviews, annual shareholder letter (typically April release). Summarize in 3–5 sentences.
JPMorgan Credit Book as Leading Indicator — Search most recent earnings call commentary on consumer credit (card charge-offs, delinquencies), auto loan stress, commercial real estate reserve builds. Summarize in 3–4 sentences. This subsection operationalizes the credit book as a macro signal — do not omit.
Recent Commentary — 2–3 sentences on most recent warnings with source and date.
Add *Source: [sources used]* and *Confidence: [High/Medium/Low]*.
SECTION 19 — FRAMEWORK 3: WARREN BUFFETT (partially dynamic)
Static subsections — copy accurately: Who He Is; Investment Philosophy; Target Allocation (Berkshire Model) with system-constructed translation label; Red Flags (with severity gradient, including gold-above-5% flag and over-20-holdings flag); Green Flags.
Dynamic subsections — search and update:
Current Thesis (current year) — Buffett vs. Abel Divergence — Search Berkshire 13F filings, Greg Abel commentary, Buffett public statements, Berkshire cash position updates, significant purchases or sales. Note explicitly where Abel's approach diverges from Buffett's historical pattern. Summarize in 3–5 sentences. Preserve any last-verified date flag on Abel compensation figures.
Recent Commentary — 2–3 sentences with source and date.
Add *Source: [sources used]* and *Confidence: [High/Medium/Low]*.
SECTION 20 — FRAMEWORK 4: OLIVIER BLANCHARD (partially dynamic)
Static subsections — copy accurately: Who He Is; Investment Philosophy; Target Allocation (Fiscal Stress Resilience) with prominent system-constructed translation label (Blanchard is an academic economist, not a published portfolio allocator — this label is critical); Red Flags (with severity gradient); Green Flags.
Dynamic subsections — search and update:
Current Thesis (current year) — Search Blanchard publications, Peterson Institute papers, IMF commentary, media appearances in last 90 days. Summarize in 3–5 sentences.
Recent Commentary — 2–3 sentences with source and date.
Add *Source: [sources used]* and *Confidence: [High/Medium/Low]*.
SECTION 21 — FRAMEWORK 5: HOWARD MARKS (partially dynamic)
Static subsections — copy accurately: Who He Is; Investment Philosophy; Target Allocation Bias (Cycle-Aware Credit) — retain the deliberate avoidance of specific numbers; Red Flags (with severity gradient); Green Flags.
Preserve last-verified date flag on Oaktree ~$200B AUM. Re-verify during this refresh.
Dynamic subsections — search and update:
Current Thesis (current year) — Search Oaktree memos, Marks interviews, Bloomberg/CNBC appearances in last 90 days. Summarize current cycle-stage assessment and credit-vs-equity view in 3–5 sentences.
Recent Commentary — 2–3 sentences with source and date.
Add *Source: [sources used]* and *Confidence: [High/Medium/Low]*.
SECTION 22 — CONSENSUS SIGNALS (dynamic — update based on research)
Output under heading ## CONSENSUS SIGNALS with note *Where multiple frameworks agree, confidence is highest*.
Carry forward the existing 14-row table. Update a cell only where research provides clear evidence of a framework position change. Add a note below any changed cell explaining the basis. Add *Last updated: [TODAY'S DATE]* below the table.
After the table, identify the highest-confidence signals (4+ framework agreement) and note any that have changed since the last refresh.
SECTION 23 — CURRENT EVENTS WATCH LIST (dynamic)
Output under heading ## CURRENT EVENTS WATCH LIST with note *Items to monitor and update in the next criteria refresh*. Format: Item description — Monitor category — Action trigger.
Review prior Watch List. Replace resolved items. Update pending items. Add new items from research.
Maintain 15–20 items covering: Fed meetings and data releases, Fed personnel, Berkshire/Abel developments, tariff and trade litigation, geopolitical conflicts, private credit stress, fiscal legislation, election positioning, China macro, Japan BOJ and fiscal, Europe defense spending, CRE refinancing, entitlement reports, hurricane season, de-dollarization and stablecoin developments.
Monitor categories:
Criteria refresh — triggers a full monthly CRITERIA.md update
Immediate watch — triggers an out-of-cycle criteria update if the event occurs
Regulatory watch — tracks legislation and regulatory developments affecting private credit, crypto, stablecoins, or fund structures
SECTION 24 — SCORING THRESHOLDS (static, copy verbatim)
Copy verbatim including all five tier definitions, scoring weights, the three score caps (critical red flag cap at 50%, horizon mismatch graduated caps at 75%/65%/55%, single-holding concentration above 25% cap at 70%), the score cap interaction rule (lowest applicable cap wins), the severity-graded red flag deductions (minor -2, moderate -5, critical -10), and the optional confidence range capability.
SECTION 25 — FILE FOOTER
End with exactly: *End of Portfolio Alignment Criteria File. Generated [TODAY'S DATE].*

OUTPUT REQUIREMENTS
One continuous markdown document, no preamble, no post-commentary
Start with # Portfolio Alignment Criteria File
End with the footer line
Every section listed above must be present and complete
If you cannot find recent information for a dynamic subsection, say so explicitly
Include confidence levels (High/Medium/Low) for each dynamic section
Only change Consensus Signal table cells when research provides clear evidence
Add a Change Log row describing what changed in this refresh
Update the Watch List with resolved items removed, pending items updated, new items added
Apply the unverified-data fallback rule to any statistic you cannot re-verify
Apply the version-increment rule to the version string
Preserve all prior audit corrections enumerated above
End of Criteria File Update Prompt.


