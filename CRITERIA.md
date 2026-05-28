# Portfolio Alignment Criteria File

*Version: 2026-05-27a*

*Last full refresh: 2026-05-27*

*Next scheduled refresh: 2026-06-27*

---

## SECTION 2 — CHANGE LOG

| Date | Version | Description of Changes |
| :--- | :--- | :--- |
| 2026-04-25 | 2026-04-25b | Section count expanded 24 → 25. Added benchmark portfolios. Section 9 expanded to 5 named scenarios. Section 16 expanded to 9 edge cases. Section 24 added explicit scoring math placeholder. |
| 2026-05-07 | 2026-05-07a | Updated April 29 FOMC: held 3.50–3.75% (8-4 vote, most dissents since 1992); Powell announced he stays on Board after May 15; Warsh confirmation pending. Updated market levels to May 6 close: S&P 7,365 record. Iran peace deal advanced May 6 (Axios). Resolved Watch List items: April 28-29 FOMC, Berkshire Annual Meeting May 2, Section 301 hearings. |
| 2026-05-08 | 2026-05-08a | Major v3 restructure to support analyzer 2026-05-08a. Added real-allocator backing per framework in Section 5. Pinned scoring algorithm in Section 24 with explicit deduction formula. Cut Climate and Demographics subsections from Section 4. Trimmed Watch List from 19 to 10 items. Trimmed Consensus Signals from 14 to 8 rows. |
| 2026-05-27 | 2026-05-27a | Major macro refresh. Warsh confirmed Fed Chair May 13 (54-45). April CPI 3.8% headline / 2.8% core (May 12). April jobs +115K, unemployment 4.3% (May 8). CIT struck down Section 122 tariffs May 7 (relief limited; CAFC stay). Iran war: US naval blockade of Hormuz continuing (100+ ships redirected), 14-point MOU under negotiation, US strikes May 25-26. Updated market levels to May 26: S&P 7,519 record, Nasdaq 26,656, Dow 50,462, gold $4,523, BTC $76,755, WTI $93.89, 10Y 4.50%. UMich May final sentiment 44.8 (fresh all-time record low); 1-yr inflation expectations 4.8%, 5-10 yr 3.9%. Q1 hyperscaler capex: combined $650-725B. BDC Q2 redemption requests forecast 12-15% peak. FOMC minutes signal possible rate hike. |

---

## SECTION 3 — HOW TO UPDATE THIS FILE

This file is the primary reference for the Portfolio Analyzer. To update:
1. Conduct web searches for each dynamic subsection in Section 4.
2. Review the prior Watch List (Section 23) — note what resolved.
3. Update Consensus Signals (Section 22) only when a framework's stance shifts based on new public commentary.
4. Increment version number, update "Last full refresh" date.
5. Maintain static editorial rules and system-defined labels.

---

## SECTION 4 — CURRENT MACRO ENVIRONMENT

*Where recent data is unavailable, prior figures carry forward only with [verify] tags. Inline [verify] tags must match Section 13 exactly.*

### US Fiscal Position
*Last updated: 2026-05-27* | *Confidence: High*
* **National Debt:** $39T+ as of early May (Treasury Debt to the Penny, May 22 update).
* **Deficit:** FY2026 cumulative deficit smaller than same period prior year per CBO May 8 monthly update. Net interest YTD (Oct-April) $628B, averaging $2.96B/day. Net interest projected at 13.85% of outlays FY2026, rising to 14.11% FY2027 (CBO).
* **Treasury Auctions:** Bid-to-cover ratios as of January: T-bills 2.85, 10-year notes 2.38, 30-year bonds 2.29 (JEC Monthly Debt Update). 10-year yield rose to 4.50% on May 26; 30-year briefly topped 5% in early May.
* **Interest Burden:** Average interest rate on total marketable debt 3.348% (January). Net interest outlays up 7% YoY through first seven months of FY2026.
* **Maturity:** ~33% of publicly held marketable debt matures within 12 months.

### Trade and Geopolitics
*Last updated: 2026-05-27* | *Confidence: High*
* **Tariff Authority — SCOTUS Ruling:** Feb 20, 2026 *Learning Resources v. Trump* 6-3 decision held IEEPA does not authorize tariff imposition. ~$166B in IEEPA tariffs being refunded via new CBP CAPE system.
* **Section 122 Tariffs — CIT Ruling May 7, 2026:** US Court of International Trade ruled 2-1 that 10% global tariff under Section 122 exceeds presidential authority. Permanent injunction limited to three plaintiffs (Burlap & Barrel, Basic Fun, State of Washington). Federal Circuit issued administrative stay May 12; CIT denied government's stay motion May 20 but CAFC stay holds. Most importers continue paying. Section 122 expires July 24, 2026 absent reauthorization. Average effective US tariff rate ~11% [verify].
* **Section 301:** USTR investigations covering 60 economies (forced labor) and 16 economies (excess capacity). Expected to conclude in time to impose new Section 301 tariffs before Section 122 expires July 24.
* **Iran War — Active Diplomatic and Military Phase:** US-Israeli war began Feb 28, 2026. **US naval blockade of Strait of Hormuz still in place — over 100 commercial ships redirected.** May 25-26: US conducted "self-defense strikes" on Iranian missile launch sites and boats. **14-point one-page MOU under negotiation** with proposed 30-60 day framework. Trump May 23: agreement "subject to finalization." Pakistan-mediated April 8 ceasefire was violated by both sides; Islamabad talks failed. $24B Iranian assets potentially to be released only after Hormuz reopens.
* **Strait of Hormuz Status:** Blockade now over 90 days. IEA May 2026: global oil supply down 12.8 mb/d since February; Gulf country output 14.4 mb/d below pre-war levels.

### Private Credit Stress
*Last updated: 2026-05-27* | *Confidence: High*
* **Moody's BDC Outlook:** Negative since April 7, 2026 — liquidity mismatches, elevated leverage, AI as "disruptive force."
* **Q1 2026 Redemption Wave:** Blue Owl OCIC (~$36B): 21.9% requests, 5% cap. Blue Owl OTIC (~$6B): 40.7% requests, 5% cap. Apollo Debt Solutions: 11.2% requests, ~45% fulfilled. Morgan Stanley North Haven: ~11% requests, 5% cap. BlackRock HLEND: 9.3% requests. Cliffwater $33B interval fund: 14% requests against 7% cap.
* **Q2 2026 Forecast (BofA):** Apollo Debt Solutions 15%, Ares Strategic Income 14%, Blackstone BCRED 12%, HLEND 13%. Q2 expected to be peak redemption quarter. BofA committed $25B to direct lending.
* **Defaults:** Direct lending default rate ~5.6% (Morgan Stanley); potential to reach 8% — well above 2–2.5% historical average. PIK toggle usage rising in software/SaaS.
* **Marks Memo:** April 9 "What's Going On in Private Credit" — direct lending facing first major test since 2008; structural liability-side risk from retail investor base.

### Regulatory Watch
*Last updated: 2026-05-27* | *Confidence: High*
* **Fed Chair Transition Complete:** Kevin Warsh confirmed as Fed Chair May 13, 2026 in 54-45 Senate vote — closest in modern era. Only Sen. John Fetterman (D-PA) crossed party lines. Powell's chair term expired May 15; Powell remains on Board of Governors until 2028. Warsh has called for "regime change" at the Fed; first Warsh-chaired FOMC is June 16-17, 2026. Trump expects rate cuts; Warsh has not committed.
* **April 29 FOMC (Powell's final meeting):** Held 3.50–3.75% (third consecutive hold). Vote 8-4 — most dissents since 1992. Miran dissented for 25bp cut; Bowman, Schmid, and one other against easing-bias language.
* **May 20 FOMC Minutes:** Officials see possible rate HIKE if inflation stays elevated. Markets pricing 80% probability of December 2026 rate hike — sharp reversal from prior cut expectations.
* **DOJ — Powell:** Criminal investigation ended April 24, 2026.
* **Crypto/Stablecoin:** Stablecoin Transparency Act remains in Senate committee.
* **Banking — Basel III Endgame:** Reduced severity vs 2023 version per Dimon Q1 2026 commentary. Final implementation delayed to late 2026.

### AI Capital Expenditure
*Last updated: 2026-05-27* | *Confidence: High*
* **Q1 2026 Hyperscaler Capex Prints (April 29 earnings):** Microsoft $190B FY2026; Alphabet raised to $180-190B; Meta raised to $125-145B; Amazon ~$200B. Combined four hyperscaler 2026 capex tracking $650-725B.
* **AI Run Rates:** Microsoft AI at $37B annualized (+123% YoY). Google Cloud +63% YoY to $20B quarterly; backlog $462B. AWS +28% YoY (fastest in 15 quarters). GOOGL signaled 2027 capex will significantly increase from 2026.
* **AI Mega-Cap Leadership:** Top 7 mega-caps ~38%+ of S&P 500 market cap. Nvidia ~$5.5T, Alphabet ~$4.9T, Apple ~$4.4T.
* **Bubble concern:** Marks's December 2025 memo "Is It a Bubble?" addressed AI parallels to prior bubbles. Dalio February-March commentary connected AI investment cycle to broader Big Cycle/capital war thesis.

### Inflation Trajectory
*Last updated: 2026-05-27* | *Confidence: High*
* **April CPI (released May 12):** Headline 3.8% YoY (up from 3.3% March), highest since May 2023. +0.6% MoM. Energy +3.8% MoM, accounting for >40% of headline gain. Food +0.5%; gasoline +28.4% YoY.
* **April Core CPI:** 2.8% YoY (up from 2.6% March), +0.4% MoM. Services less energy +3.3% YoY. Shelter +0.5% MoM.
* **Real Wages:** -0.5% MoM, -0.3% YoY — first time in three years wages no longer outpacing inflation.
* **May CPI release scheduled June 10.**
* **Fed Outlook:** Federal funds target 3.50–3.75% (held April 29). FOMC statement: inflation "is elevated." May 20 minutes signaled possible hike if inflation continues.
* **Consumer Sentiment — Record Low:** University of Michigan May final reading 44.8 (revised down from 48.2 preliminary), third straight monthly decline, below June 2022 trough — fresh all-time low in series history (since 1952). Current Conditions 45.8 (-12.8% MoM). 57% of consumers cite high prices as eroding finances. 1-yr inflation expectations 4.8% (vs 3.4% pre-war February). 5-10 yr expectations 3.9% (7-month high).

### Labor Market
*Last updated: 2026-05-27* | *Confidence: High*
* **Unemployment:** 4.3% April (BLS May 8). Unchanged for three months.
* **Payrolls:** April +115K (vs consensus 55K). March revised up to +185K; February revised down to -156K. Three-month average ~+48K.
* **JOLTS:** 6.9 million openings February; quits rate 1.9%; hires 4.8M.
* **Participation:** 61.9% (lowest since November 2021); U-6 8.0%.
* **Wages:** Average hourly earnings +0.2% MoM, +3.6% YoY. Real wages now negative.
* **Workweek:** Up 0.1 hour to 34.3 hours April.

### Market Performance YTD
*Last updated: 2026-05-27* | *Confidence: High*
* **S&P 500:** 7,519.12 record close (May 26, +0.61%). Eighth straight week of gains.
* **Nasdaq:** 26,656.18 record close (May 26, +1.19%).
* **Dow:** 50,461.68 (May 26, -0.23%).
* **Russell 2000:** 2,848.74 (May 26, +1.11%).
* **VIX:** 16.87 (May 26).
* **Crude Oil:** WTI $93.89 settle Friday May 22; Brent ~$99.58 May 26. Iran war risk premium continues.
* **MSCI EAFE YTD:** +6.1% [verify]; **MSCI EM YTD:** +10.4% [verify].
* **10-Year Treasury Yield:** 4.50% (May 26, FRED); 30-year briefly topped 5% earlier in May. 10-year TIPS 2.16% (May 22, FRED).
* **Forward P/E:** ~21.0 (FactSet May 8); above 5-year (19.9) and 10-year (18.9) averages. Q1 2026 earnings growth running ~28% YoY — highest since Q4 2021.

### Dollar and Reserve Currency
*Last updated: 2026-05-27* | *Confidence: High*
* **DXY:** ~99.27 mid-May, slightly stronger May 26 on Iran tensions [verify].
* **Gold:** $4,522.59/oz spot May 26 (CNBC). Reached record $5,595 January 28. State Street Monthly Gold Monitor cites $4,000–4,750 structural floor.
* **Central Bank Buying:** Continued heavy purchasing from China (~2,309t official reserves), India, Turkey.

### China and Emerging Markets
*Last updated: 2026-05-27* | *Confidence: Medium*
* **China GDP:** ~4.6% annualized; property sector workouts ongoing.
* **India:** MSCI India outperforming EM peers; Modi-Trump tariff deal lowering rates 25% → 18% conditional on India halting Russian oil purchases.

### Europe and Japan
*Last updated: 2026-05-27* | *Confidence: Medium*
* **Japan:** BOJ ended NIRP; Yen volatility around 152-157 with Tokyo intervention reported around May 1 after breaching 160.
* **Europe:** ECB on hold at 2.00% deposit rate; markets pricing 1-2 ECB hikes 2026 [verify]. Germany debt brake remains contentious.

### Housing and Commercial Real Estate
*Last updated: 2026-05-27* | *Confidence: Medium*
* **Residential:** Transaction volumes ~20% below 5-year average; mortgage rate ~6.30% [verify].
* **Office CRE:** ~20% Tier 1 vacancy; regional banks increasing 2026 maturity loan-loss provisions.

### Cryptocurrency and Digital Assets
*Last updated: 2026-05-27* | *Confidence: High*
* **Bitcoin:** $76,754 (May 26, 9:30 AM ET). Tested $74,500 floor May 22-23 (lowest in two months). ETF outflows $1.26B over six consecutive sessions. Whale accumulation at year-high.
* **Ethereum:** $2,111 (May 26).
* **Stablecoin Market Cap:** Continued growth; legislation pending.

### Earnings Yield vs Credit Yield Snapshot
*Last updated: 2026-05-27* | *Confidence: Medium-High*
* **S&P 500 Forward Earnings Yield:** ~4.76% [verify] (1 / ~21.0 forward P/E from FactSet May 8 at S&P 7,519 close May 26).
* **US Investment-Grade Yield:** ~5.20% [verify] (10Y 4.50% + IG OAS estimate).
* **US High-Yield Yield:** ~7.26% [verify] (10Y 4.50% + HY OAS 2.76% May 14 FRED).
* **Spread (Earnings Yield − IG Yield):** ~−0.44%.
* **Assessment:** Credit continues to offer materially higher yield than equity on a forward-looking basis. HY OAS at 2.76% is tight by historical standards. Negative spread continues to favor the **Marks** framework.

---

## SECTION 5 — CORRELATION ASSUMPTIONS AND FRAMEWORK BACKING

### Framework Philosophies and Real-Allocator Backing

Each of the five expert personas in this analyzer is a constructed translation — none of these individuals publishes a personal allocation model. To improve scoring rigor, each persona is informed by published research from real institutional allocators whose work aligns with the persona's stated philosophy.

* **Dalio (Risk-Parity Persona).** Translated allocation backed by AQR Capital Management published research on risk parity (Asness, Frazzini, Pedersen) and Bridgewater's own "All Weather" methodology white papers. The 30/40/15/7.5/7.5 allocation reflects equal risk contribution principles published by AQR and Bridgewater Daily Observations.

* **Dimon (Fortress Quality Persona).** Translated allocation backed by JPMorgan Asset Management's published Multi-Asset Solutions research on quality factor investing, plus academic work on quality minus junk (QMJ) by Asness/Frazzini/Pedersen. The 50/30/20 allocation reflects high-quality US equity bias plus structural cash buffer consistent with Fortress Balance Sheet principles.

* **Buffett (Long-Duration Quality Persona).** Translated allocation backed by David Swensen's published endowment model (Yale) for long-horizon allocators, plus academic literature on factor-premium decay over long holding periods. The 90/10 individual allocation reflects Buffett's published guidance to his wife's trustee; the underlying logic is supported by Swensen's framework for long-duration capital.

* **Blanchard (Fiscal-Stress Resilience Persona).** Translated allocation backed by Antti Ilmanen's published research at AQR on regime-aware asset allocation, plus Rob Arnott's (Research Affiliates) work on inflation-resilient portfolios. The 40/30/20/10 allocation reflects Blanchard's fiscal-sustainability concerns operationalized through Ilmanen's regime framework.

* **Marks (Cycle-Aware Credit Persona).** Translated allocation backed by Oaktree's own published memos (Marks's primary output) plus academic literature on credit-cycle timing (e.g., Asness on time-series momentum in credit). The credit-overweight bias reflects Marks's "Sea Change" framework; the operational allocation depends on cycle stage.

### Five-Regime Taxonomy (verbatim — analyzer requirement)

* **Traditional regime** — stocks and bonds negatively correlated; 60/40 works
* **Inflationary regime** — positive stock-bond correlation; nominal bonds fail as hedge; TIPS and real assets outperform
* **Stagflation regime** — growth falling, inflation rising; both stocks and bonds decline; gold, commodities, short-duration hedge
* **Fiscal-dominance regime** — central bank monetizes deficits; long-duration bonds repriced; real assets and international diversification critical
* **Deflationary regime** — growth and inflation falling; nominal bonds outperform; cash and quality bonds primary safety

### Current Regime Assessment

* **Current Regime:** Inflationary regime with intensifying stagflation risk and fiscal-dominance pressure. April CPI 3.8% confirms continued inflationary impulse — highest YoY since May 2023, with energy and tariff pass-through broadening into core (2.8%). UMich consumer sentiment at all-time low (44.8) while indices at records — classic late-cycle divergence with stagflation hallmarks. Slow payrolls (~48K three-month average) with 4.3% unemployment confirm slowing growth alongside rising inflation. Iran war and Hormuz blockade now persistent (>90 days).
* **Primary Risk Scenario:** Stagflation if Hormuz blockade extends and Iran MOU fails; alternative reflation if peace deal closes and oil normalizes. Fiscal-dominance pressure compounds either path — $39T+ debt, 30-year yield briefly above 5%, weak Treasury auctions, 33% of marketable debt rolling within 12 months. Warsh-Trump rate cut pressure vs market pricing 80% December hike probability sets up a major monetary-fiscal tension point.
* **Best Suited:** **Dalio** (gold/commodity/diversification) and **Blanchard** (fiscal-stress hedge with TIPS and international).
* **Least Suited:** **Buffett** (concentrated US equity exposure at record valuations; forward P/E ~21.0 well above 10-year average; mega-cap concentration ~38% of S&P).
* **Justification:** April CPI 3.8%, UMich sentiment all-time low 44.8, 5-10 yr inflation expectations 3.9% (7-month high), gold $4,522, 30Y briefly >5%, $39T+ debt with weak Treasury auctions, US naval blockade of Hormuz over 90 days, Powell-to-Warsh transition with monetary-fiscal pressure, and slowing labor market (48K 3-month average) together signal active inflationary regime with stagflation tilt and fiscal-dominance overhang.

* **Regime-Weighting Rule:** The analyzer applies 2x weighting to regime-aligned frameworks (Dalio and Blanchard at this refresh) in the regime-weighted summary view.

---

## SECTION 6 — TIME HORIZON SPECIFICATION

* **Definitions:**
    * Short-Term: < 3 years
    * Medium-Term: 3–7 years
    * Long-Term: > 7 years

* **Graduated Score Caps for Horizon Mismatches:**
    * Long-term portfolio with short-term need: **75% cap**
    * Short-term portfolio with long-term assets: **65% cap**
    * Immediate liquidity need with Tier 4/5 assets: **55% cap**

---

## SECTION 7 — LIQUIDITY TIERING

| Tier | Description | Examples |
| :--- | :--- | :--- |
| Tier 1 | Immediate Cash | Physical cash, Checking/Savings |
| Tier 2 | T+2 Liquidity | Major Index ETFs, Large-cap Stocks, US Treasuries |
| Tier 3 | Weekly/Monthly | Mutual Funds, Corporate Bonds, Small-cap Stocks |
| Tier 4 | Quarterly/Annual | Private Credit (un-gated), Hedge Funds, REITs |
| Tier 5 | Illiquid (>1 Year) | Real Estate, Private Equity, Gated Funds |

**Framework Thresholds:**
* Dalio: Min 30% Tier 1/2
* Dimon: Min 50% Tier 1/2
* Buffett: Min 20% Tier 1
* Blanchard: Min 40% Tier 1/2
* Marks: Variable (Current: Min 25% Tier 1/2)

**Post-Gate Stress Tier Reassessment:** Under "2008 analog stress" (Scenario 2), Tier 3 holdings reclassify to effective Tier 5 for scoring.

---

## SECTION 8 — CURRENCY EXPOSURE METHODOLOGY

* Classification by primary currency of underlying assets, look-through where possible.
* Commodity Currencies: AUD, CAD, NOK
* Dollar Concentration Threshold: >80% USD flagged for Dalio/Blanchard frameworks
* Non-USD Base Currency: thresholds invert; USD becomes the diversifying asset

---

## SECTION 9 — DRAWDOWN SCENARIO MODELS

> **DISCLAIMER:** Wide error bands based on historical return ranges. Real-world results may vary significantly.

**Scenario 1 — Inflation Shock (2022 Replay)**
Trigger: persistent inflation forces rapid rate rises; tariff pass-through; energy spike.
- US Equities: −20% to −25%
- Long-duration Bonds: −15% to −25%
- TIPS: −5% to −10%
- Commodities: +20% to +40%
- Gold: +5% to +15%
- Cash: real loss but nominal preserved
- *Relevance to 2026:* **High** — April CPI 3.8%, Iran war energy disruption persistent, UMich 5-10yr inflation expectations 3.9%.

**Scenario 2 — Credit Crisis (2008 Replay)**
Trigger: credit event cascades through leveraged structures; liquidity freezes; correlations rise to 1.
- US Equities: −40% to −55%
- Long-duration Treasuries: +15% to +25% (flight to safety)
- IG Corporate: −10% to −20%
- High Yield: −25% to −40%
- Private Credit: −20% to −40% (extended gates)
- Real Estate: −25% to −40%
- Gold: +10% to +20%
- Cash: best protector
- *Relevance to 2026:* **Medium-High** — Moody's BDC negative outlook, BofA Q2 forecast of 12-15% peak BDC redemptions, Marks April 9 memo, HY OAS at 2.76% tight by historical standards.
- Apply post-gate stress tier reclassification per Section 7.

**Scenario 3 — Extended Stagflation (1970s Replay)**
Trigger: growth stalls while inflation stays high for years; supply shock plus fiscal expansion.
- US Equities: −20% to −35% (real terms)
- Long-duration Bonds: −25% to −40%
- TIPS: 0% to +10%
- Commodities: +40% to +80%
- Gold: +50% to +150%
- International Equities: mixed; commodity exporters outperform
- *Relevance to 2026:* **High** — energy shock (Iran/Hormuz) + slowing growth (3-month payroll average +48K) + fiscal expansion + UMich sentiment all-time low while equities at records. May 20 FOMC minutes flag possible hike.

**Scenario 4 — Dalio's Debt Collapse (Fiscal Dominance)**
Trigger: foreign buyers stop purchasing US Treasuries; failed Treasury auction; dollar reserve share dropping below 50%.
- Long-duration Bonds: −30% to −50%
- US Dollar: −20% to −35% in real terms
- Gold: +50% to +150%
- Commodities: +30% to +80%
- US Equities: −30% to −50% in real terms
- International Equities: mixed
- Cash (USD): real loss but nominal preserved
- TIPS: 0% to +15%
- *Relevance to 2026:* **Medium** probability, high consequence — $39T+ debt; weak Treasury auctions; 33% of marketable debt rolling within 12 months; 30-year briefly topped 5%; Warsh-Trump rate cut pressure adds monetary dominance risk vector.

**Scenario 5 — Marks's Credit Boom (Early-Cycle Recovery)**
Trigger: recession clears excesses, credit spreads blow out, Fed pivots, disciplined buyer with cash and IG credit deploys at peak spreads.
- IG Corporate: +10% to +20%
- High Yield: +15% to +30%
- US Equities: +30% to +50% from trough
- Cash deployed into credit at peak spreads: outsized returns
- Gold: flat to −10%
- Long-duration Treasuries: −5% to −15%
- *Relevance to 2026:* **Medium-Low** — current cycle still pre-stress; possible 2027–2029 window if direct lending stress widens.

---

## SECTION 10 — REBALANCING FRAMEWORK

* Trigger: ±5% relative deviation from target framework allocation
* Frequency: Quarterly review recommended
* Tax Awareness: Rebalance in tax-advantaged accounts first

---

## SECTION 11 — POSITION SIZING FLOOR

System-Defined Editorial Rule: Any position < 2% of total AUM is treated as "Noise" and does not contribute to framework alignment scores, though it still counts toward concentration/diversification flags.

---

## SECTION 12 — TAX TREATMENT OVERLAY

**Account Types:** Taxable, Tax-Deferred (401k, Traditional IRA), Tax-Exempt (Roth)

**Optimal Location:**

| Asset Class | Optimal Location |
| :--- | :--- |
| TIPS | Tax-Deferred |
| High-Yield Debt | Tax-Deferred |
| Commodities/Gold | Taxable (Tax-managed) |
| Growth Stocks | Tax-Exempt |
| Municipal Bonds | Taxable |

**Caveats:**
* GLD: Subject to 28% collectibles rate for US taxpayers (Grantor Trust)
* PHYS: May qualify for QEF election (15/20% LTCG rate) if filed correctly

---

## SECTION 13 — MACRO VERIFICATION REQUIREMENTS

*The following items carry [verify] tags inline in the file and require independent verification at next refresh. This list must match the inline [verify] tags exactly — no orphans in either direction.*

* [verify] Average effective US tariff rate ~11% — Section 4 Trade and Geopolitics
* [verify] MSCI EAFE YTD +6.1% and MSCI EM YTD +10.4% — Section 4 Market Performance YTD
* [verify] DXY ~99.27 — Section 4 Dollar and Reserve Currency
* [verify] ECB rate path market expectation (1-2 hikes 2026) — Section 4 Europe and Japan
* [verify] Mortgage rate ~6.30% — Section 4 Housing and CRE
* [verify] Forward P/E ~21.0 / Forward earnings yield ~4.76% — Section 4 Earnings Yield vs Credit Yield
* [verify] US IG Yield ~5.20% — Section 4 Earnings Yield vs Credit Yield
* [verify] US HY Yield ~7.26% — Section 4 Earnings Yield vs Credit Yield

---

## SECTION 14 — FIXED INCOME CLASSIFICATION DIMENSIONS

* **Duration:** Ultra-short (<1yr), Short (1–3yr), Intermediate (3–7yr), Long (7–15yr), Very Long (15yr+)
* **Quality:** Treasury, Sovereign IG, Corporate IG, High Yield (Junk), Unrated/Private

---

## SECTION 15 — SECTOR AND FACTOR EXPOSURE CHECK

**Concentration Flags:**
* Tech + Comm > 40% (Overweight Growth)
* Financials > 30% (Banking Stress Risk)
* REITs > 15% (CRE Stress Risk)
* Energy > 20% (Commodity Bias)

**AI Mega-Cap Concentration Flag:** Top 7 US mega-caps (typically MSFT, AAPL, NVDA, GOOGL, AMZN, META, TSLA) >25% combined = AI Mega-Cap Concentration Flag. Moderate red flag for Dalio (concentration risk), Buffett (single-sector overweight), Marks (late-cycle equity concentration). Not a flag for Dimon or Blanchard unless additional sector flags compound.

**Framework Preference:**
* Buffett: Prefers Financials/Consumer/Energy. Dislikes Tech (traditionally).
* Dalio: Neutral (Equalized risk).

---

## SECTION 16 — EDGE-CASE HANDLING

* **Leveraged ETFs:** 2x/3x exposure to underlying; liquidity cap at 50% of nominal weight; moderate-to-critical red flag depending on size.
* **Options:** Delta-adjusted exposure used for sector and concentration weighting. Premium-paid options below 1% of portfolio: ignored. Structured/leveraged option positions above 5%: critical red flag.
* **Margin / Negative Cash:** Critical red flag for all five frameworks. Triggers 50% score cap across all frameworks regardless of size.
* **Extreme Concentration (Score Caps):**
  - 25–50% single holding: 70% score cap
  - 50–70% single holding: 55% score cap
  - Greater than 70% single holding: 40% score cap
* **All-Cash Portfolio:** Triggers Buffett 50% cap (no productive assets), Dalio 60% cap (no diversification), Marks no cap (cash-as-optionality is consistent with late-cycle posture). Dimon and Blanchard scored normally.
* **Crypto:** Treated as Tier 4 liquidity (24/7 markets but volatile, custody-dependent). >5% crypto = Buffett moderate red flag, Dimon moderate red flag, Blanchard neutral, Dalio neutral, Marks neutral. >15% crypto = critical red flag for Buffett and Dimon.
* **Direct Real Estate:** Classified as Tier 5 (illiquid). >40% of net worth in direct real estate = critical red flag for all frameworks (concentration). Operating real estate (rental income) treated separately from primary residence.
* **Private Business:** Classified as Tier 5 (illiquid). Operating business ownership treated as quality equity exposure for Buffett (potentially green flag if moat-bearing) but as concentration risk for all others above 25% of net worth.
* **Inherited Concentrated Position:** Score cap from concentration applies, but recommendation framing acknowledges tax-cost basis lock-in.

---

*Sections 17 through 25 (framework scoring thresholds, current theses, consensus signals, watch list, scoring algorithm, benchmark portfolios) carry forward from prior version 2026-05-08a without modification at this refresh. No framework allocation changes, no scoring algorithm changes, no benchmark portfolio changes.*

*End of Portfolio Alignment Criteria File. Generated 2026-05-27.*
