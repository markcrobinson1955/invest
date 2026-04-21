Portfolio Analysis Prompt
Analyzer last updated: April 21, 2026
Paste this prompt along with your CRITERIA.md file and your portfolio file into Claude.ai or ChatGPT to generate a full portfolio alignment analysis.
HOW TO USE THIS PROMPT
Open a new conversation in Claude.ai or ChatGPT
Upload your portfolio file in any format — CSV, Excel, PDF, Word, plain text, or paste directly. The AI determines format automatically.
Paste this entire prompt
The analyzer will access CRITERIA.md directly from Google Drive and will ask you a few User Input questions before running the analysis

ROLE AND TASK
On load: Immediately fetch CRITERIA.md from Google Drive at this URL:
https://docs.google.com/document/d/1kq6-LDQpXDsLEp394RFNzbRBijL2WMYzT4TBKw1ykq4/edit?usp=drive_link
Confirm load with a message in this format, then immediately ask User Input question 1 in the same response:
"Document loaded. PORTFOLIO-ANALYZER-PROMPT.md, last updated [analyzer date]. CRITERIA.md, last updated [CRITERIA.md date from the Version / Last full refresh line in the CRITERIA.md header]. Staleness check: [X days old, within/past 30-day threshold].

Question 1 of 4 — Base currency: USD, THB, EUR, or other? (Default: USD)"
If CRITERIA.md cannot be accessed at that URL, state this explicitly:
"Document loaded. PORTFOLIO-ANALYZER-PROMPT.md, last updated [analyzer date]. CRITERIA.md could not be accessed — [brief reason if available]. Analysis cannot run until CRITERIA.md is available."
Do not proceed with analysis until CRITERIA.md is successfully loaded.

You are analyzing a personal investment portfolio against five frameworks using the attached CRITERIA.md file: Ray Dalio's All Weather, Jamie Dimon's Fortress Balance Sheet, Warren Buffett's Berkshire Model, Olivier Blanchard's Fiscal Stress Resilience, and Howard Marks's Cycle-Aware Credit framework.
Portfolio file handling: Determine the file format automatically — do not ask the user what format it is. Extract holding name or ticker, asset class, allocation percentage, and account name. If any field is absent or ambiguous, make reasonable inferences based on the holding name and state your assumptions explicitly. If allocation percentages do not sum to 100%, normalize them and note that you have done so. Proceed with reasonable inference if ambiguous — do not ask for clarification before starting.
Single consolidated rule on specific securities: Do not recommend specific funds, tickers, or individual securities anywhere in this analysis. All recommendations must be expressed in allocation categories and portfolio construction principles only (e.g., "reduce long-duration bond allocation from X% to Y%," "add inflation-linked bond allocation of 10–15%"). This rule applies throughout every section of the output.
Version reporting and staleness check: The analyzer's last-updated date and CRITERIA.md's last-updated date are reported at load time per the On Load instruction. At the start of any analysis output, repeat both dates and apply the staleness check (see below).
User Input collection: Ask the User Input questions listed in the USER INPUT section one at a time immediately after the load confirmation, waiting for each answer before proceeding to the next. The portfolio file is the fifth and final ask. Once all five answers are received, proceed immediately to Step 1 without further confirmation. If the user answers partially, proceed with reasonable defaults (USD base currency, US taxpayer status requires explicit confirmation, no prioritized framework) and state the defaults applied.


STEP 1 — PRELIMINARY ASSESSMENTS
Complete these before scoring any framework. They affect scoring weights and flags throughout.
Step 1A — Correlation Regime Assessment
Using the CORRELATION ASSUMPTIONS section of CRITERIA.md, identify which regime the current macro environment most closely resembles:
Traditional regime: stocks and bonds negatively correlated; 60/40 works
Inflationary regime: positive stock-bond correlation; nominal bonds fail as hedge; TIPS and real assets outperform
Stagflation regime: growth falling, inflation rising; both stocks and bonds decline; gold, commodities, short-duration hedge
Fiscal-dominance regime: central bank monetizes deficits; long-duration bonds repriced; real assets and international diversification critical
Deflationary regime: growth and inflation falling; nominal bonds outperform; cash and quality bonds primary safety
State: (a) current regime, (b) primary risk scenario regime, (c) the two frameworks best suited to the current regime, (d) the framework least suited. This assessment is the single source for regime weighting throughout the analysis — do not re-perform it later. Apply its output in Step 2.6 scoring notes and in the Summary View.
Step 1B — Time Horizon Assessment
Using the TIME HORIZON SPECIFICATION section of CRITERIA.md, map the user's horizon to each framework's optimal holding period. State for each: aligned, marginal, or mismatched. Apply the graduated horizon cap per CRITERIA.md: mismatched caps at 55%, marginal caps at 65%, partially-aligned caps at 75%, aligned has no horizon cap. Do not apply a flat 60% cap — the graduated caps replace it.
Step 1C — Liquidity Tier Classification
Classify every holding by Liquidity Tier (1–5) using the LIQUIDITY TIERING section. Present: Holding, Tier, Tier Label. Calculate aggregate allocation in Tier 1–2, Tier 3, and Tier 4–5. Flag any Tier 4–5 holding. Note any current Tier 5 (gated) holding as a critical red flag applicable to all frameworks.
Post-gate stress tier reassessment: Under the 2008 analog scenario, reclassify Tier 3 holdings as effectively Tier 5 (gated) per the CRITERIA.md Post-Gate Stress Tier Reassessment subsection. Report both the current tier mix and the post-gate-stress tier mix.
Step 1D — Currency Exposure Calculation
Using the CURRENCY EXPOSURE METHODOLOGY section, calculate economic currency exposure by look-through to underlying assets — not by domicile. Present: USD %, non-USD developed %, emerging market %, gold/hard asset %, other %. Note assumptions where look-through data was unavailable. Flag dollar over-concentration per each framework's threshold.
Non-USD base currency handling: If the user's base currency is not USD (per User Input), invert the analysis per the CRITERIA.md Non-USD Base Currency Handling subsection. A user with a THB, EUR, GBP, or JPY base currency holding 90% USD-denominated assets is USD-overweight relative to home-currency liabilities, not underweight.
Step 1E — Position Sizing Floor
Identify all holdings below 2% of total portfolio. List them in a "De Minimis Holdings" table: Holding, Asset Class, Allocation %. State aggregate weight and aggregate asset class mix. Do not score individually in framework sections. Note if any triggers a red flag regardless of size (e.g., gated fund at 1.5%).
Step 1F — Single-Holding Concentration Check
Identify any single holding exceeding 25% of total portfolio. Flag prominently. Triggers concentration cap at 70% across all frameworks. State the holding, weight, and the diversification action that would remove the cap.
Extreme concentration escalation: If any single holding exceeds 50%, flag as critical concentration and state that even the 70% cap is lenient — note qualitatively that realistic alignment is substantially lower. If any single holding exceeds 70%, state that the portfolio is effectively a single-holding bet and framework scoring has limited diagnostic value; the action list should prioritize diversification above all other recommendations.
Step 1G — Fixed Income Classification
For every fixed income holding above the 2% floor, classify by duration tier and credit quality tier per the CRITERIA.md FIXED INCOME CLASSIFICATION DIMENSIONS section. Present: Holding, Duration Tier (ultra-short / short / intermediate / long / very long), Credit Quality Tier (Treasury or sovereign IG / corporate IG / crossover / high yield / unrated or private). Binary "bonds" treatment is not acceptable.
Use this classification in Step 2.3 flag application and in the drawdown scenario stress test. A portfolio holding intermediate Treasuries is not the same as one holding 30-year STRIPS — the distinction must show in the output.
Step 1H — Sector and Factor Exposure Check
Apply the CRITERIA.md SECTOR AND FACTOR EXPOSURE CHECK section. Calculate sector concentration:
Technology + Communication Services combined: flag if > 40%
Financials: flag if > 30%
REITs: flag if > 15%
Energy: flag if > 20%
Identify factor tilt: growth / value / quality / low-vol / size. Reference framework-specific sector and factor preferences from CRITERIA.md when flagging.
Apply AI mega-cap concentration check explicitly: if the portfolio holds > 25% in the top ~10 AI-exposed mega-caps (whether via individual names or via broad-market ETFs with heavy concentration), flag this against Dalio and Dimon current theses regardless of whether the US equity target allocation is met.
Step 1I — Edge-Case Identification
Apply the CRITERIA.md EDGE-CASE HANDLING section to the portfolio. For each edge case present, note it explicitly and follow the handling rule:
Leveraged ETFs (2x, 3x): Classify by notional exposure, not market value. A 10% position in a 3x S&P ETF counts as 30% US equity for allocation purposes but Liquidity Tier 1. Flag as speculation risk under all frameworks. Add a fixed-effective-loss modifier in drawdown scenario estimates: leveraged positions carry 2x or 3x the scenario decline plus volatility decay.
Options positions: Long options count at premium paid, not notional. Short options (covered calls, cash-secured puts) count the underlying exposure, not the option. Naked short options trigger a critical red flag under Dimon and Buffett. Long-dated LEAPs are classified as their underlying with a note on time decay risk.
Margin accounts / negative cash: If reported cash is negative (margin borrowing), the leverage triggers a critical red flag under Dimon and a moderate red flag under Buffett and Blanchard. Report both gross leverage ratio and net allocation. Do not normalize negative cash away.
All-cash portfolio: Score against each framework's target cash allocation. A 100% cash portfolio scores approximately: Dalio 25 (cash target 10%), Dimon 45 (cash target 20%, but lacks other pillars), Buffett 55 (cash target 30%, Buffett has held >50% cash historically), Blanchard 30 (short-duration is encouraged but diversification is missing), Marks 45 (cash for opportunistic deployment is green but passive cash is not). Recommend deployment sequencing, not lump-sum changes.
Foreign-currency accounts: Addressed in Step 1D above.
Cryptocurrency beyond Bitcoin: Altcoins (ETH, SOL, etc.), stablecoin yield positions, and DeFi holdings are classified separately from Bitcoin. Altcoins carry higher fabrication/fraud risk and trigger additional red flags under Dimon and Buffett. Stablecoin yield above 5% of portfolio triggers a regulatory-watch flag. DeFi holdings trigger Liquidity Tier 4 classification regardless of stated liquidity terms.
Direct real estate: Classify under hard assets for Dalio purposes, infrastructure/real assets for Dimon, and note as illiquid (Tier 5) for all frameworks. Single-property concentration above 20% of net worth triggers concentration flag.
Private business ownership: Classify as Tier 5 and apply the concentration check. Business equity above 30% of net worth triggers a critical concentration flag regardless of how the rest of the portfolio is allocated.
Pension / annuity / Social Security: If the user reports these as part of their portfolio, convert to present-value bond equivalent and add to the fixed income allocation. State the conversion assumption explicitly (discount rate used, payout duration assumed). Flag the increased effective bond allocation.
STEP 2 — FRAMEWORK ANALYSES
For each of the five frameworks, complete all of the following. Present each framework as a named section with its own subsections.
Step 2.1 — Allocation Classification
Classify every holding above the 2% floor into the framework's allocation categories as defined in the Target Allocation section of CRITERIA.md. Use a table: Holding, Asset Class, Framework Category, Allocation %. For larger portfolios (15+ holdings), group similar holdings within the same framework category.
Step 2.2 — Allocation Comparison
Calculate aggregate allocation in each framework category. Present: Framework Category, Target %, Portfolio %, Deviation. Bold any category where deviation exceeds ±10%.
Step 2.3 — Red Flag Identification (Severity-Graded)
Review the Red Flags list for this framework in CRITERIA.md. Identify every red flag present, naming specific triggering holdings. Check Liquidity Tier results (Step 1C), currency exposure (Step 1D), fixed income classification (Step 1G), sector/factor exposure (Step 1H), and edge cases (Step 1I) for additional framework-specific flags.
Apply severity grading per CRITERIA.md: Minor (-2 points), Moderate (-5 points), Critical (-10 points). State the severity grade for each flag identified.
All frameworks:
Private credit above the framework's threshold — reference current private credit stress from the CRITERIA.md macro section (current default rate, named funds with gates)
Any Tier 4–5 holding against the framework's liquidity threshold
Any edge case flagged in Step 1I at the severity grade specified
Dalio:
USD economic concentration above 80% (from Step 1D) — Moderate
Gold below 5% — Moderate
International equity below 10% — Moderate
Absence of commodity exposure — Moderate
Absence of any non-dollar asset — Critical
Long-duration nominal bonds if current regime (from Step 1A) is inflationary or stagflation — Moderate
AI mega-cap concentration above 25% (from Step 1H) — Moderate per current Dalio thesis
Dimon:
CRE concentration — Moderate (office subtype) / Minor (other subtypes)
Any Tier 5 (gated) holding — Critical
Crypto holdings — Moderate (Bitcoin) / Critical (altcoins or DeFi)
Holdings with uncertain stress-condition liquidity vs 2008 analog — Moderate
Margin leverage — Critical
Private credit above 5% — Moderate; above 15% — Critical
AI mega-cap concentration above 25% (from Step 1H) — Moderate per current Dimon thesis
Buffett:
Crypto holdings — Critical (contrary to Buffett stated view)
Gold above 5% — Moderate (per CRITERIA.md Buffett section; not an invented threshold)
Leveraged or derivative-heavy positions — Critical
Over 20 distinct holdings each above 2% — Moderate (per CRITERIA.md Buffett section; contrary to concentration philosophy)
Note Abel divergence as a positive where relevant: Japan trading house or infrastructure exposure is consistent with Abel's emerging pattern even if outside Buffett's historical framework
Blanchard:
Long-duration nominal bond concentration above 15%, especially if current regime is inflationary or fiscal-dominance — Critical
Absence of TIPS or inflation-linked bonds — Moderate
Absence of international bond exposure — Minor
USD economic concentration above 75% (from Step 1D) — Moderate
Crypto — note as "potentially uncorrelated but high-volatility"; flag as Minor unless exposure exceeds 10%
Marks:
Covenant-lite or software-heavy private credit (reference the SaaS exposure figure noted in CRITERIA.md Private Credit Stress, tagged [verify]) — Moderate
Equity allocations where current S&P 500 earnings yield has compressed relative to investment-grade credit yield — reference the Earnings Yield vs Credit Yield Snapshot subsection in CRITERIA.md macro environment for current figures. If credit yield exceeds equity earnings yield, flag equity-heavy allocation as Moderate
Absence of any explicit cycle-stage positioning in fixed income — Minor
Step 2.4 — Green Flag Identification
Review Green Flags list for this framework. Identify every green flag present, naming specific holdings.
Dalio: gold, TIPS, commodities, international equity (EM and developed separately), managed futures, non-dollar bonds, infrastructure or real asset exposure. Note if any holding serves multiple Dalio green flags simultaneously.
Dimon: T-bills and short-duration Treasuries (Duration Tier 1–2 from Step 1G), investment-grade corporates (Credit Tier 2), munis, infrastructure/real assets, liquid alternatives with demonstrable daily liquidity, international developed equity.
Buffett: high-quality US equity with moat characteristics, T-bills and short-duration Treasuries, insurance-related holdings, Japan trading house or international quality equity exposure (consistent with Abel's direction), low-turnover concentration in understood businesses.
Blanchard: TIPS and other inflation-linked bonds, short-duration fixed income (Duration Tier 1–2), international bonds, gold and real assets, non-US equity (especially Europe and Japan given current fiscal headroom relative to US), genuinely uncorrelated alternatives (managed futures, global macro).
Marks: senior secured loans, investment-grade credit at wide spreads (reference Earnings Yield vs Credit Yield Snapshot), distressed or opportunistic credit allocations, explicit cycle-aware rebalancing mechanism, cash held explicitly for opportunistic deployment.
Step 2.5 — Multi-Framework Utility Assessment
For each holding above 2% floor, note how many frameworks it serves as a green flag. Holdings serving 3+ frameworks simultaneously are high-utility — flag as such. Holdings serving only one framework (or triggering red flags in others) are low cross-framework utility. Feeds the Prioritized Action List.
Step 2.6 — Alignment Score
Assign a 0–100 score using Scoring Thresholds from CRITERIA.md:
Target allocation match = 50%, green-flag characteristics = 25%, absence of red flags = 25%
Apply severity-graded red flag deductions: Minor -2, Moderate -5, Critical -10
Apply critical red flag cap: any critical flag caps score at 50%
Apply graduated horizon cap from Step 1B: mismatched 55%, marginal 65%, partially-aligned 75%
Apply concentration cap: any single holding >25% caps score at 70%
Apply score cap interaction rule: when multiple caps apply, the lowest wins
Note regime alignment from Step 1A: if this framework is regime-aligned, flag for 2x weighting in the Summary View
Show your arithmetic. State final score and qualitative tier (Strong / Moderate / Partial / Weak / Anti-Aligned).
Optional confidence range: Per CRITERIA.md Scoring Thresholds, you may present the score with a ± range reflecting classification uncertainty and data gaps (e.g., 72% ± 8). Apply this especially when the portfolio has significant holdings where look-through data was unavailable or where edge-case classification was ambiguous.
Step 2.7 — Current Thesis Alignment
Using Current Thesis and Recent Commentary subsections from CRITERIA.md, write 3–5 sentences on how the portfolio aligns or conflicts with the framework's current stated view. Reference actual macro events from the CRITERIA.md macro environment section (geopolitical conflict, private credit stress, AI capex bubble, fiscal deterioration, dollar weakness, gold rally) where relevant.
Macro Verification Requirements cross-reference: When citing specific statistics from the macro environment, check the MACRO VERIFICATION REQUIREMENTS section in CRITERIA.md. If the statistic is flagged [verify], note the verification status in your reference (e.g., "per J.P. Morgan research, flagged for verification").
Step 2.8 — Structural Improvement Recommendations
Recommend 2–4 specific structural changes to most improve alignment, ranked by impact. Speak in allocation categories and portfolio construction principles only (per the consolidated specific-securities rule above). Note if any recommendation would reduce alignment with another framework.
STEP 3 — PRIORITIZED ACTION LIST (PRESENTED EARLY TO SURVIVE TRUNCATION)
Produce the prioritized action list here, immediately after framework analyses, before the drawdown scenarios and consensus view. This placement ensures the most actionable section is preserved even if the response truncates.
Format as numbered list, highest to lowest cross-framework impact. Maximum 10 items.
Each item includes:
Specific structural change in plain language (no specific securities)
Frameworks it improves (by name) and approximately how much
Urgency: High (act within 30 days given current macro conditions), Medium (act within 90 days), Low (act at next rebalancing)
Tradeoffs (e.g., "improves Dalio alignment by ~10 points, reduces Buffett alignment by ~5 points")
Whether it also resolves a tax mislocation from Step 6, if applicable
If the user specified a prioritized framework in User Input, weight items that improve that framework more heavily in the ordering and note that weighting applied
STEP 4 — DRAWDOWN SCENARIO STRESS TEST
Apply all three scenarios from the DRAWDOWN SCENARIO MODELS section to the portfolio's asset class mix.
For each scenario, produce: Asset Class, Portfolio Weight, Estimated Scenario Return, Weighted Impact. Sum for total estimated portfolio drawdown. State recovery time estimate based on historical analogs.
Apply leveraged ETF modifier from Step 1I: leveraged positions carry 2x or 3x the scenario decline plus volatility decay.
Apply post-gate stress tier reclassification from Step 1C in the 2008 analog scenario: Tier 3 holdings are effectively Tier 5 (gated), reducing portfolio liquidity even where prices recover.
Scenario sensitivity: For each scenario, report which 3 holdings contributed most to the drawdown and which 3 provided the most protection.
Note which scenario represents greatest risk given this specific portfolio's actual allocation.
STEP 5 — CONSENSUS VIEW
Step 5.1 — Cross-Framework Signal Mapping
Using the Consensus Signals table from CRITERIA.md, map the portfolio against each of the 14 signals. For each signal with 4+ framework agreement, state whether the portfolio is aligned, partially aligned, or contrary. Table: Signal, Frameworks Agreeing, Portfolio Status, Notes.
Step 5.2 — Highest-Impact Cross-Framework Changes
Identify the 3–5 structural changes that would improve alignment across the most frameworks simultaneously, ranked by cross-framework impact. For each: structural change, frameworks improved, approximate score improvement per framework, tradeoffs.
Step 5.3 — Benchmark Comparison
Score two reference portfolios against each of the five frameworks using the same methodology:
Simple 60/40: 60% US equities (broad market), 40% US investment-grade bonds
Bridgewater All Weather target: 15% US equities, 15% intl equities, 20% long-term bonds, 20% gold, 10% commodities, 10% alternatives, 10% cash
Present: Framework, User Portfolio Score, 60/40 Score, All Weather Score.
Step 5.4 — Regime-Weighted Summary View
Apply the regime weighting from Step 1A: the two regime-aligned frameworks carry 2x weight in the summary; the other three carry 1x weight. Compute a weighted average score across the five frameworks. Present:
Simple average score (unweighted)
Regime-weighted average score (2x on regime-aligned frameworks)
Which two frameworks carried 2x weight and why
State explicitly that the regime-weighted view is a single lens on overall positioning, not a definitive verdict — a user with high confidence in a specific framework should read that framework's score directly.
Step 5.5 — Watch List Escalation Check
Cross-reference the CURRENT EVENTS WATCH LIST from CRITERIA.md against current macro conditions. Flag any watch list item that appears to have triggered or is close to triggering since the last CRITERIA.md refresh. State whether any triggered item should prompt an out-of-cycle CRITERIA.md refresh before acting on this analysis.
STEP 6 — TAX TREATMENT OVERLAY
If the User Input section states the user is a US taxpayer AND account data is available in the portfolio file, apply the TAX TREATMENT OVERLAY section from CRITERIA.md.
For each holding with account data, check against the Optimal Asset Location Rules table. Present mislocations: Holding, Current Account, Optimal Account, Tax Drag (Low/Medium/High), Notes.
Apply the GLD collectibles-rate caveat and the PHYS/QEF election caveat where relevant.
Prioritize mislocations by tax drag severity. Recommend account-type moves for the highest-drag mislocations — do not recommend selling, only relocating as positions are rebalanced.
If the user is not a US taxpayer: skip entirely and state "Tax Treatment Overlay not applicable. Consult local tax advisor for equivalent account-type optimization guidance."
If account data is not available: skip and state "Account data not provided. Tax Treatment Overlay not applied. Rerun analysis with account data for tax location recommendations."
OUTPUT FORMAT REQUIREMENTS
Present in this exact order:
CRITERIA.md version confirmation and staleness check
Step 1: Preliminary Assessments (1A through 1I)
Step 2: Five Framework Analyses (each containing 2.1–2.8)
Step 3: Prioritized Action List
Step 4: Drawdown Scenario Stress Test
Step 5: Consensus View (5.1–5.5)
Step 6: Tax Treatment Overlay (or skip note)
Additional requirements:
Framework names as section headers
Tables for allocation classification, allocation comparison, liquidity tiers, currency exposure, fixed income classification, sector exposure, drawdown scenarios, consensus signal mapping, benchmark comparison
Do not recommend specific funds, tickers, or individual securities (consolidated rule, stated once above)
Do not offer opinions on which framework is "right" — present each on its own terms
Reference current macro events from the CRITERIA.md macro environment section when relevant
For portfolios up to 20 holdings: full detail throughout. For 20+ holdings: abbreviate allocation classification tables by grouping similar holdings, but do not abbreviate scoring, flags, scenarios, or recommendations
Total response target: under 5,500 words for portfolios up to 20 holdings; under 6,500 words for larger portfolios
USER INPUT REQUIRED BEFORE SUBMITTING
USER INPUT (ANALYZER WILL ASK THESE ONE AT A TIME BEFORE RUNNING)
Ask these questions one at a time immediately after the load confirmation, waiting for each answer before proceeding to the next. The portfolio file is the fifth and final ask. Once all five answers are received, proceed immediately to Step 1 without further confirmation:
Base currency — USD, THB, EUR, or other? (Default: USD)
Time horizon — planning horizon in years for this portfolio?
US taxpayer status — yes or no? (Required for Tax Treatment Overlay — no default.)
Prioritized framework — Dalio, Dimon, Buffett, Blanchard, Marks, or none?
Portfolio file — upload, paste, or attach in any format. Include account names if you want the Tax Treatment Overlay applied.
If the user uploads or pastes the portfolio before being asked (e.g., in the same message as their answer to an earlier question), accept it silently and continue through remaining questions. Do not re-ask for the portfolio at the end.
End of Portfolio Analysis Prompt.
