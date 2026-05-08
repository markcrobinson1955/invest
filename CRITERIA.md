# Portfolio Alignment Criteria File

*Version: 2026-05-08a*

*Last full refresh: 2026-05-08*

*Next scheduled refresh: 2026-06-08*

---

## SECTION 2 — CHANGE LOG

| Date | Version | Description of Changes |
| :--- | :--- | :--- |
| 2026-04-25 | 2026-04-25b | Section count expanded 24 → 25. Added benchmark portfolios. Section 9 expanded to 5 named scenarios. Section 16 expanded to 9 edge cases. Section 24 added explicit scoring math placeholder. |
| 2026-05-07 | 2026-05-07a | Updated April 29 FOMC: held 3.50–3.75% (8-4 vote, most dissents since 1992); Powell announced he stays on Board after May 15; Warsh confirmation pending. Updated market levels to May 6 close: S&P 7,365 record. Iran peace deal advanced May 6 (Axios). Resolved Watch List items: April 28-29 FOMC, Berkshire Annual Meeting May 2, Section 301 hearings. |
| 2026-05-08 | 2026-05-08a | Major v3 restructure to support analyzer 2026-05-08a. **Added real-allocator backing per framework in Section 5** — each of the five expert personas now references named published research from real institutional allocators (Swensen, AQR, Ilmanen, Arnott, Asness) that informs the constructed-translation. **Pinned scoring algorithm in Section 24** — replaced "proportional to match quality" with explicit deduction formula: per-category score = max(0, 10 − 0.5 × deviation_pp). **Cut Climate and Demographics subsections from Section 4** (low decision-utility per refresh, kept in Watch List where relevant). **Trimmed Watch List from 19 to 10 items** — kept only items with measurable triggers and high impact. **Trimmed Consensus Signals from 14 to 8 rows** — kept only highest-confidence signals (4+ frameworks agreeing, or clear divergence). **Trimmed change log** to last 3 entries (full history available in git). Section count unchanged at 25; Section 4 subsection count reduced from 16 to 14 (Climate and Demographics removed). |

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
*Last updated: 2026-05-08* | *Confidence: High*
* **National Debt:** $39.0+ trillion as of early May (Treasury Debt to the Penny, May 5).
* **Deficit:** FY2026 cumulative deficit reached $1.2 trillion at end of March (BPC). Net interest costs projected at $1.0 trillion FY2026, on track to exceed defense spending.
* **Treasury Auctions:** Bid-to-cover ratios remain weak; primary dealer take-up of late-March 2-year auction at 24% (twice normal). 10-year yield rose to 4.37% on May 6 (highest since July 2025) before retracing on Iran peace news.
* **Interest Burden:** Average interest rate on total marketable debt 3.365% (March, carry forward). Net interest as share of outlays projected at 13.95% FY2026 (CBO).
* **Maturity:** ~33% of publicly held marketable debt matures within 12 months; average maturity 70 months.

### Trade and Geopolitics
*Last updated: 2026-05-08* | *Confidence: High*
* **Tariff Authority — SCOTUS Ruling:** Feb 20, 2026 *Learning Resources v. Trump* 6-3 decision held IEEPA does not authorize tariff imposition. ~$166B in IEEPA tariffs being refunded via new CBP CAPE system.
* **Section 122 Tariffs:** 10% baseline since Feb 24, 2026; **Bessent announced March 4 increase to 15%** (effective date and country list pending). Average effective US tariff rate ~11% (Yale Budget Lab April 2). Section 122 expires July 24, 2026 absent extension.
* **CIT Litigation:** 24-state lawsuit and Burlap and Barrel v. Trump consolidated; oral arguments held April 10 before three-judge panel. **Ruling pending.**
* **Section 301:** USTR launched investigations covering 60 economies on forced labor (March 11) and 16 economies on excess capacity (March 12). ITC hearings April 28 and May 5; preliminary findings pending.
* **Iran Conflict — Peace Deal Progressing:** US-Israeli war that began Feb 28, 2026 shows signs of de-escalation. **May 6: Axios reported White House close to one-page MOU with Iran on ending the war, including nuclear enrichment moratorium.** Trump indicated agreement "not certain." Strait of Hormuz traffic resuming with US military escort. Markets repricing on peace optimism: oil down 11% from peak, yields backing off post-spike, equities at records. Ceasefire architecture remains fragile.
* **Strait of Hormuz Status:** Traffic resuming under US military escort. Iran briefly attacked US-flagged vessels and UAE infrastructure in early May before May 6 peace progression. Rystad estimates oil flows reach 90% of pre-war levels by July.

### Private Credit Stress
*Last updated: 2026-05-08* | *Confidence: High*
* **Moody's BDC Outlook:** Negative since April 7, 2026 — liquidity mismatches, elevated leverage, AI as "disruptive force."
* **Q1 2026 Redemption Wave:** Aggregate redemption requests across non-traded BDCs ~$20B; ~53% fulfilled, most funds invoking 5–7% caps. Blue Owl publicly traded fund reported declining income/asset values in early May filings; Blue Owl stock down >33% YTD.
* **Specific Funds:** Blue Owl OCIC (~$36B): 21.9% requests, 5% cap. Blue Owl OTIC (~$6B): 40.7% requests, 5% cap. Apollo Debt Solutions: 11.2% requests, ~45% fulfilled. Morgan Stanley North Haven: 5% cap.
* **Defaults:** Direct lending default rate ~5.6% (Morgan Stanley); potential to reach 8% — well above 2–2.5% historical average. PIK toggle usage rising in software/SaaS.
* **Marks Memo:** April 9 "What's Going On in Private Credit" — direct lending facing first major test since 2008; structural liability-side risk from retail investor base.

### Regulatory Watch
*Last updated: 2026-05-08* | *Confidence: Medium-High*
* **Fed Chair Transition:** Powell announced April 29 he will remain on Board of Governors after May 15, "until convinced the administration's criminal investigation is over." Governor term expires January 2028. **Kevin Warsh approved by Senate Banking April 29 (party line); full Senate vote expected week of May 11.** Warsh likely to chair June 16-17 FOMC. He has publicly indicated openness to cutting rates and proposed limits on forward guidance.
* **April 29 FOMC:** Held federal funds rate at 3.50–3.75% (third consecutive hold). Vote 8-4 — most dissents since 1992. Miran dissented for 25bp cut; Bowman, Schmid, and one other against easing-bias language. Markets pricing zero rate movements through end-2026 and one 25bp cut December 2027.
* **DOJ — Powell:** Department of Justice ended its criminal investigation into Powell on April 24, 2026.
* **Crypto/Stablecoin:** Stablecoin Transparency Act remains in Senate committee.
* **Banking — Basel 3 Endgame:** Reduced severity vs 2023 version per Dimon Q1 2026 commentary. Final implementation delayed to late 2026.

### AI Capital Expenditure
*Last updated: 2026-05-08* | *Confidence: Medium*
* **Hyperscaler Capex:** MSFT, GOOGL, META, AMZN combined FY2026 capex in $400B+ range [verify]. Aggregate AI capex commitment across sector ~$725B for 2026.
* **AI Mega-Cap Leadership:** May 6 session: Nvidia +5.5%, AMD +17.77% on earnings beat, Supermicro +24.5%, Apple set first all-time closing high of 2026. Top 7 mega-caps approximately 38%+ of S&P 500 market cap.
* **Bubble concern:** Marks's December 2025 memo "Is It a Bubble?" addressed AI parallels to prior bubbles. Dalio February-March commentary connected AI investment cycle to broader Big Cycle/capital war thesis.

### Inflation Trajectory
*Last updated: 2026-05-08* | *Confidence: High*
* **Headline CPI:** 3.3% YoY March 2026 (BLS, April 10), up from 2.4% February. Largest monthly increase (+0.9% MoM) since June 2022. **April CPI scheduled May 12.**
* **Core CPI:** 2.6% YoY March, +0.2% MoM. Underlying inflation contained.
* **Core PCE:** 3.0% YoY February (US Bank); March/April pending.
* **Drivers:** Iran war energy shock — gasoline +21.2% MoM March, energy index +10.9%. Oil prices rose >76% February-early April. May 6 peace deal news caused sharp oil pullback; April CPI may show peak energy contribution.
* **Fed Outlook:** Federal funds target 3.50–3.75% (held April 29). FOMC statement upgraded language: inflation "is elevated" (was "remains somewhat elevated"). Middle East "contributing to a high level of uncertainty."
* **Consumer Sentiment:** University of Michigan final April reading 49.8 — lowest in series history (since 1952), surpassing June 2022 pandemic-era low.

### Labor Market
*Last updated: 2026-05-08* | *Confidence: High*
* **Unemployment:** 4.3% March 2026 (BLS April 3). **April Employment Report scheduled May 8** — consensus +55-65K, unemployment 4.3% steady.
* **Payrolls:** +178K March (vs −133K Feb revised); rolling 3-month average +68K.
* **JOLTS:** 6.9 million openings February; quits rate 1.9%; hires 4.8M.
* **Participation:** 61.9% (lowest since November 2021); U-6 8.0%.
* **Wages:** Average hourly earnings +0.2% MoM, +3.5% YoY (lowest annual since May 2021).

### Market Performance YTD
*Last updated: 2026-05-08* | *Confidence: High*
* **S&P 500:** 7,365.12 record close (May 6).
* **Nasdaq:** 25,838.94 record close (May 6).
* **Dow:** 49,910.59 (May 6).
* **Russell 2000:** 2,888.24 record (May 6).
* **VIX:** 17.30 (May 6).
* **Crude Oil:** WTI $91-95/bbl, down sharply (-7%) on Iran peace progression news.
* **MSCI EAFE YTD:** +6.1% [verify]; **MSCI EM YTD:** +10.4% [verify].
* **10-Year Treasury Yield:** 4.37% (May 6, FRED); 30-year briefly topped 5%.
* **Forward P/E:** ~20.4 [verify] (S&P 7,365 vs forward EPS estimate); above 5-year (19.9) and 10-year (18.9) averages.

### Dollar and Reserve Currency
*Last updated: 2026-05-08* | *Confidence: High*
* **DXY:** ~97.8 close May 6, weakening on peace deal hopes from 98.51.
* **Gold:** $4,752.84/oz spot May 7 (JM Bullion); LBMA May 5 reference $4,576-$4,636. Reached record $5,602 January 28. State Street Monthly Gold Monitor cites $4,000–4,750 structural floor.
* **Central Bank Buying:** Continued heavy purchasing from China (~2,309t official reserves), India, Turkey.

### China and Emerging Markets
*Last updated: 2026-05-08* | *Confidence: Medium*
* **China GDP:** ~4.6% annualized; property sector workouts ongoing.
* **India:** MSCI India outperforming EM peers; Modi-Trump tariff deal lowering rates 25% → 18% conditional on India halting Russian oil purchases.

### Europe and Japan
*Last updated: 2026-05-08* | *Confidence: Medium*
* **Japan:** BOJ ended NIRP; Yen volatility around 152-157 with Tokyo intervention to prop up yen reported around May 1 after breaching 160.
* **Europe:** ECB on hold at 2.00% deposit rate; markets pricing 1-2 ECB hikes 2026 [verify]. Germany debt brake remains contentious.

### Housing and Commercial Real Estate
*Last updated: 2026-05-08* | *Confidence: Medium*
* **Residential:** Transaction volumes ~20% below 5-year average; mortgage rate ~6.30% [verify].
* **Office CRE:** ~20% Tier 1 vacancy; regional banks increasing 2026 maturity loan-loss provisions.

### Cryptocurrency and Digital Assets
*Last updated: 2026-05-08* | *Confidence: Medium-High*
* **Bitcoin:** $81,267 (May 6 close); rallied $1,415-$1,504 on May 6 session on Iran peace deal optimism.
* **Stablecoin Market Cap:** Continued growth; legislation pending.

### Earnings Yield vs Credit Yield Snapshot
*Last updated: 2026-05-08* | *Confidence: Medium-High*
* **S&P 500 Forward Earnings Yield:** ~4.90% [verify] (1 / ~20.4 forward P/E from FactSet at S&P 7,365 close May 6).
* **US Investment-Grade Yield:** ~5.05% [verify] (FRED ICE BofA April 23 carry forward).
* **US High-Yield Yield:** ~6.85% [verify] (FRED ICE BofA April 23 carry forward).
* **Spread (Earnings Yield − IG Yield):** ~−0.15%.
* **Assessment:** Credit continues to offer slightly higher yield than equity on forward-looking basis. Negative spread continues to favor the **Marks** framework (credit > equity in late-cycle posture).

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

* **Current Regime:** Inflationary regime with stagflation risk **and transitional uncertainty** — Iran peace deal progression May 6 may unwind active war regime if it materializes. Energy shock from Iran war drove headline CPI to 3.3% in March; April release pending May 12. Equity at record highs while VIX moderately elevated and gold at structural-high $4,752 signals continued regime stress. UMich consumer sentiment at all-time low (49.8) while indices at records signals classic late-cycle divergence. FOMC 4-dissent split April 29 signals end of consensus period.
* **Primary Risk Scenario:** Stagflation if peace deal fails / sustained Hormuz disruption returns; reflation if peace materializes and oil resets lower.
* **Best Suited:** **Dalio** (gold/commodity/diversification) and **Blanchard** (fiscal-stress hedge with TIPS and international).
* **Least Suited:** **Buffett** (concentrated US equity exposure at record valuations carries elevated drawdown risk in stagflation; Forward P/E ~20.4 well above 10-year average).
* **Justification:** March 2026 CPI energy-led spike to 3.3%, gold at $4,752 (record territory), VIX at 17.30, $39T+ debt with weak Treasury auctions, UMich sentiment at all-time low, Powell-to-Warsh transition, and Iran war (with conditional peace progression) together signal active inflationary regime with stagflation risk and fiscal-dominance pressure.

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
- *Relevance to 2026:* **High** — March CPI energy shock to 3.3%, Iran war disruption, Section 122 tariffs adding to consumer prices.

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
- *Relevance to 2026:* **Medium-High** — Moody's BDC negative outlook, $20B redemption surge with only 53% fulfilled, Marks April 9 memo.
- Apply post-gate stress tier reclassification per Section 7.

**Scenario 3 — Extended Stagflation (1970s Replay)**
Trigger: growth stalls while inflation stays high for years; supply shock plus fiscal expansion.
- US Equities: −20% to −35% (real terms)
- Long-duration Bonds: −25% to −40%
- TIPS: 0% to +10%
- Commodities: +40% to +80%
- Gold: +50% to +150%
- International Equities: mixed; commodity exporters outperform
- *Relevance to 2026:* **High** — energy shock + slowing growth (3-month payroll average +68K) + fiscal expansion is textbook stagflation; consumer sentiment at all-time low while equities at records signals classic late-cycle divergence.

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
- *Relevance to 2026:* **Medium** probability, high consequence — $39T+ debt; primary dealer take-up at 24% on late-March 2-year auction; ~33% of marketable debt rolling within 12 months at elevated rates; 30-year yield briefly topped 5% in early May.

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

*Items carry [verify] tags inline; this list must match exactly.*

* [verify] Hyperscaler combined FY2026 capex $400B+ — Section 4 AI Capital Expenditure
* [verify] ECB rate path market expectation (1-2 hikes 2026) — Section 4 Europe and Japan
* [verify] MSCI EAFE YTD +6.1% and MSCI EM YTD +10.4% — Section 4 Market Performance YTD
* [verify] Forward P/E ~20.4 — Section 4 Market Performance YTD
* [verify] US IG Yield ~5.05% — Section 4 Earnings Yield vs Credit Yield
* [verify] US HY Yield ~6.85% — Section 4 Earnings Yield vs Credit Yield
* [verify] Mortgage rate ~6.30% — Section 4 Housing and CRE

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
* **Margin / Negative Cash:** Critical red flag for all five frameworks. Triggers 50% score cap regardless of size.
* **Extreme Concentration (Score Caps):**
    * 25–50% single holding: **70% score cap**
    * 50–70%: **55% score cap**
    * Greater than 70%: **40% score cap**
* **All-Cash Portfolio:** Buffett 50% cap (no productive assets), Dalio 60% cap (no diversification), Marks no cap (cash-as-optionality consistent with late-cycle posture). Dimon and Blanchard scored normally.
* **Crypto:** Tier 4 liquidity. >5% crypto = Buffett moderate red flag, Dimon moderate red flag. >15% crypto = critical red flag for Buffett and Dimon.
* **Direct Real Estate:** Tier 5. >40% of net worth = critical red flag for all frameworks (concentration). Operating real estate (rental income) treated separately from primary residence.
* **Private Business:** Tier 5. Operating business ownership treated as quality equity exposure for Buffett (potentially green flag if moat-bearing) but as concentration risk for all other frameworks if >30% of net worth.
* **Pension / Annuity:** Bond-Equivalent (Sovereign IG duration-matched to expected payout horizon). Defined benefit pension and Social Security counted in fixed income allocation for risk parity purposes.

---

## SECTION 17 — FRAMEWORK 1: RAY DALIO

*Source: Bridgewater Daily Observations; Fortune commentary March 14, 2026; World Governments Summit Dubai February 2-5, 2026; HBR IdeaCast January 20, 2026; All-In Podcast appearance March 19, 2026. Allocator backing: AQR research (Asness/Frazzini/Pedersen on risk parity); Bridgewater All Weather methodology.*

*Confidence: High.*

* **Who He Is:** Founder of Bridgewater Associates.
* **Optimal hold period:** 5–20 years (multi-cycle framework).
* **Bridgewater AUM:** ~$100B–$150B [verify] [last verified 2026-04-25].
* **Investment Philosophy:** Risk parity. Diversification across "four seasons" of growth and inflation.
* **Target Allocation (System-Constructed Translation, backed by AQR risk-parity research):** 30% Stocks, 40% Long-Term Treasuries, 15% Intermediate Treasuries, 7.5% Gold, 7.5% Commodities.
* **Current Thesis (2026):** Late stages of Big Debt Cycle. February 2 Dubai speech framed dynamics as approaching "capital war" stage. March 14 Fortune commentary placed US in transition from Stage 5 to Stage 6 ("the war stage"). Recommends gold (10–15%) as primary fiscal-dominance hedge. Warns abundant capital fueling AI build-out could dry up if foreign Treasury demand falters.
* **Recent Commentary:** "Cash is no longer trash, but debt is a risky hold" (early 2026). "We are on the brink. That means not in, but it means we are quite close" (Feb 4, World Governments Summit Dubai).
* **Red Flags:**
    * Dollar over-reliance (>80%) — Moderate
    * No gold allocation — Moderate
    * No commodity allocation — Minor
    * Heavy long-bond concentration without inflation hedge — Critical
* **Green Flags:**
    * Gold/hard asset allocation 7.5%+
    * Balanced risk-parity construction
    * Material non-USD exposure
    * Inflation-linked bonds present

---

## SECTION 18 — FRAMEWORK 2: JAMIE DIMON

*Source: JPMorgan Chase 2025 Annual Report (Letter to Shareholders, April 6, 2026); JPM Q1 2026 8-K April 14, 2026; JPM 2026 proxy April 2, 2026. Allocator backing: JPMorgan Asset Management Multi-Asset Solutions research; AQR quality-factor research (Asness/Frazzini/Pedersen QMJ).*

*Confidence: High.*

* **Who He Is:** Chairman and CEO of JPMorgan Chase.
* **Optimal hold period:** 3–7 years (cycle-aware quality compounding).
* **JPMorgan Assets:** ~$4.3T [last verified 2026-04-25]. 2025 full-year results: managed revenue $185.6B, net income $57.0B, ROE 17%, ROTCE 20%. Q1 2026 net income $16.5B, EPS $5.94, revenue $50.5B (+10% YoY).
* **Investment Philosophy:** "Fortress Balance Sheet" — high capital ratios, massive liquidity, preparation for tail risks.
* **Target Allocation (System-Constructed Translation, backed by JPMAM and AQR quality research):** 50% High-Quality US Equities, 30% Cash/Short-duration High-Quality Debt, 20% Alternative/Strategic Credit.
* **Current Thesis (2026):** April 6 letter framed "increasingly complex set of risks": geopolitical conflicts, persistent inflation risk, AI-related uncertainty, large global fiscal deficits, elevated asset prices. Warned drawn-out Iran war could push energy/commodity prices higher in ways markets have not fully priced — producing "stickier inflation and ultimately higher interest rates." Q1 2026 markets revenue record $11.6B; fixed income trading +21% on commodities/credit/FX/EM.
* **Recent Commentary:** "The outcome of current geopolitical events may very well be the defining factor in how the future global economic order unfolds" (April 6 letter).
* **Red Flags:**
    * Private Credit >15% — Critical
    * Margin debt — Critical
    * Tier 5 gated holdings — Moderate
    * Cash/T-bills <20% — Moderate
* **Green Flags:**
    * Cash/T-bills >25%
    * Quality US large-cap equity core
    * Minimal leverage
    * Liquid alternatives capped <10%

---

## SECTION 19 — FRAMEWORK 3: WARREN BUFFETT

*Source: Berkshire Hathaway Q4 2025 10-K; Q4 2025 13F filing (Buffett's final quarter); Berkshire 2026 proxy March 13, 2026; Morningstar Berkshire 2026 Annual Meeting recap May 3, 2026. Allocator backing: David Swensen Yale endowment model; academic literature on long-horizon factor premiums.*

*Confidence: High.*

* **Who He Is:** Former Chairman/CEO of Berkshire Hathaway. As of January 1, 2026, **Greg Abel is CEO**; Ted Weschler manages investment portfolio. Buffett continues as Chairman of the Board.
* **Optimal hold period:** 20+ years ("favorite holding period is forever").
* **Berkshire Cash Position:** ~$400B at meeting reference (May 2, 2026). Plus ~$300B in securities.
* **Investment Philosophy:** Value investing. High-conviction concentration in "moat" businesses at reasonable prices.
* **Target Allocation (System-Constructed Translation, backed by Swensen long-horizon framework):** 90% Low-cost S&P 500 Index, 10% Short-term Treasuries (for individuals).
* **Annual Meeting May 2, 2026 — First Abel-led:**
    * Theme: "The Legacy Continues."
    * Abel **explicitly ruled out break-up**: "Absolutely not. We see our conglomerate structure working."
    * Abel on cash deployment: "We're not anxious to deploy capital into subpar opportunities."
    * AI cybersecurity flagged as significant risk; "not going to do AI for the sake of AI."
    * Buffett: "Greg is doing everything I did and then some."
* **Current Thesis (2026):** Continuity-first under Abel. Iran war-driven March selloff and elevated valuations did not produce Buffett-criteria opportunities sufficient to deploy meaningful cash. No major capital deployment announced at meeting.
* **Red Flags:**
    * Crypto >5% (Buffett historically negative) — Moderate
    * Margin — Critical
    * >20 distinct equity holdings (Buffett prefers concentration) — Minor
    * Gold >5% (Buffett dislikes non-productive assets) — Moderate
* **Green Flags:**
    * S&P 500 index core or concentrated US large-cap
    * Cash/T-bills 20–30%
    * Demonstrated moat businesses
    * Minimal turnover

---

## SECTION 20 — FRAMEWORK 4: OLIVIER BLANCHARD

*Source: PIIE event page (Future Economic Architecture of the Eurozone panel, mid-April 2026); PIIE Briefings (Karen Dynan and David Wilcox eds., February 2026); Blanchard "Why Low Interest Rates Force Us to Revisit Scope and Role of Fiscal Policy" (April 2025). Allocator backing: Antti Ilmanen (AQR) regime-aware allocation research; Rob Arnott (Research Affiliates) inflation-resilient portfolio work.*

*Confidence: Medium.*

* **Who He Is:** Senior Fellow at PIIE; Robert M. Solow Professor of Economics emeritus at MIT; former Chief Economist of the IMF (2008–2015).
* **Optimal hold period:** 5–15 years (fiscal-stress hedge over policy/cycle horizon).
* **Investment Philosophy:** Academic, not allocator. Focuses on fiscal sustainability and the relationship between r (interest rate) and g (growth rate).
* **Target Allocation (Fiscal Stress Resilience, backed by Ilmanen regime-aware framework and Arnott inflation-resilient research):** 40% TIPS, 30% International Equities (Non-USD), 20% Short-duration Bonds, 10% Real Assets.
* **Current Thesis (2026):** Continued focus on fiscal sustainability when r > g, with US trajectory increasingly explosive without primary surplus. April 2026 PIIE eurozone panel addressed how rising long-term defense commitments and industrial policy expose fiscal architecture weaknesses. Current macro environment (energy-driven CPI spike, weak auctions, fiscal trajectory deteriorating, 30-year yield briefly above 5%) increasingly aligned with Blanchard's hedging thesis.
* **Recent Commentary:** Recent academic emphasis on scope and role of fiscal policy under low (and rising) rate regimes; April 2026 eurozone panel commentary on integration and ECB framework.
* **Red Flags:**
    * No TIPS allocation — Critical
    * Dollar over-reliance (>75%) — Moderate
    * High duration without inflation protection — Moderate
    * No international equity exposure — Moderate
* **Green Flags:**
    * TIPS allocation 15%+
    * Material non-USD international equities 25%+
    * Real assets allocation 10%+
    * Short-duration bond bias

---

## SECTION 21 — FRAMEWORK 5: HOWARD MARKS

*Source: Oaktree memo "What's Going On in Private Credit" (April 9, 2026); memo "Is It a Bubble?" (December 2025); Oaktree Conference 2026 podcast (March 24, 2026). Allocator backing: Oaktree's own published memos (Marks's primary output); Asness time-series momentum research applied to credit cycles.*

*Confidence: High.*

* **Who He Is:** Co-founder and Co-Chairman of Oaktree Capital Management.
* **Optimal hold period:** 2–5 years (cycle-aware tactical credit).
* **Oaktree AUM:** ~$223B [last verified 2026-04-25].
* **Investment Philosophy:** "Sea Change" — moving from 40-year period of declining rates to a normal rate environment where credit offers equity-like returns with less risk.
* **Target Allocation Bias (Cycle-Aware Credit, backed by Oaktree memos and Asness credit-cycle research):** Overweight Credit (Distressed, Senior Secured) relative to Equities; specific weighting depends on cycle stage assessment.
* **Current Thesis (2026):** April 9 memo "What's Going On in Private Credit" outlined growing concerns about retail private credit. Marks distinguishes direct lending (under stress) from broader private credit, emphasizes liability-side risk: retail/mass-affluent investor base structurally different from institutional capital, may behave differently under stress. Sea Change thesis intact: credit can deliver equity-like returns with less risk in current rate environment. Refresh evidence: Moody's BDC negative outlook, $20B Q1 redemption surge with ~53% fulfilled, Blue Owl public fund declining income/asset values.
* **Recent Commentary:** April 9 memo: financial cycles follow predictable patterns; sub-investment grade yield premium "isn't a freebie, but rather compensation for bearing credit risk."
* **Red Flags:**
    * Covenant-lite private credit concentration — Critical
    * Software/SaaS debt concentration — Moderate
    * Retail private credit BDCs exceeding 10% — Critical
    * No credit allocation in late-cycle posture — Moderate
* **Green Flags:**
    * Senior secured credit allocation
    * Distressed/opportunistic credit exposure
    * Credit overweight relative to equities in current cycle assessment
    * Minimal direct lending exposure to software/SaaS

---

## SECTION 22 — CONSENSUS SIGNALS

*Trimmed to 8 highest-confidence signals (4+ frameworks agreeing or clear divergence).*

| Signal | Dalio | Dimon | Buffett | Blanchard | Marks |
| :--- | :--- | :--- | :--- | :--- | :--- |
| Hold significant cash / T-bills | ✓ | ✓ | ✓ | ✓ | ✓ |
| Warning on private credit | ✓ | ✓ | ✓ | ✓ | ✓ |
| Quality over yield | ✓ | ✓ | ✓ | ✓ | ✓ |
| Avoid leverage / complexity | ✓ | ✓ | ✓ | ✓ | ✓ |
| US fiscal sustainability concern | ✓ | ✓ | ⚠ | ✓ | ✓ |
| AI / tech bubble concern | ✓ | ✓ | ✓ | — | ✓ |
| International diversification | ✓ | ✓ | ✓ | ✓ | — |
| Warning on long-duration bonds | ✓ | ✓ | — | ✓ | ✓ |

Legend: ✓ = recommends / warns in alignment; ⚠ = warns against or diverges; — = not a primary view.

*Last updated: 2026-05-08*

* **Highest-confidence signals (5/5 unanimous):** Hold significant cash/T-bills (reinforced by Berkshire ~$400B); Warning on private credit (intensified by Blue Owl); Quality over yield; Avoid leverage/complexity.
* **No cell-level changes this refresh.**

---

## SECTION 23 — CURRENT EVENTS WATCH LIST

*Trimmed to 10 items with measurable triggers and high impact.*

1. **April CPI Release May 12, 2026** — Immediate watch — Headline >3.5% YoY triggers stagflation regime reassessment; core >3.0% YoY triggers Fed reaction function reassessment.

2. **April Employment Report May 8, 2026** — Immediate watch — Payrolls below +30K triggers labor market deterioration concern; unemployment >4.5% triggers stagflation scenario probability bump.

3. **US-Iran Peace Deal Progression** — Immediate watch — Formal MOU signing triggers regime reassessment toward reflation; collapse triggers stagflation re-escalation.

4. **Kevin Warsh Senate Confirmation Vote (week of May 11)** — Regulatory watch — Confirmation triggers reassessment of Fed reaction function; rejection or withdrawal triggers Watch List re-prioritization.

5. **CIT Ruling on Section 122 Lawsuits** — Regulatory watch — Ruling pending since April 10. Ruling that strikes Section 122 triggers refund analysis and successor-tariff reassessment.

6. **Section 122 Tariff Expiration July 24, 2026** — Regulatory watch — Lapse without replacement reduces effective tariff rate from ~11% to ~8%; extension or replacement under Section 301 triggers macro reassessment.

7. **Berkshire Q1 2026 13F Filing (mid-May)** — Criteria refresh — First filing under Abel/Weschler primary control. Material deployment >$25B triggers Buffett framework redefinition review.

8. **June 16-17 FOMC Meeting** — Criteria refresh — First Warsh-chaired meeting; rate decision plus SEP/dot-plot revisions trigger Fed reaction function reassessment.

9. **Howard Marks Next Memo / Oaktree Q2 Conference** — Criteria refresh — Cycle-stage update; whether direct-lending stress widens to broader credit (HY OAS >500bp would be a trigger).

10. **CRE Refinancing Pulse Q2 2026** — Criteria refresh — Regional bank delinquency rate >5% triggers banking stress flag; multi-family/office reserve increase >20% QoQ at JPM peers triggers reassessment.

---

## SECTION 24 — SCORING THRESHOLDS (PINNED ALGORITHM)

**Framework Weights:**
* Simple average: Dalio 20%, Dimon 20%, Buffett 20%, Blanchard 20%, Marks 20%
* Regime-weighted average: 2x weight on regime-aligned frameworks per Section 5

**Pinned Scoring Algorithm (per-framework, 0–100 scale):**

The score is computed as the sum of three components, then capped:

**Component 1 — Allocation Match (0–50 points):**

For each target allocation category in the framework's published targets:
- deviation_pp = |actual_percent − target_percent|
- category_score = max(0, 10 − 0.5 × deviation_pp)
- category_score is capped at 10

Sum the category scores. Then normalize to 50:
- allocation_match_score = (sum_of_category_scores / max_possible_sum) × 50

Where max_possible_sum = number_of_categories × 10.

Worked example for Dalio (5 categories):
- Targets: 30/40/15/7.5/7.5 (Stocks, LT Treasuries, Int Treasuries, Gold, Commodities)
- Portfolio actuals: 60/30/0/0/0
- Deviations: 30, 10, 15, 7.5, 7.5
- Category scores: 0, 5, 2.5, 6.25, 6.25
- Sum: 20
- Max possible: 50
- allocation_match_score = (20 / 50) × 50 = 20 points

**Component 2 — Green Flags (0–25 points):**

Each framework lists 4 green flags. Each green flag present awards 6.25 points (4 × 6.25 = 25).

Partial credit allowed for threshold-based flags:
- Example: flag is "Cash/T-bills 25%+"; portfolio has 20%
- Partial score: (20 / 25) × 6.25 = 5.0 points
- Cap any single flag at 6.25 points

**Component 3 — Red Flag Component (0–25 points):**

Start at 25 points. Apply deductions:
- Minor red flag: −2 points
- Moderate red flag: −5 points
- Critical red flag: −10 points AND apply 50% framework score cap

Floor at 0 points for this component.

**Total Raw Score:** sum of three components. Floor 0, ceiling 100.

**Apply Caps (lowest cap wins):**

- Critical Red Flag: 50% cap
- Horizon mismatch: graduated 75% / 65% / 55% per Section 6
- Single Holding >25%: graduated 70% / 55% / 40% per Section 16
- Margin / negative cash: 50% cap across all frameworks
- All-cash: 50% Buffett, 60% Dalio (Marks no cap; Dimon and Blanchard normal)

When multiple caps apply: name all in Section 2 narrative; state which cap won.

**Score Bands:**
* Strong: 80–100
* Moderate: 60–79
* Partial: 40–59
* Weak: 20–39
* Anti-Aligned: 0–19

---

## SECTION 25 — BENCHMARK PORTFOLIOS

*Reference portfolios used by analyzer STEP 5.3 for context. Static; do not modify per refresh.*

**Benchmark 1 — Simple 60/40**
- 60% US Equity (broad market index)
- 40% US Aggregate Bond Index (intermediate duration, IG quality)
- Currency: 100% USD
- Liquidity: 100% Tier 1–2

**Benchmark 2 — Bridgewater All Weather (translation)**
- 30% US Equities
- 40% Long-term Treasuries
- 15% Intermediate Treasuries
- 7.5% Gold
- 7.5% Commodities
- Currency: ~85% USD
- Liquidity: 100% Tier 1–2

**Analyzer use:** Score both benchmarks against all five frameworks. Reference results in Section 2 narrative where they add context.

---

*End of Portfolio Alignment Criteria File. Generated 2026-05-08.*
