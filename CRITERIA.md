Portfolio Alignment Criteria File
Version: 2026-04-20a (audit remediation) Last full refresh: 2026-04-20 Next scheduled refresh: 2026-05-20

CHANGE LOG
Version
Date
Changes
2026-04-18a
2026-04-18
Initial expanded version. Added Frameworks 4–5, Consensus Signals table, macro environment.
2026-04-18b
2026-04-18
Added 9 new macro subsections, Correlation Assumptions, Time Horizon Specification, Watch List expanded to 20 items, Howard Marks framework.
2026-04-18c
2026-04-18
Added Change Log, Liquidity Tiering, Currency Exposure Methodology, Drawdown Scenario Models, Rebalancing Framework, Position Sizing Floor, Tax Treatment Overlay, Regulatory Watch. Updated Scoring Thresholds with concentration cap.
2026-04-18d
2026-04-18
Hallucination audit. Added disclaimer block to Drawdown Scenario Models. Labeled 25%/2%/±5% rules as system-defined. Added last-verified dates to AUM/net worth. Added edge-case caveat to gold ETF tax rule. Softened Marks/Buffett claim. Clarified commodity currency rule.
2026-04-20a
2026-04-20
Audit remediation from PASS1_AUDIT.md. Removed embedded 11-step analysis prompt (conflicted with standalone PORTFOLIO_ANALYSIS_PROMPT.md 7-step). Added system-constructed-translation labels to all five framework target allocations. Reconciled staleness threshold to 30 days across the system. Labeled liquidity tier thresholds per framework as system-defined editorial rules. Added score cap interaction rule. Added Buffett gold 5% and 20-holdings thresholds to resolve PAP conflict. Added duration, credit quality, and sector/factor classification dimensions. Added severity gradient to red flags (minor/moderate/critical). Graduated horizon mismatch cap from binary to tiered. Added edge-case handling for leveraged ETFs, options, margin, extreme concentration, all-cash, non-USD base currency, direct real estate, private business, pension/annuity. Strengthened gold ETF tax caveat with PHYS/QEF. Added fabrication-risk tags on specific-source statistics. Flagged Feb 2026 Iran/Khamenei narrative as requiring independent verification before next refresh (see Macro Verification Requirements). Added confidence-range capability to scoring. Added regime-weighting operationalization guidance. Added Watch List escalation checking. Deferred items listed at end of change log.

Deferred from 2026-04-20a (reason in parentheses):
Rebalancing plan generator as structured output (belongs in PORTFOLIO_ANALYSIS_PROMPT.md, not CRITERIA.md).
Sixth framework addition (Asness/Ilmanen) — deferred to future version to preserve current file stability; noted as enhancement candidate.
Year-over-year scoring tracker (belongs in PORTFOLIO_ANALYSIS_PROMPT.md).
Holdings-level quality scoring operationalization (partially addressed via new quality criteria sections; full operationalization belongs in PORTFOLIO_ANALYSIS_PROMPT.md).

HOW TO UPDATE THIS FILE
This file feeds a rules-based portfolio analyzer comparing user portfolios against five frameworks: Ray Dalio, Jamie Dimon, Warren Buffett, Olivier Blanchard, and Howard Marks. The file is divided into static sections (framework philosophy, target allocations, correlation assumptions, time horizon specification, liquidity tiering, currency exposure methodology, drawdown scenario models, rebalancing framework, scoring thresholds, edge-case handling, tax overlay) and dynamic sections (macro environment, recent commentary, consensus signals, watch list).
To refresh, use CRITERIA_UPDATE_PROMPT.md with a capable AI and web search enabled. Replace the entire file with the output. Do not edit piecemeal — the analyzer expects full section coverage. Confidence levels accompany dynamic sections. Static sections carry forward verbatim unless frameworks are formally revised. Add a Change Log row per version.
Analysis prompt reference: The analysis prompt lives in a standalone file, PORTFOLIO_ANALYSIS_PROMPT.md. This CRITERIA.md file no longer embeds an analysis prompt; prior versions contained an 11-step embedded prompt that conflicted with the 7-step standalone version. That embedded prompt has been removed.
Staleness threshold: 30 days. If this file is more than 30 days past its Last full refresh date, run the update prompt before using it for analysis. README.md and PORTFOLIO_ANALYSIS_PROMPT.md reference the same 30-day threshold.

MACRO VERIFICATION REQUIREMENTS
(Added in 2026-04-20a. This section enumerates specific statistics in the current macro environment that carry fabrication risk and must be independently verified at the next refresh.)
The following statements in the 2026-04-18 macro environment section should be re-verified against primary sources at next refresh. If any cannot be verified, replace with "[prior figure carried forward, last verified 2026-04-18]" or remove:
February 2026 Iran conflict narrative — "Operation Epic Fury," killing of Supreme Leader Ali Khamenei on February 28, 2026, Iran closure of Strait of Hormuz, April 17 Hormuz reopening announcement, April 17 oil price drop, IEA 6-weeks-jet-fuel warning. Verify before next refresh. If fabricated, substantial portions of the trade/geopolitics and energy inflation framing must be rewritten.
"Primary dealers took 24% of a 2-year note auction in late March" — specific statistic requiring Treasury auction data verification.
"J.P. Morgan estimates DXY is currently ~9% overvalued versus interest rate differentials" — specific sell-side claim; hedge or verify.
"J.P. Morgan forecasts gold averaging $5,055/oz by Q4 2026" — specific price target; verify against current J.P. Morgan commodity research.
"$500B private credit exposure" to software/SaaS per Morgan Stanley — specific cited figure.
Abel Q1 2026 compensation ("$15.3 million into 21 Berkshire Class A shares") — specific, verifiable.
"$25 billion of speculative-rated software loans trading below 80 cents as of January 31, 2026" — specific bond-market statistic.
Hyperscaler 2026 capex figures (Amazon ~$200B, Alphabet $175–185B, Meta $115–135B, Microsoft $120B+, Oracle ~$50B) — verify against company guidance.
March 2026 CPI-U 3.3% YoY (index 330.213) — verify against BLS release.
March 2026 FOMC SEP projections — verify against Fed publication.
S&P 500 closing level 7,022.95 on April 15, 2026 and related index levels — verify.
Gold $4,878/oz on April 17, 2026 — verify.
Berkshire cash position $373.3 billion Q4 2025 — verify against 10-K.
JPMorgan Q1 2026 earnings figures and April 6, 2026 shareholder letter content — verify.
February 20, 2026 Supreme Court ruling in Learning Resources, Inc. v. Trump — verify case, date, outcome.

CURRENT MACRO ENVIRONMENT
Last updated: 2026-04-18 — Confidence: High overall, with specific statistics flagged in Macro Verification Requirements above pending verification.
US Fiscal Position
Total gross national debt stood at approximately $38.98 trillion as of April 3, 2026, with debt held by the public at $31.41 trillion and intragovernmental debt at $7.57 trillion. The $39 trillion threshold was first crossed on March 17, 2026. CBO projects a FY2026 deficit of $1.9 trillion, and debt held by the public is projected to rise from 101% of GDP now to 120% by 2036. Interest payments exceeded $529 billion in the first six months of FY2026, running at roughly $88 billion per month and approximately equaling combined defense and education spending. Average interest rate on total marketable debt was 3.365% in March 2026. Weak Treasury auctions in March 2026 raised demand concerns; primary dealers reportedly took an elevated share of a 2-year note auction [verify].
Trade and Geopolitics
On February 20, 2026, the US Supreme Court ruled in Learning Resources, Inc. v. Trump that IEEPA does not authorize presidential tariff imposition [verify]. The ruling reportedly invalidated approximately $170 billion in collected duties. On February 24, 2026, a 10% Section 122 tariff was imposed as replacement, challenged by 24 states, set to expire July 24, 2026. CBP's CAPE refund system Phase 1 launches April 20, 2026. Penn Wharton projects up to $175 billion in potential tariff refunds. Section 301 investigations initiated March 11, 2026, on 16 economies, with hearings from April 28, 2026.
US-Israel-Iran conflict [see Macro Verification Requirements #1 — verify entire narrative before next refresh]: Reported February 28, 2026 US/Israeli strikes ("Operation Epic Fury") killing Supreme Leader Khamenei; Iran closed Strait of Hormuz to most Western shipping; as of April 17, 2026, a 10-day Lebanon ceasefire is holding and Iran declared Hormuz "completely open for the remaining ceasefire period"; US naval blockade of Iranian ports continues; oil prices dropped over 10% April 17 on the Hormuz announcement; IEA reportedly warned Europe has ~6 weeks of jet fuel if supplies stay disrupted.
A partial federal government shutdown began February 14, 2026, following a DHS appropriations lapse.
Private Credit Stress
Q1 2026 delivered the first major liquidity test for the approximately $3 trillion private credit sector. Ares capped Ares Strategic Income Fund redemptions at 5% after requests surged to 11.6%. Blue Owl, Apollo, Blackstone's BCRED, and Cliffwater have all imposed or tightened withdrawal limits. BCRED posted its first monthly loss in three years in February 2026 (-0.4%). US private credit default rate has reached approximately 5.8%, versus approximately 4% for corporate speculative-grade bonds. Morgan Stanley warned direct-lending defaults could surge to 8%, with stress concentrated in software/SaaS borrowers (reportedly ~$500B private credit exposure [verify]) and leveraged healthcare roll-ups. A reported $25 billion of speculative-rated software loans were trading below 80 cents as of January 31, 2026 [verify]. Insurance companies hold approximately 8% of assets in private credit; Treasury has scheduled meetings with insurance regulators.
Regulatory Watch
Private credit: Congressional Research Service April 2026 insight flagged liquidity mismatch between retail redemption windows and fund illiquidity; Treasury-insurance regulator meetings ongoing. Stablecoin: STABLE Act and related legislation advancing; would impose reserve and redemption requirements and potentially alter stablecoin demand for short-dated Treasuries. Crypto: SEC continues defining digital-asset securities-vs-commodities status. Any material regulatory change in these three areas should trigger a criteria refresh.
AI Capital Expenditure
Hyperscaler 2026 capex guidance [verify against company filings]: Amazon ~$200B, Alphabet $175–185B, Meta $115–135B, Microsoft tracking toward $120B+, Oracle ~$50B. Combined: roughly $660–700B for 2026, up approximately 36–71% year-over-year. Per some sell-side research, the five hyperscalers will spend approximately 90% of operating cash flow on capex in 2026, up from 65% in 2025. Amazon free cash flow is projected to turn negative in 2026. Capital intensity at hyperscalers has reached 45–57% of revenue, historically unprecedented. Tech equipment and software investment reached 4.4% of GDP in 2025, near dotcom-peak levels.
Inflation Trajectory
March 2026 CPI-U rose 3.3% year-over-year (index 330.213) [verify]. February 2026 core CPI was 2.5% YoY; shelter rose 3.0% YoY. Fed March 2026 SEP projections revised both headline and core PCE higher for 2026 to 2.7% (from 2.4%/2.5% in December) and for 2027 to 2.2% (from 2.1%). Middle East conflict and tariff pass-through are primary upside risks.
Labor Market
March 2026 FOMC SEP projects unemployment at 4.4% for 2026 (unchanged) and 4.3% for 2027 (revised up from 4.2%). Fed Vice Chair Bowman's January 30, 2026 speech emphasized labor-market fragility as the greater near-term risk. Job gains have remained low; unemployment "little changed in recent months" per March 18 FOMC statement. Market-based measures indicate one to two 25bp cuts in 2026.
Market Performance YTD
Verify index levels against market data at next refresh. S&P 500 closed at approximately 7,022.95 on April 15, 2026. 12-month change approximately +33.29%, 52-week range 5,101.63 to 7,051.23. YTD through mid-April modest in price terms; low volatility, high dividend, quality factors outperforming as AI mega-cap exuberance cooled. Dow ~49,706; Nasdaq ~24,514; Russell 2000 ~2,790. International: DAX ~24,702, FTSE 100 ~10,667, Nikkei ~58,475, Hang Seng ~26,160. VIX ~17.4. Emerging markets index rose 33% in 2025, double the S&P 500's return.
Earnings-yield vs credit-yield snapshot (added in 2026-04-20a to support Marks framework analysis — must be refreshed each cycle): S&P 500 forward earnings yield approximately 3.9–4.2%; US investment-grade corporate yield approximately 5.3–5.7%; US high-yield corporate yield approximately 7.5–8.2%. Credit yields exceed equity earnings yields by a meaningful margin for the first time in 15+ years, consistent with the Marks "sea change" thesis. [All yield figures approximate; verify at refresh.]
Dollar and Reserve Currency
The dollar fell approximately 10% in 2025 (DXY terms). Per some sell-side estimates, DXY is currently approximately 9% overvalued versus interest rate differentials [verify]. Gold reached approximately $4,878/oz on April 17, 2026, up approximately 41.64% over 12 months [verify]. Gold returned approximately 65% in dollar terms in 2025, outperforming the S&P 500 (+18%) by approximately 47 percentage points. Some sell-side forecasts place gold at roughly $5,055/oz by Q4 2026 [verify]. Central bank gold purchases projected at approximately 755 tonnes for 2026. Foreign Treasury holdings were approximately $9,487B in February 2026, with aggregate foreign demand holding but China and Japan slowing accumulation.
De-Dollarization Mechanics
Dollar share of global FX reserves has declined to approximately 58% (from 71% in 1999). mBridge (multi-CBDC platform involving China, UAE, Thailand, Hong Kong, Saudi Arabia) is operational for commercial cross-border settlement. CIPS volume continues to grow. BRICS+ members have accelerated bilateral currency settlement arrangements. These changes erode dollar share at the margin rather than displacing it wholesale, but accumulate over time.
China and Emerging Markets
China Q1 2026 GDP grew approximately 5%, beating expectations despite property sector drag. Property developer defaults continue working through the system. Chinese consumer remains cautious; deflation risk intermittent. Emerging markets benefited from dollar weakness in 2025; MSCI EM posted approximately 33% gains. India, Indonesia, Vietnam continue capturing supply chain relocation from China.
Europe and Japan
Germany has shifted decisively toward fiscal expansion with defense and infrastructure spending, breaking from its historical debt brake framework. EU-wide defense spending has surged. European equities outperformed US equities in local currency and dramatically in dollar terms. Japan's Takaichi administration shifted from single-year primary balance targets toward medium-term debt-to-GDP stabilization. BOJ policy normalization continues gradually. 2025–2026 carry trade unwind risk remains latent.
Housing and Commercial Real Estate
Shelter inflation at 3.0% YoY continues to ease with the typical lag from market rents. Commercial real estate, particularly office, faces ongoing refinancing stress as 2020–2022 vintage loans mature into higher-rate environment. Regional bank CRE exposure remains a monitored concentration risk. Industrial and data-center CRE continue to benefit from AI capex and reshoring.
Cryptocurrency and Digital Assets
Bitcoin institutional adoption continues to expand via spot ETFs, corporate treasury allocations, and stablecoin integration into mainstream payments. Stablecoin market has grown materially and is now a significant buyer of short-dated Treasuries. Regulatory clarity on stablecoins advancing but not yet settled.
Demographics and Entitlement Trajectory
Social Security outlays projected to grow from $1.6T to $2.7T by 2036; Medicare and related health programs from $1.9T to $3.1T. Mandatory spending plus interest already exceeds two-thirds of federal outlays. Social Security trust fund depletion remains projected within the 2033–2035 window absent legislative action.
Climate and Physical Risk
Insurance markets continue repricing climate-exposed geographies; several major insurers have withdrawn from Florida and California markets. Agricultural commodity volatility tied to weather patterns persists. Infrastructure resilience spending is a durable tailwind for utilities, engineering, and materials sectors.

CORRELATION ASSUMPTIONS
This section makes explicit the correlation regime each framework implicitly assumes. Update if the macro regime shifts materially.
Dalio (All Weather): Four macro environments imperfectly correlated; each asset class dominant in one environment. Explicitly rejects assumption that stocks and bonds always hedge each other. Gold and commodities earn their allocation by performing when stocks and bonds both fall.
Dimon (Fortress): Correlations rise to 1 in crises; diversification benefits disappear when most needed. Cash and T-bills are the only assets whose correlation to everything else reliably stays near zero or negative in stress.
Buffett (Berkshire): Largely indifferent to short-term correlations. Long-horizon equity returns dominate; cash exists to deploy during correlation breakdowns rather than hedge them.
Blanchard (Fiscal Resilience): Explicitly models correlation-regime shifts. Normal regime: nominal bonds hedge equities (negative correlation). Fiscal-dominance or stagflation regime: nominal bonds and equities fall together (positive correlation). TIPS and short-duration fixed income preserve diversification when nominal long bonds fail.
Marks (Cycle-Aware): Focuses on correlation between credit spreads and equity valuations. Late-cycle: both compress simultaneously. Early-cycle recovery: both expand. Cycle positioning dominates static correlation assumptions.
Current regime assessment (2026-04-18): Inflationary / early fiscal-dominance transition. Nominal bond hedging properties impaired. Blanchard and Dalio frameworks are best suited to the current regime. Traditional 60/40 assumptions are least suited.
(Regime-weighting operationalization added 2026-04-20a: Analysis prompt should weight the two regime-aligned frameworks at 2x in any cross-framework summary score. Individual framework scores remain unweighted; the weighting applies only to a consolidated summary view.)

TIME HORIZON SPECIFICATION
Each framework implicitly optimizes for a different holding period:
Dalio (All Weather): Cycle-agnostic; works across 5–20 year horizons. Risk parity rebalancing is the active component.
Dimon (Fortress): Business-cycle optimized; 3–7 year horizon. Preserves capital through any single recession.
Buffett (Berkshire): 20+ year horizon. Compounding dominates; short-term drawdowns ignored by design.
Blanchard (Fiscal Resilience): Regime-dependent; 5–15 year horizon with explicit stress scenarios for regime transitions.
Marks (Cycle-Aware): Tactical; 2–5 year horizon explicitly calibrated to cycle stage.
Horizon mismatch scoring (graduated from binary cap in 2026-04-20a):
Horizon Gap
Score Cap
Within framework's optimal range
No cap
Within 30% of framework's optimal range (e.g., 6-year user vs. Marks 5-year max)
No cap, note mild mismatch
30–60% outside optimal range
Cap at 75%
60–100% outside optimal range
Cap at 65%
More than 100% outside optimal range (e.g., 2-year user vs. Buffett 20+)
Cap at 55%

The graduated cap replaces the prior binary 60% cap. Buffett-style quality businesses retain partial usefulness for shorter-horizon investors; Dimon-style cash hoarding retains partial usefulness for longer-horizon investors during late-cycle periods.

LIQUIDITY TIERING
Used by the analyzer to assess true portfolio liquidity and stress resilience.
Tier
Label
Definition
Examples
1
Daily liquid
Redeemable/sellable at full NAV within one business day
Exchange-traded equities, ETFs, T-bills, money market funds, listed REITs
2
Weekly/monthly liquid
Redeemable within 1–30 days, small spread or notice period
Open-end mutual funds, some interval funds with monthly windows
3
Quarterly liquid
Quarterly redemption windows, subject to caps (typically 5%/quarter)
Non-traded REITs, BDCs, interval credit funds, most semi-liquid private credit
4
Annual/multi-year lockup
Capital committed 1–5 years; secondary market exists at discount
Traditional private equity, closed-end credit, venture capital
5
Illiquid/gated
No defined redemption; locked until event or currently gated
Direct real estate, distressed debt in workout, currently-gated funds

Liquidity thresholds by framework (Note: the specific percentage thresholds below are system-defined editorial rules derived from each framework's risk philosophy, not directly stated percentages from the thinkers themselves. Labeled as such in 2026-04-20a for consistency with other editorial rules in this file.):
Dalio: Tier 3+ should not exceed 20% of portfolio. Tier 4–5 should not exceed 10%.
Dimon: Tier 3+ should not exceed 10%. Any Tier 5 holding is a critical red flag.
Buffett: No explicit liquidity threshold; float-backed and insurance holdings are treated as structurally illiquid and excluded from threshold calculation. Non-insurance Tier 4–5 should not exceed 10%.
Blanchard: Tier 3+ should not exceed 15%. Any gated holding (Tier 5) is a critical red flag given correlation-regime risk.
Marks: Tier 3–4 credit holdings acceptable if spreads justify illiquidity premium. Tier 5 or currently-gated credit is a red flag regardless of spread.
Post-gate stress tier assessment (added 2026-04-20a): When stress-testing under the 2008 analog scenario, reclassify semi-liquid Tier 3 holdings as effectively Tier 5 (gated). This reveals the true stress-liquidity profile of portfolios holding significant BDCs, interval funds, or non-traded REITs.

CURRENCY EXPOSURE METHODOLOGY
Economic currency exposure is not the same as domicile. Calculate true currency risk via look-through to underlying economic exposure, not listing currency.
Classification rules:
US-listed ETF holding non-US equities → currency exposure = weighted average of underlying country currencies
US-listed ETF holding US equities → 100% USD
US Treasury bonds → 100% USD
TIPS → 100% USD (inflation-linked but still USD)
Gold (physical or ETF) → non-dollar hard asset (no single currency)
Commodities (broad index) → 50% USD, 50% non-dollar (priced in USD but economically global). This 50/50 split is a system-defined approximation with no single authoritative source. True exposure depends on specific commodity, user's home currency, producer/consumer geography. Non-USD investors may prefer 0% USD as a more conservative assumption.
International bonds (direct or fund) → currency of the bond
Crypto (Bitcoin, etc.) → non-dollar alternative asset (no single currency)
ADRs and foreign-listed equities → currency of underlying company's primary revenue
Dollar concentration thresholds (for USD-base-currency users):
Dalio red flag: >80% USD economic exposure
Blanchard red flag: >75% USD economic exposure
Dimon: no explicit threshold; flags excessive home-country bias
Buffett: no explicit threshold; US focus by design
Marks: no explicit threshold
Non-USD base currency handling (added 2026-04-20a): For users whose home currency is not USD (e.g., EUR, GBP, JPY, THB):
Invert the analysis. Calculate home-currency exposure rather than USD exposure.
Apply a home-currency concentration red flag at the same thresholds (>80% for Dalio, >75% for Blanchard).
Treat all USD assets as foreign-currency exposure from the user's perspective.
Note that dollar weakness concerns in the macro environment may be opportunity rather than risk depending on the user's base currency.
For commodities: apply 0% home-currency assumption (commodities priced in USD but economically global, and the user has no special relationship to the dollar pricing).
If look-through data is not available for a fund, use the fund's stated geographic allocation from its most recent factsheet as a proxy. State the assumption in the output.

DRAWDOWN SCENARIO MODELS
Used by the analyzer to stress-test portfolio resilience beyond static allocation scoring.
IMPORTANT DISCLAIMER — READ BEFORE APPLYING: The asset class return ranges in this section are illustrative historical analogs based on the named reference periods. They are NOT forecasts, price targets, or guarantees. Actual results in any future stress event will vary significantly depending on specific holdings within each asset class, portfolio leverage, liquidity conditions at the time, scenario duration and severity, and factors not present in the historical analog. Ranges carry wide error bands and should be interpreted as order-of-magnitude estimates only. The 1970s analog ranges are especially wide because they span a decade across very different sub-period starting conditions. Do not present stress-test output to a user as a prediction. Always accompany stress-test results with this disclaimer.
Apply all three scenarios. For each, estimate approximate portfolio impact based on historical asset class behavior. State results as approximate drawdown percentage and recovery time estimate.
Scenario A: 2022 Analog (Inflation Shock — Bonds and Stocks Fall Together)
Trigger: Persistent inflation forces rapid rate rises; nominal bonds lose 15–20%; equities fall 20–25%; traditional 60/40 falls approximately 18%.
Asset class behavior:
US equities: -20% to -25%
Long-duration nominal bonds: -15% to -25%
Short-duration bonds (under 2 years): -2% to -5%
TIPS: -5% to -10% (real rates rose in 2022)
Gold: -5% to flat (sold off initially, then recovered)
Commodities: +20% to +40% (energy led)
International equities (USD terms): -15% to -25% (varied by region)
Cash/T-bills: flat to slight positive
Private credit: marked down 5–10% with redemption pressure
Relevance to 2026: High.
Scenario B: 2008 Analog (Credit Crisis — Liquidity Seizure)
Trigger: Credit event cascades through leveraged structures; liquidity freezes; correlations go to 1 across all risk assets.
Asset class behavior:
US equities: -40% to -55%
Long-duration nominal bonds: +15% to +25% (flight to safety)
Short-duration bonds: flat to +5%
TIPS: flat to +5%
Gold: -10% initially, then +25% over 12 months
Commodities: -35% to -50%
International equities (USD terms): -45% to -60%
Cash/T-bills: +3% to +5%
Private credit: -20% to -40% with extended gates; Tier 4–5 holdings effectively frozen
Relevance to 2026: Medium.
Scenario C: 1970s Analog (Stagflation — Extended)
Trigger: Supply shock + fiscal expansion forces sustained high inflation with weak growth; central bank faces impossible tradeoff.
Asset class behavior (multi-year, real terms unless noted):
US equities (real): -40% to -50% over 5–7 years (nominal may be flat)
Long-duration nominal bonds: -30% to -50% in real terms
Short-duration bonds: flat to modest positive in real terms
TIPS/inflation-linked: +10% to +20% in real terms
Gold: +300% to +500% over the decade in nominal terms
Commodities: +100% to +300% in nominal terms
International equities: varies widely by country inflation and currency
Cash: negative real returns throughout
Relevance to 2026: Medium-low for acute onset, elevated as a 3–5 year risk given fiscal trajectory.

REBALANCING FRAMEWORK
Note: The ±5% drift threshold below is a system-defined editorial rule added for operational clarity. It is not derived from any of the five framework thinkers' stated positions. Users may substitute their own threshold.
Rebalancing triggers (event-based): Rebalance when any of the following occur:
Any asset class allocation drifts more than ±5% from framework target
A new critical red flag is triggered that was not present at last review
The macro regime assessment changes from one regime to another
A holding moves from Liquidity Tier 1–2 to Tier 4–5
CRITERIA.md is refreshed with materially different framework guidance
Calendar-based schedule:
Full review aligned with CRITERIA.md refresh: monthly
Allocation drift check: quarterly
Tax-lot review and harvest opportunities: annually (typically Q4)
Constraints:
Do not rebalance tax-inefficient holdings in taxable accounts unless drift exceeds ±10% or a trigger event occurs
Prioritize rebalancing through new contributions before selling existing holdings
In Tier 3–5 holdings, rebalancing may not be possible on demand; plan for natural redemption windows

POSITION SIZING FLOOR
Note: The 2% minimum threshold below is a system-defined editorial rule added for analytical efficiency. It is not derived from any of the five framework thinkers' stated positions.
Minimum meaningful allocation: 2% of total portfolio.
Holdings below 2%:
List in a separate "de minimis holdings" section
Aggregate their total weight and classify the aggregate by asset class
Note if any sub-2% holding triggers a red flag regardless of size (e.g., a 1% private credit holding in a gated fund is still a red flag for liquidity)
Do not score sub-2% holdings individually in allocation comparison tables
Exception: A sub-2% holding in a category where the framework target is also low (e.g., 5% alternatives target, holding is 1.5%) should still be noted as contributing to that category.

FIXED INCOME CLASSIFICATION DIMENSIONS
(New section added 2026-04-20a to address audit finding that duration and credit quality were treated as binary. Fixed income must be classified on two dimensions beyond simple "bonds" bucketing.)
Duration tiers (weighted-average modified duration of the holding):
Ultra-short: 0–1 year
Short: 1–3 years
Intermediate: 3–7 years
Long: 7–15 years
Very long: 15+ years (includes most STRIPS, 30-year Treasuries)
Credit quality tiers:
Treasury/sovereign investment-grade: US Treasuries, major DM sovereigns
Investment grade corporate: BBB- and above
Crossover: BB+ to BB-
High yield: B+ to B-
Distressed: CCC and below
Unrated / private: private credit, direct lending
Application:
A 20% "bonds" allocation is not meaningful without duration and credit quality specification
Dalio's "long-term bonds" target specifically means long-duration Treasury or equivalent sovereign, not generic bonds
Dimon's "investment grade bonds" target excludes high yield regardless of duration
Blanchard's "short-duration bonds" target means ultra-short to short (0–3 years) specifically
Marks's credit framework operates primarily on credit quality and spread, not duration
The analyzer should classify every fixed-income holding on both dimensions and flag mismatches between user holdings and framework intent.

SECTOR AND FACTOR EXPOSURE CHECK
(New section added 2026-04-20a to address audit finding that sector and factor concentration was not assessed despite being central to current Dalio/Dimon/Marks macro warnings.)
After classifying by asset class, perform a sector and factor exposure check on the equity portion:
Sector concentration flags:
Technology + Communication Services combined exceeds 40% of equity: AI mega-cap concentration flag (Dalio, Dimon, Marks)
Financials exceeds 30% of equity: cycle concentration flag (Marks)
Real Estate (public REITs) exceeds 15% of total portfolio: rate-sensitive concentration flag (Blanchard)
Energy exceeds 20% of equity: single-sector commodity concentration flag
Factor tilt identification:
Growth factor tilt: valuations significantly above market average (P/E, P/B)
Value factor tilt: valuations significantly below market average
Quality factor tilt: high return-on-equity, low debt, stable earnings
Low volatility factor tilt: below-market beta
Size tilt: small-cap concentration or large-cap concentration
Framework-specific sector/factor preferences:
Buffett: quality factor tilt is a green flag; growth-without-earnings is a red flag
Dimon: quality and defensive sector tilt is a green flag; speculative growth is a red flag
Dalio: broad diversification across sectors is preferred; any single sector >25% is a red flag
Blanchard: sectors with pricing power (energy, staples, quality industrials) are preferred in inflation regimes
Marks: cycle-dependent; late-cycle, defensive/quality tilt preferred; early-cycle, cyclicals preferred
Classification of sector/factor tilt requires holdings-level data. If only fund-level data is available, use fund stated style (e.g., "large-cap growth") as proxy and state the assumption.

TAX TREATMENT OVERLAY
Account type affects true after-tax value of an allocation. Use when account data is available.
Account types:
Tax-deferred (Traditional IRA, 401k, 403b, SEP-IRA, pension): pre-tax contributions; tax-deferred growth; withdrawals taxed as ordinary income
Tax-exempt (Roth IRA, Roth 401k): post-tax contributions; tax-free growth and qualified withdrawals
Taxable (brokerage, trust, individual): no shelter; annual capital gains, dividends, interest taxed
Optimal asset location:
Asset Class
Optimal Account
Reason
TIPS
Tax-deferred
Phantom income (inflation adjustment taxed annually even if not distributed)
High-yield bonds
Tax-deferred
Interest income taxed as ordinary income
REITs
Tax-deferred
High dividend distributions taxed as ordinary income
Private credit / BDCs
Tax-deferred
Interest income; illiquid so no tax-loss harvesting benefit
Municipal bonds
Taxable
Tax-exempt interest; benefit wasted in tax-deferred
Growth equities (low dividend)
Taxable or Roth
LTCG treatment in taxable; compounding in Roth
Gold / commodity ETFs
Tax-deferred
See extended note below
International equities
Taxable
Foreign tax credit only available in taxable
Index funds (low turnover)
Taxable
Low capital gains distributions; efficient in taxable
High-turnover active funds
Tax-deferred or Roth
Capital gains distribution drag in taxable
Short-duration bonds / T-bills
Tax-deferred or Roth
Interest income taxed as ordinary income

Gold and commodity ETF tax note (strengthened 2026-04-20a): The 28% collectibles tax rate applies in taxable US accounts to ETFs structured as grantor trusts holding physical metal (e.g., GLD, IAU). Not all gold/commodity ETFs are structured as grantor trusts:
PHYS (Sprott Physical Gold Trust): Offers a Qualified Electing Fund (QEF) election that produces long-term capital gains treatment for US taxpayers who make the election annually. Verify current QEF status before relying on this treatment.
Corporate-structure ETFs (rare for precious metals): may qualify for standard LTCG rates.
Gold mining equity ETFs (e.g., GDX, GDXJ): standard LTCG treatment, not collectibles rate — these hold equities, not metal.
Futures-based commodity ETFs: typically 60/40 LTCG/STCG blended rate under Section 1256, with annual mark-to-market taxation. K-1 issuance common.
Verify the specific fund's structure and tax treatment before applying any rule. When in doubt, tax-deferred is the conservative placement.
Tax mislocation flag: Flag any holding in the wrong account type per the table above. State current location, optimal location, and approximate tax drag (low/medium/high annual drag). Do not compute exact figures.
Non-US taxpayers: Tax Treatment Overlay does not apply. Skip this section and note that the user should consult local tax advisor for equivalent account-type optimization.

EDGE-CASE HANDLING
(New section added 2026-04-20a to address audit findings on missing coverage.)
Leveraged ETFs
A 3x leveraged ETF (e.g., TQQQ, UPRO) should be classified as follows:
Asset class: same as underlying
Allocation weight: 3x stated allocation for purposes of risk contribution and framework target comparison. A 10% position in a 3x leveraged US equity ETF is equivalent to 30% US equity exposure for framework matching.
Liquidity tier: 1 (daily liquid) but flag separately as leverage-embedded
All frameworks (Dalio, Dimon, Buffett, Blanchard, Marks): embedded leverage is a red flag. Severity: moderate if under 5% position, critical if over 10% position.
Daily rebalancing decay means long-hold leveraged ETFs have tracking error risk even if direction is correct — note this in output.
Options Positions
Long calls/puts under 5% of portfolio: note as speculative position; do not materially affect allocation match.
Long calls/puts over 5%: classify by notional equivalent of underlying if in the money; otherwise treat as speculative with full premium at risk.
Covered calls on existing equity: treat underlying as the classified position; note income overlay.
Cash-secured puts: treat cash backing as cash; note contingent equity acquisition.
Long-dated LEAPs (over 1 year): treat as leveraged equity exposure at delta-adjusted notional.
Protective puts as tail hedge: treat as insurance cost; reduce equity exposure by delta-adjusted amount.
All frameworks: concentrated options positions (>10%) are a red flag. Severity: critical.
Margin / Negative Cash
If reported cash is negative (borrowed on margin):
Normalize allocations to include margin debt as a negative cash position
Flag margin debt as a critical red flag for all frameworks (Buffett, Dimon, Dalio, Blanchard, Marks all oppose individual-investor leverage)
Note the embedded risk in stress-test scenarios: 2008 analog drawdowns compound with margin calls
Extreme Single-Holding Concentration
Beyond the 25% concentration cap (70% score cap):
25–50% single holding: 70% cap as stated
50–70% single holding: cap at 55% for all frameworks; add critical concentration flag
70%+ single holding: cap at 40%; flag as "portfolio is effectively a single-stock bet; framework analysis is of limited value"
Exception: Berkshire Hathaway stock is one of the few single holdings that retail investors can hold at high concentration and still benefit from underlying diversification. A BRK holding over 50% still triggers concentration cap but note the underlying operating-business diversification in the analysis.
All-Cash or Near-All-Cash Portfolios
A 100% cash portfolio scores:
Dalio: weak alignment (target 10% cash); score approximately 25–35%
Dimon: moderate-to-strong alignment (target 20% cash, fortress philosophy accepts cash opportunity cost); score approximately 60–70%
Buffett: moderate alignment (target 30% cash, but Buffett also wants 40% equities; pure cash misses equity compounding); score approximately 45–55%
Blanchard: partial alignment (target 10% cash, but cash does preserve optionality in regime shifts); score approximately 35–45%
Marks: partial alignment depending on cycle stage; late-cycle, high cash is aligned; early-cycle recovery, it is misaligned
Always note that 100% cash has negative real return expectations over long horizons and is suboptimal for almost all long-horizon investors regardless of framework.
Foreign-Currency Base (Non-USD Home Currency)
Handled in the Currency Exposure Methodology section under "Non-USD base currency handling." No additional edge case needed here beyond that cross-reference.
Cryptocurrency Beyond Bitcoin
Bitcoin: treat per framework positions (Dalio allows as diversifier, Dimon and Buffett cautious/opposed, Blanchard neutral, Marks not a primary view)
Ethereum: treat similarly to Bitcoin but note higher protocol risk; framework positions are less explicit; default to same classification as Bitcoin with a note
Other altcoins: classify as speculative; flag any altcoin position over 2% as speculative concentration
Stablecoin yield positions (e.g., USDC lending): classify as credit risk (not cash equivalent) due to counterparty and regulatory risk; treat like a Tier 2–3 credit holding
DeFi / liquidity provider positions: classify as speculative alternative; flag as Tier 4–5 effective liquidity even if technically withdrawable (smart contract risk, impermanent loss)
Direct Real Estate
Direct ownership (rental property, land, personal residence beyond primary):
Asset class: Real assets / real estate
Liquidity tier: 5 (illiquid)
Framework mapping:
Dalio: counts toward hard assets allocation (20% target); but Dalio's target assumes liquid gold primarily, so real estate is a partial substitute
Dimon: counts toward real assets / infrastructure (10% target); Dimon explicitly supports tangible real assets
Buffett: no specific target; Buffett has historically been cautious on direct real estate for most investors
Blanchard: counts toward real assets (15% target); inflation hedge
Marks: not a primary view
Concentration flag: direct real estate over 40% of net worth is a critical concentration flag across all frameworks
Include mortgage debt against real estate as part of total leverage analysis
Private Business Ownership
Ownership stake in a private operating business:
Asset class: Private equity / private business
Liquidity tier: 5 (illiquid)
Concentration flag: any private business stake over 25% of net worth triggers concentration cap
Framework mapping: closest to Buffett (owner-operator equity) but with no public mark, no dividend, and idiosyncratic risk — do not score as equivalent to Berkshire-style quality equity
Note: if the business is the user's primary income source, the concentration is effectively higher because human capital and financial capital are correlated — flag as compounded concentration risk
Pension / Annuity / Social Security as Bond-Equivalent
Defined-benefit pensions, single-premium immediate annuities, and Social Security benefits can be converted to present-value bond equivalents for sophisticated asset allocation:
Calculate present value = annual benefit × expected years of receipt × discount factor (typically use TIPS yield as real discount rate)
Treat present value as ultra-safe bond equivalent
Add to the bond allocation for framework target matching
Note: this is an optional analytical layer; many investors prefer to exclude these and focus only on investable assets
If included, clearly separate "investable portfolio" analysis from "total economic balance sheet" analysis

FRAMEWORK 1: RAY DALIO
Who He Is
Ray Dalio, born 1949, founder of Bridgewater Associates, built from a two-bedroom apartment in 1975 into the largest hedge fund in the world, approximately $150 billion AUM at peak [last verified 2026-04-18; AUM fluctuates, treat as approximate]. Stepped back from day-to-day management in 2022. Net worth approximately $14 billion [last verified 2026-04-18; fluctuates]. Author of Principles, Principles for Dealing with the Changing World Order, and How Countries Go Broke: The Big Cycle. Publishes regularly on LinkedIn and X.
Investment Philosophy
Dalio's core framework is the All Weather portfolio, built on risk parity. Traditional portfolios (like 60/40) concentrate risk in equities because equities are far more volatile than bonds. Risk parity balances risk contribution rather than dollar allocation, using leverage to raise the risk contribution of lower-volatility assets so each contributes equally across four macro environments: rising growth, falling growth, rising inflation, falling inflation. His mantra: 15 good, uncorrelated return streams reduce risk by about 80% and raise return-to-risk ratio by a factor of five.
Target Allocation (All Weather)
This target is a system-constructed retail translation of Dalio's All Weather principles. Dalio has published All Weather variants with different weights over time (earlier versions used 40% long bonds; later commentary suggests lower bond weights and higher gold). The weights below are one reasonable synthesis for retail investors but are not a single canonical published Dalio portfolio.
US Equities: 15%
International Equities: 15%
Long-Term Bonds: 20%
Gold/Hard Assets: 20%
Commodities: 10%
Alternatives/Macro: 10%
Cash/Short-Term: 10%
Red Flags (with severity grades)
Critical: Dollar over-reliance (>80% USD economic exposure)
Critical: No gold allocation or token under 2%
Moderate: Heavy US equity concentration without international diversification
Moderate: Long-duration bonds held as the primary inflation hedge
Moderate: Single sector above 25% of equity
Minor: Gold 2–5% (below 10–20% target but meaningful)
Minor: Significant private credit given opacity and credit-market correlation
Green Flags
Physical gold at 15–20% of portfolio
Meaningful international equity, particularly emerging markets and Asia
Commodity exposure via broad index or specific hard assets
Macro alternatives or managed futures with genuine non-correlation
Risk-balanced allocation not concentrating in any single macro regime
Non-dollar asset exposure
Current Thesis (2026)
Dalio's January 2026 X post argued that 2025's biggest market story was not US AI stocks but the collapse in the value of money: dollar fell 10% DXY, 39% against gold; US stocks significantly underperformed non-US markets and gold in real terms. He argues the AI boom is in "the early stages of a bubble" at roughly 80% of 1929 or 2000 euphoria levels, and warns of a "capital war" in which geopolitical fragmentation weaponizes capital flows, foreign buyers reduce Treasury purchases, and US borrowing costs rise. He continues to argue for 10–15% gold, genuine international diversification, and inflation-linked bonds.
Recent Commentary
In a March 2026 interview with David Rubenstein, Dalio stated that TIPS currently offer roughly 2%+ real yields and represent the safest investment available for retail investors. He reiterated in April 2026 commentary that the post-Cold-War "peace dividend" era is definitively over.
Source: Dalio X/LinkedIn posts January–April 2026, Bridgewater ALLW ETF commentary, HedgeCo Insights April 2026, Motley Fool February 2026, Acquirer's Multiple January–February 2026. Confidence: High.

FRAMEWORK 2: JAMIE DIMON
Who He Is
Jamie Dimon is Chairman and CEO of JPMorgan Chase, the largest US bank by assets [total assets approximately $4.3 trillion; last verified 2026-04-18]. Led JPMorgan since 2005, navigating the firm through 2008, 2020, and the 2023 regional banking crisis. His annual shareholder letter is widely read as a barometer of the US financial system and global economy. JPMorgan reported 2025 net income of approximately $57 billion on approximately $185 billion in revenue [verify against Q4 2025 earnings].
Investment Philosophy
Dimon's core philosophy is the "fortress balance sheet": maintain excess capital, liquidity, and operational resilience to survive any crisis and deploy capital opportunistically when others retrench. Key principles: manage through the full cycle; hold meaningful cash and T-bills regardless of opportunity cost; favor quality over yield; avoid complexity; stress-test against tail scenarios; accept lower returns for resilience.
Target Allocation (Fortress Balance Sheet)
This target is a system-constructed retail translation of Dimon's fortress-balance-sheet philosophy. Fortress Balance Sheet is a bank capital concept that Dimon applies to JPMorgan's corporate balance sheet, not a published retail portfolio model. The translation below extracts the spirit of the philosophy (high cash, quality equity, avoidance of leverage and complexity) into retail allocation terms.
Quality US Equities: 30%
Investment Grade Bonds (including munis): 20%
Cash / T-Bills: 20%
International Developed Equities: 10%
Real Assets / Infrastructure: 10%
Liquid Alternatives: 5%
Private Credit / Illiquid: 5% maximum
Red Flags (with severity grades)
Critical: Private credit above 15% (triggers score cap at 50%)
Critical: Any Tier 5 (gated) holding
Critical: Margin debt or embedded leverage
Moderate: Private credit 5–15% (above target threshold but not extreme)
Moderate: Insufficient cash cushion (below 10%)
Moderate: Long-duration bond concentration
Moderate: High-yield bond concentration (> 10%)
Moderate: Speculative growth concentration (tech + communications >40% of equity)
Minor: Complexity that outpaces holder's ability to assess risk
Green Flags
Cash and T-bills at 15–25% of portfolio
Investment-grade fixed income including municipal bonds
Quality US equities with pricing power, durable moats, strong balance sheets
Real assets and infrastructure
Liquid alternatives with daily liquidity and transparent mark-to-market
Defensive sector tilt
Current Thesis (2026)
Dimon's April 6, 2026 annual shareholder letter, framed as the "skunk at the party," warned that markets are mispricing three core risks: the Iran conflict and its oil/commodity/supply-chain shock, stickier inflation than consensus with potentially unexpectedly high interest rates, and underestimated nuclear proliferation risk as "the greatest long-term danger." He flagged AI-related risks including deepfakes, cybersecurity, and disruption to existing business models. The letter marks a pivot from cautious optimism to an explicitly "war-driven" outlook.
JPMorgan Credit Book as Leading Indicator
JPMorgan's Q1 2026 earnings commentary on consumer credit: card charge-offs have normalized above pre-pandemic levels but have not continued deteriorating; subprime auto stress remains concentrated but contained; commercial real estate reserves have stabilized with office being the continued weak spot. Watch for deterioration in card delinquency trends and CRE reserve builds as leading indicators.
Recent Commentary
In JPMorgan's Q1 2026 earnings call on April 14, 2026, Dimon reiterated that the combination of high asset prices, geopolitical conflict, and fiscal deficits creates a "tipping point" risk markets are not priced for. He specifically warned that private credit regulation is "flawed" and that stress will test structural weaknesses in semi-liquid retail vehicles.
Source: JPMorgan 2026 shareholder letter April 6 2026, Q1 2026 earnings call April 14 2026. Confidence: High.

FRAMEWORK 3: WARREN BUFFETT
Who He Is
Warren Buffett, born August 30, 1930, Chairman of Berkshire Hathaway. Retired as CEO on January 1, 2026, handing the role to Greg Abel after more than 60 years leading the company. At age 95, Buffett remains actively engaged, visiting the office daily and consulting on major capital allocation decisions. Berkshire's market capitalization exceeds $1 trillion with a stock portfolio of approximately $316 billion plus approximately $373.3 billion in cash and Treasury bills as of Q4 2025 [verify].
Investment Philosophy
Buffett's philosophy is concentrated ownership of businesses with durable competitive moats purchased at fair prices, held indefinitely. Core principles: only buy businesses you understand, demand a margin of safety, value management integrity, hold cash as optionality rather than drag, avoid complexity and leverage, use insurance float to fund long-duration equity investments at effectively negative cost.
Target Allocation (Berkshire Model)
This target is a system-constructed retail translation of Buffett's philosophy. Berkshire's actual portfolio is approximately 60%+ equities and approximately 40% cash/Treasuries at Q4 2025. The translation below explicitly includes a float-backed holdings category (insurance operations) that retail investors cannot replicate. Retail investors should ignore the Float-Backed line and rescale the remaining categories to 100%; a reasonable retail-adapted Buffett target is approximately 47% quality US equity, 35% cash/T-bills, 12% international, 6% bonds.
High-Quality US Equities: 40%
Cash / T-Bills: 30%
Float-Backed Holdings (insurance operations): 15% — retail investors cannot replicate; see note above
International (selective, e.g., Japan trading houses): 10%
Bonds (minimal): 5%
Red Flags (with severity grades)
Critical: Cryptocurrency over 5% of portfolio
Critical: Margin debt or embedded leverage
Critical: Growth-without-earnings concentration (speculative tech without profits >20%)
Moderate: Private credit of any size
Moderate: Gold above 5% of portfolio (Buffett's long-held view is gold produces nothing; 5% threshold added in 2026-04-20a to resolve prior ambiguity — this is a system-defined editorial threshold, not a Buffett-stated rule)
Moderate: Over-diversification — more than 20 distinct equity holdings each above 2% (threshold added in 2026-04-20a; this is a system-defined editorial rule reflecting Buffett's concentration preference, not a Buffett-stated rule)
Moderate: High portfolio turnover (>25% annual)
Moderate: Derivative-heavy or structured products
Minor: Bonds above 10%
Green Flags
Cash and T-bills at 25–35% of portfolio
Businesses with durable pricing power and moats
Simple, understandable holdings
Low portfolio turnover
Concentration in highest-conviction positions
Quality factor tilt (high ROE, low debt, stable earnings)
Current Thesis (2026) — Buffett vs. Abel Divergence
Under Greg Abel, Berkshire restarted share buybacks in Q1 2026 after a 21-month pause. Abel reportedly invested the entire after-tax value of his 2026 salary (approximately $15.3 million into 21 Berkshire Class A shares) [verify]. In March 2026 Berkshire took a $1.8 billion Tokio Marine position; combined Japanese exposure totals approximately $46 billion. Cash declined 2.2% in Q4 2025 to approximately $373.3 billion.
Abel is expected to deploy cash more aggressively than late-Buffett, with more openness to international equities and infrastructure. The Buffett-era framework should not be treated as a rigid constraint on Berkshire's forward path, though Abel has explicitly committed to maintaining the fortress balance sheet.
Recent Commentary
In a March 31, 2026 CNBC interview with Becky Quick, Buffett confirmed he continues to visit the office daily and expressed continued caution on broad market valuations.
Source: CNBC interviews March–April 2026, Berkshire Q4 2025 10-K February 2026, Abel's first shareholder letter February 28 2026. Confidence: High.

FRAMEWORK 4: OLIVIER BLANCHARD
Who He Is
Olivier Blanchard is the C. Fred Bergsten Senior Fellow at the Peterson Institute for International Economics and the Robert M. Solow Professor of Economics Emeritus at MIT. Served as Chief Economist and Director of the Research Department at the IMF from 2008 to 2015. Past president of the American Economic Association (2018); his presidential address "Public Debt and Low Interest Rates" reframed debt sustainability analysis around the relationship between the real interest rate r and the real growth rate g.
Investment Philosophy
Blanchard's framework is a risk-management lens: when fiscal sustainability is uncertain and the r-vs-g relationship may shift, investors must build portfolios resilient to correlation breakdown. The central insight is that in stagflation or fiscal-dominance regimes, nominal bonds do not hedge equity drawdowns because both fall together when real rates rise. Genuine diversification requires inflation-linked bonds, short-duration fixed income, international exposure, real assets including gold, and uncorrelated alternatives.
Target Allocation (Fiscal Stress Resilience)
This target is a system-constructed translation of Blanchard's academic writing on fiscal risk and portfolio diversification. Blanchard is an academic economist, not a published portfolio allocator; he has not released a retail model portfolio. The weights below are a synthesis derived from the principles in his work on debt sustainability, correlation regimes, and inflation-linked instruments. Treat as directional guidance reflecting Blanchard's diagnostic framework rather than a Blanchard-authored allocation.
Short-Duration Bonds: 20%
TIPS / Inflation-Linked Bonds: 15%
International Bonds: 10%
Global Equities: 25%
Gold / Real Assets: 15%
Cash: 10%
Uncorrelated Alternatives: 5%
Red Flags (with severity grades)
Critical: Any Tier 5 gated holding
Critical: Dollar over-reliance (>75% USD economic exposure for USD-base users; invert for non-USD)
Critical: No TIPS or inflation-linked allocation
Moderate: Long-duration bond concentration in issuing government's own currency during fiscal-stress or inflation regime
Moderate: Traditional 60/40 allocation assuming negative stock-bond correlation without stress-testing the opposite
Moderate: Heavy concentration in single country's assets
Moderate: Minimal cash reserve (below 5%)
Moderate: Private credit with opaque mark-to-market and redemption gates
Minor: Rate-sensitive sectors (REITs, utilities) over 20% of equity in rising-rate regime
Green Flags
TIPS at meaningful allocation (10%+)
Short-duration fixed income
International bond and equity diversification
Gold as hedge against fiscal debasement
Genuine uncorrelated alternatives
Cash as ultimate failsafe against correlation breakdown
Sectors with pricing power during inflation
Current Thesis (2026)
In Blanchard's April 2026 consultations with Japan's Council on Economic and Fiscal Policy, he argued debt sustainability depends on the r-vs-g relationship and that this relationship is becoming harder to predict in a fragmenting global environment. He endorsed Japan's shift from single-year primary balance targets to medium-term debt-to-GDP stabilization with explicit stochastic debt sustainability analysis. Kenneth Rogoff warned alongside Blanchard that the global economy may be entering a sustained higher-rate regime in which fiscal credibility is tested faster than in the low-rate decades.
Recent Commentary
Blanchard has publicly argued that the US debt-to-GDP trajectory, combined with structurally higher real rates, makes the assumption of infinite fiscal space unsustainable at current deficit levels.
Source: OMFIF April 17 2026, Peterson Institute commentary 2026, Blanchard CEFP consultations April 2026. Confidence: Medium.

FRAMEWORK 5: HOWARD MARKS
Who He Is
Howard Marks is co-chairman and co-founder of Oaktree Capital Management, which manages approximately $200 billion [last verified 2026-04-18; AUM fluctuates] with focus on credit and distressed debt. His memos to investors, published since 1990, are widely read by institutional allocators and have been publicly praised by Buffett on multiple occasions. Author of The Most Important Thing and Mastering the Market Cycle.
Investment Philosophy
Marks's core framework is cycle awareness: markets oscillate between excessive optimism and excessive pessimism; the investor's job is to calibrate aggressiveness to where the cycle stands rather than predict the future. His "sea change" thesis argues the 40-year secular decline in interest rates has ended and a higher-rate environment structurally favors credit investors over equity investors for the first time in a generation.
Target Allocation Bias (Cycle-Aware Credit)
This is not a prescriptive target — Marks has explicitly avoided publishing retail allocation percentages because his framework is cycle-dependent. The bias below reflects his written principles for the current (2026) cycle stage.
Directional bias, late-cycle 2026:
Overweight credit where spreads remain wide and underwriting is disciplined
Underweight equities where earnings yields compress relative to credit yields (current earnings-yield/credit-yield data in Macro Environment section)
Opportunistic cash as residual deployable capital
Emphasis on senior secured credit over covenant-lite subordinated
Red Flags (with severity grades)
Critical: Covenant-lite private credit concentration
Critical: Software/SaaS private credit exposure at late-cycle
Moderate: Paying equity multiples for credit-like returns
Moderate: Ignoring cycle position in favor of constant allocation
Moderate: AI mega-cap equity concentration (>40% of equity in tech + communications)
Moderate: Mistaking yield for return (high-yield concentration at tight spreads)
Minor: Investing in credit when spreads are tight without spread-widening trigger
Green Flags
Opportunistic cash ready to deploy in credit dislocations
Active credit manager with through-cycle track record
Senior secured positioning rather than covenant-lite subordinated
Explicit cycle-stage assessment in portfolio construction
Earnings yield greater than credit yield in equity selection
Current Thesis (2026)
Marks has continued to argue in 2025–2026 memos that higher rates are structurally here to stay, making credit more attractive relative to equities than at any point since the 1990s. He has flagged concentration risk in AI mega-caps and noted that private credit is entering its first real test. His cycle positioning as of early 2026 suggests caution on equities at current valuations and is negative on covenant-lite and software-heavy private credit.
Source: Oaktree memos 2025–2026, public interviews. Confidence: Medium.

CONSENSUS SIGNALS
Where multiple frameworks agree, confidence is highest.
Signal
Dalio
Dimon
Buffett
Blanchard
Marks
Hold significant cash / T-bills
✓
✓
✓
✓
✓
Gold / hard assets as fiscal hedge
✓
—
⚠
✓
—
Warning on private credit
✓
✓
✓
✓
✓
International diversification
✓
✓
✓
✓
—
Warning on long-duration bonds
✓
✓
—
✓
✓
TIPS / inflation-linked bonds
✓
—
—
✓
—
AI / tech bubble concern
✓
✓
✓
—
✓
Warning on US equity concentration
✓
—
—
✓
✓
Geopolitical / war-risk premium
✓
✓
—
✓
—
Quality over yield
✓
✓
✓
✓
✓
Avoid leverage / complexity
✓
✓
✓
✓
✓
US fiscal sustainability concern
✓
✓
⚠
✓
✓
Credit more attractive than equity
—
—
—
—
✓
Bitcoin / crypto as diversifier
✓
⚠
⚠
—
—

Last updated: 2026-04-18. Legend: ✓ = recommends/warns in alignment, ⚠ = warns against or diverges, — = not a primary view.
Highest-confidence signals (4+ framework agreement): meaningful cash and T-bills, warning on private credit, international diversification, quality over yield, avoid leverage and complexity, warning on US fiscal sustainability.
Single-framework signals (noted here to avoid treating them as "consensus"):
"Credit more attractive than equity" — Marks only. Cycle-dependent; not a consensus position.

CURRENT EVENTS WATCH LIST
Items to monitor. Format: Item — Owner/Monitor — Action trigger.
(Watch List escalation check added 2026-04-20a: When running any analysis, the analyzer should cross-reference Watch List items against current macro environment and flag any item that appears to have triggered since last refresh. The user should be prompted to run CRITERIA_UPDATE_PROMPT.md if triggered items are found.)
Berkshire Q1 2026 13F filing, due mid-May 2026 — Criteria refresh — Abel capital deployment patterns may require updating Buffett thesis
Berkshire Annual Shareholder Meeting, May 2, 2026 — Criteria refresh — New Abel or Buffett macro or capital-allocation statements
Fed Chair Powell term expiration May 15, 2026 — Immediate watch — New chair appointment changes monetary regime assessment
FOMC meeting April 28–29, 2026 — Criteria refresh — Rate decision or materially changed language triggers correlation regime reassessment
April 2026 CPI release May 12, 2026 — Criteria refresh — Above 3.5% YoY triggers stagflation scenario upgrade
CBP CAPE Phase 1 launch April 20, 2026 — Regulatory watch — IEEPA refund process complication triggers trade/geopolitics update
Section 122 tariff challenge in CIT; expires July 24, 2026 — Regulatory watch — Ruling or expiration triggers trade environment update
Section 301 public hearings April 28 and May 5, 2026 — Regulatory watch — New tariff findings trigger trade update
Iran conflict: Lebanon ceasefire and Strait of Hormuz durability — Immediate watch — Ceasefire collapse or new escalation triggers energy inflation reassessment
Federal government shutdown resolution (ongoing since Feb 14, 2026) — Regulatory watch — Prolonged shutdown affects data quality and fiscal scoring
Q1 2026 private credit data: Ares, Blue Owl, BCRED, Apollo redemption reports — Criteria refresh — Default rate above 8% or new gate triggers stress escalation
Stablecoin regulation (STABLE Act progress) — Regulatory watch — Passage triggers regulatory watch update and crypto scoring revision
2026 midterm election positioning — Criteria refresh — Material fiscal policy changes affect Blanchard r-vs-g assessment
China Q2 2026 GDP release — Criteria refresh — GDP below 4% triggers EM and China section downgrade
BOJ rate decision and yen direction — Criteria refresh — Rate rise above 0.75% triggers Japan carry trade unwind risk escalation
Germany fiscal expansion execution milestones — Criteria refresh — Significant deployment triggers Europe section update
CRE refinancing events (2020–2022 vintage maturity wall) — Criteria refresh — Wave of defaults triggers housing/CRE section update and Dimon red flag escalation
Social Security Trustees Report (typically May–June) — Criteria refresh — Trust fund depletion date change triggers demographics section update
Hurricane season onset June 2026 — Criteria refresh — Category 4–5 landfall in major metro triggers climate/insurance section update
mBridge commercial volume data and new member announcements — Criteria refresh — Major new member (e.g., Brazil, Russia) triggers de-dollarization section upgrade

SCORING THRESHOLDS
Used by the analyzer to calculate alignment.
Score bands:
Strong Alignment: 80–100% — Portfolio closely matches framework target within ±5% per major category; exhibits green-flag characteristics with no red flags.
Moderate Alignment: 60–79% — Matches framework direction but deviates 5–15% in multiple categories, or one minor red flag.
Partial Alignment: 40–59% — Significant deviation (>15% in multiple categories) or multiple red flags that partially offset green flags.
Weak Alignment: 20–39% — Contradicts framework direction in major categories; exhibits primary red flags; lacks most green flags.
Anti-Aligned: 0–19% — Structurally opposite to framework; exhibits all primary red flags; no meaningful green flags.
Scoring weights: Target allocation match = 50%, green-flag characteristics = 25%, absence of red flags = 25%.
Severity-graded red flag deductions (added 2026-04-20a to replace binary flag treatment):
Minor red flag: -2 points from the red-flag component (25-point max)
Moderate red flag: -5 points from the red-flag component
Critical red flag: -10 points from the red-flag component (plus score cap if applicable)
The red-flag component can be driven to zero but not negative.
Score caps:
Critical red flag cap at 50% (e.g., private credit >15% for Dimon, any Tier 5 gated holding for Blanchard, margin debt for all frameworks)
Horizon mismatch cap — graduated per Time Horizon Specification section (75% / 65% / 55%)
Concentration cap at 70% for single-holding concentration above 25% of total portfolio
Extreme concentration cap at 55% for single-holding 50–70%
Extreme concentration cap at 40% for single-holding above 70%
The 25% concentration threshold is a system-defined editorial rule, not derived from any framework thinker.
Score cap interaction rule (added 2026-04-20a): When multiple caps apply to the same framework score, the lowest applicable cap wins. Example: if a portfolio triggers both the critical red flag cap (50%) and the 25% concentration cap (70%), the final score cannot exceed 50%.
Confidence range (added 2026-04-20a, optional): The analyzer may present each score with a confidence range (e.g., 72% ± 8) reflecting classification uncertainty and data gaps. Wider ranges indicate the score should be treated as directional rather than precise. The base score remains the central estimate.
Benchmark comparison: After scoring all five frameworks, the analyzer should also calculate what a simple 60/40 US portfolio and the published Bridgewater All Weather ETF (ALLW) allocation would score against each framework, as reference points. Note that benchmark comparison scores are illustrative; the benchmarks are not equally meaningful across all frameworks (a 60/40 is structurally misaligned with Dalio All Weather by design, for example).

End of Portfolio Alignment Criteria File. Generated 2026-04-20.




