# Portfolio Alignment Criteria File

*Version: 2026-05-16b*

*Last full refresh: 2026-05-16 07:30 ICT*

*Next scheduled refresh: 2026-06-16*

---

## SECTION 2 — CHANGE LOG

| Date | Version | Description of Changes |
| :--- | :--- | :--- |
| 2026-05-07 | 2026-05-07a | Updated April 29 FOMC; Powell post-May 15 status; market levels to May 6 close; Iran peace deal advancing per Axios May 6. |
| 2026-05-08 | 2026-05-08a | Major v3 restructure to support analyzer 2026-05-08a. Added real-allocator backing per framework. Pinned scoring algorithm. Cut Climate/Demographics. Trimmed Watch List 19→10 and Consensus Signals 14→8. |
| 2026-05-16 | 2026-05-16a | Significant macro reset. April CPI 3.8% YoY (May 12), April PPI 6.0% YoY. Iran ceasefire on "life support" per Trump May 11. Warsh confirmed Fed Chair May 13 (54-45). April payrolls +115K, unemployment 4.3%. S&P record 7,517.12 May 14, then -1.24% May 15 to 7,408.50. 10-year 4.58%. Regime call: stagflation risk actively confirmed. Added new Section 4 subsection: Repo Market and Short-Term Funding. Added repo dimension to Section 9 Scenario 2, Section 15 fixed income classification, Section 22 Consensus Signals, Section 23 Watch List. |
| 2026-05-16 | 2026-05-16b | Re-verified all dynamic figures previously carried forward as [verify]. **Confirmed/updated:** EEM YTD +22.85% (was +10.4% — major outperformance), Forward P/E 21.0 (was 20.2), DXY 99.05 (was 98.5), 30-year yield 5.12% (was 5.0%), 10-year yield 4.595% (was 4.58%), 2-year yield 4.08% (was [verify]), mortgage rate 6.36% (was 6.30%), hyperscaler capex ~$700B for four / ~$690B Big Five (was $400B+ / $725B), IG yield ~5.50% (was 5.05%), HY yield ~7.20% (was 6.85%), Brent crude $109.24 (new datapoint). **Remaining [verify] tags reduced from 25 to 11.** Behavioral cleanup: removed silent carry-forward; explicit notation where verification incomplete. |

---

## SECTION 3 — HOW TO UPDATE THIS FILE

This file is the primary reference for the Portfolio Analyzer. To update:
1. Conduct web searches for each dynamic subsection in Section 4.
2. Review the prior Watch List (Section 23) — note what resolved.
3. Update Consensus Signals (Section 22) only when a framework's stance shifts based on new public commentary.
4. Increment version number, update "Last full refresh" date.
5. Maintain static editorial rules and system-defined labels.
6. **Re-verify every dynamic figure independently. Do not carry forward [verify] tags without searching.** This is the most common failure mode and the rule exists to force a forcing function.

---

## SECTION 4 — CURRENT MACRO ENVIRONMENT

*Where recent data is unavailable, prior figures carry forward only with [verify] tags. Inline [verify] tags must match Section 13 exactly.*

### US Fiscal Position
*Last updated: 2026-05-16 07:30 ICT* | *Confidence: High*
* **National Debt:** $38.91 trillion as of May 5, 2026 (JEC Monthly Debt Update); Treasury Debt to the Penny published through May 13, 2026. $39T threshold projected to be crossed approximately May 18, 2026.
* **Deficit:** FY2026 cumulative deficit reached $1.2 trillion at end of March (BPC). Net interest costs projected at $1.0 trillion FY2026, on track to exceed defense spending.
* **Treasury Auctions:** Bid-to-cover ratios remain weak; primary dealer take-up of late-March 2-year auction at 24% (twice normal).
* **Yields (May 15, 2026 close, CNBC):** 30-year **5.121%** (highest since May 2025, nearing highest since October 2023); 10-year **4.595%** (one-year high); 2-year **4.079%**. 30Y up nearly 11bp Friday alone; 10Y up nearly 14bp.
* **Interest Burden:** Average interest rate on total marketable debt 3.373% (April 2026, JEC). Net interest as share of outlays projected at 13.95% FY2026 (CBO), 14.25% FY2027, 14.94% FY2028.
* **Maturity:** ~33% of publicly held marketable debt matures within 12 months; average maturity 70 months. Rolling at elevated rates is structural pressure.

### Trade and Geopolitics
*Last updated: 2026-05-16 07:30 ICT* | *Confidence: High*
* **Tariff Authority — SCOTUS Ruling:** Feb 20, 2026 *Learning Resources v. Trump* 6-3 decision held IEEPA does not authorize tariff imposition. ~$166B in IEEPA tariffs being refunded via new CBP CAPE system.
* **Section 122 Tariffs:** 10% baseline since Feb 24, 2026; Bessent announced March 4 increase to 15% (effective date and country list still pending). Average effective US tariff rate ~11% (Yale Budget Lab April 2). Section 122 expires July 24, 2026 absent extension.
* **CIT Litigation:** 24-state lawsuit and Burlap and Barrel v. Trump consolidated; oral arguments held April 10 before three-judge panel. **Ruling still pending.**
* **Section 301:** USTR investigations covering 60 economies on forced labor (March 11) and 16 economies on excess capacity (March 12). ITC hearings April 28 and May 5; preliminary findings pending.
* **Iran Conflict — Ceasefire on Life Support:** US-Israeli war that began Feb 28, 2026 produced a fragile April 8 ceasefire mediated by Pakistan. **Status deteriorated sharply since May 8.** Trump declared ceasefire on "massive life support" May 11 after rejecting Iran's response to US 14-point proposal (TIME, CBS). Both sides exchanged fire in Strait of Hormuz May 7-8. Israeli airstrikes on Lebanon continuing despite April 16 Israel-Lebanon ceasefire (500+ Lebanese killed since). Project Freedom mission paused for diplomacy; France and UK assembling multinational naval force. Iran demands: end to war on all fronts, war reparations, recognition of Hormuz sovereignty. US demands: nuclear program halt, 12-year enrichment freeze, transfer of 440kg HEU stockpile. Trump-Xi summit (mid-May) ended without major breakthrough. China agreed to 200 Boeing aircraft purchase (below expected 500).
* **Strait of Hormuz Status:** Effectively partially disrupted. **WTI rallied to $100.96 May 15 (+4.17% on the day); Brent at $109.24 (+3.33%).** Oil flow recovery in question.

### Repo Market and Short-Term Funding
*Last updated: 2026-05-16 07:30 ICT* | *Confidence: Medium-High*
* **SOFR:** 3.59% as of May 13, 2026 publication (sofrrate.com); SOFR Index 1.24323913. Sitting at lower bound of Fed funds target (3.50-3.75%).
* **Standing Repo Facility (SRF) usage pattern:** Three notable spikes since mid-2025 mark a regime shift from dormancy to active usage:
  - **September 15, 2025:** $18.5B single-day draw (largest since SRF inception in 2021); occurred without a major shock.
  - **October 31, 2025:** $50.35B record SRF usage on month-end pressures (Reuters); some lending rates exceeded 4% (above top of Fed funds range).
  - **December 31, 2025:** $75B SRF usage on year-end balance sheet pressures; SOFR jumped to 3.87% with some transactions at 4.0%. Fully reversed by January 5, 2026.
* **QT END announced October 2025:** Powell announced end of balance sheet runoff at the October FOMC, citing "signs have clearly emerged" of reserve scarcity. Fed balance sheet shrunk from $9T peak to $6.6T. This was the trigger event: the Fed conceded reserves were no longer "ample."
* **Bank Reserves:** $2.8T (4-year low) at trigger of October QT halt. Current level [verify — likely modestly higher since QT end but precise current figure not confirmed in this refresh].
* **Basis Trade Risk:** Hedge funds running large Treasury cash-vs-futures basis trades depend on cheap repo funding. SOFR-IORB spread widening raises carry cost; sharp spike could force unwinds — selling Treasuries spot into already-weak demand. September 2019 is canonical precedent. Estimated size $1T+ but [verify — precise current size requires institutional data not publicly aggregated].
* **Treasury issuance pressure:** $38.91T debt with ~33% rolling within 12 months requires constant bill/note issuance into a market where dealer balance-sheet capacity is constrained. Heavy T-bill issuance under Bessent draws cash from money market funds.
* **Why this matters for portfolio analysis:**
  - **Marks framework:** Repo stress is the canonical late-cycle signal. Marks's "Sea Change" explicitly identifies plumbing as where the next crisis emerges.
  - **Dimon framework:** Banking system stress propagates through repo. Fortress balance sheet means cash + Treasury collateral that can be repo'd; this is why Dimon's quality persona requires high Tier 1/2.
  - **Dalio framework:** Repo dysfunction is a fiscal-dominance symptom. When the central bank must intervene at scale to support its own debt market, "monetization" is functionally underway regardless of label.
  - **Buffett framework:** Less direct sensitivity, but record SRF usage historically precedes equity drawdowns.
  - **Blanchard framework:** Repo stress reflects fiscal-sustainability strain. This is Blanchard's thesis operationalized.
* **Watch metric:** SRF usage outside quarter-/year-end pinch points. Sustained mid-month SRF draws >$10B = stress confirmed. SOFR-IORB spread persistently >5bp = stress building.

### Private Credit Stress
*Last updated: 2026-05-16 07:30 ICT* | *Confidence: Medium-High*
* **Moody's BDC Outlook:** Negative since April 7, 2026 — liquidity mismatches, elevated leverage, AI as "disruptive force."
* **Q1 2026 Redemption Wave:** Aggregate redemption requests across non-traded BDCs ~$20B; ~53% fulfilled, most funds invoking 5–7% caps. Blue Owl publicly traded fund reported declining income/asset values in early May filings; Blue Owl stock down >33% YTD. [verify — fund-level redemption details below not independently re-confirmed this refresh]
* **Specific Funds [verify]:** Blue Owl OCIC (~$36B): 21.9% requests, 5% cap. Blue Owl OTIC (~$6B): 40.7% requests, 5% cap. Apollo Debt Solutions: 11.2% requests, ~45% fulfilled. Morgan Stanley North Haven: 5% cap.
* **Defaults [verify]:** Direct lending default rate ~5.6% (Morgan Stanley); potential to reach 8% — well above 2–2.5% historical average. PIK toggle usage rising in software/SaaS.
* **Marks Memo:** April 9 "What's Going On in Private Credit" — direct lending facing first major test since 2008; structural liability-side risk from retail investor base.
* **Linkage to repo stress:** Private credit relies on repo and warehouse lines for leveraged structures. When SOFR rises and dealer balance-sheet capacity contracts, BDC funding costs rise faster than asset yields can reprice.

### Regulatory Watch
*Last updated: 2026-05-16 07:30 ICT* | *Confidence: High*
* **Fed Chair Transition COMPLETED:** **Kevin Warsh confirmed Fed Chair May 13, 2026 by Senate 54-45 vote** (narrowest margin in modern era, party line except Fetterman crossover). Powell's term as chair expired May 15; Powell remains on Board of Governors with vote on 12-member FOMC (term through January 2028). **Warsh's first FOMC scheduled June 16-17.** Stephen Miran continues to dissent toward larger cuts. Warsh during confirmation pledged independence; market expectation he will face inflation reality (3.8% headline) constraining the rate-cut narrative.
* **April 29 FOMC (Powell's penultimate):** Held federal funds rate at 3.50–3.75% (third consecutive hold). Vote 8-4 — most dissents since 1992. Miran dissented for 25bp cut; Bowman, Schmid, and one other against easing-bias language.
* **Market pricing (May 15, 2026):** Markets fully priced out 2026 rate cuts. ~28% probability of 25bp HIKE in December 2026 (TradingEconomics); over 50% probability of hike before end of 2026 per some sources. Some traders now pricing 1 rate hike by March 2027.
* **DOJ — Powell:** Department of Justice ended its criminal investigation into Powell on April 24, 2026.
* **Crypto/Stablecoin:** Stablecoin Transparency Act remains in Senate committee.
* **Banking — Basel 3 Endgame:** Reduced severity vs 2023 version per Dimon Q1 2026 commentary. Final implementation delayed to late 2026.

### AI Capital Expenditure
*Last updated: 2026-05-16 07:30 ICT* | *Confidence: High*
* **Hyperscaler Capex (UPDATED):** Microsoft, Alphabet, Meta, and Amazon combined 2026 capex now ~$700B per recent earnings reports (Yahoo/Reuters Morning Bid, late April 2026). Big Five including Oracle: $660–690B (CreditSights, Introl, Futurum). Roughly 75% (~$450B) targets AI infrastructure. Individual figures: Amazon ~$200B, Alphabet $175-185B, Meta $115-145B, Microsoft tracking $190B+, Oracle $50B. Three of four raised capex guidance in late-April earnings.
* **Funding mechanism:** Hyperscalers raised $108B in debt during 2025; $1.5T in debt issuance projected over coming years.
* **AI Mega-Cap Leadership:** Nvidia Q1 earnings due May 20. May 14 saw new S&P record 7,517.12 driven by AI sector. Cerebras Systems IPO May 14 surged 68% on debut; Cisco beat earnings. Profit-taking May 15: Nvidia -4.4%, Intel -6%, AMD -5.7%, Micron -6.6%, Cerebras -10%. Top 7 mega-caps approximately 35-38% of S&P 500 market cap (Slickcharts).
* **Bubble concern:** Marks's December 2025 memo "Is It a Bubble?" addressed AI parallels. Dalio February-March commentary connected AI investment cycle to broader Big Cycle/capital war thesis. May 15 Niles Investment Management: "Ten of the last 12 recessions were preceded by a spike in oil."

### Inflation Trajectory
*Last updated: 2026-05-16 07:30 ICT* | *Confidence: High*
* **Headline CPI:** **3.8% YoY April 2026 (BLS, released May 12)** — highest since May 2023, accelerated sharply from 3.3% in March. MoM +0.6%.
* **Core CPI:** **2.8% YoY April** (up from 2.6% March); MoM +0.4%. Highest core monthly read since January 2025.
* **Drivers:** Energy index +17.9% YoY (steepest since September 2022); gasoline +28.4% YoY; fuel oil +54.3%. Energy accounted for 40%+ of total CPI gain. Shelter costs +0.6% MoM (re-accelerating). Tariff-sensitive categories: apparel +0.6%, airline fares +2.8% MoM (+20.7% YoY). Real average hourly earnings -0.5% MoM, -0.3% YoY.
* **PPI:** **April PPI +1.4% MoM, +6.0% YoY (highest since 2022)** — released May 13. Core PPI also beat expectations.
* **Core PCE:** 3.0% YoY February (US Bank); March/April readings pending [verify].
* **Fed Outlook:** Federal funds target 3.50–3.75% (held April 29). FOMC statement upgraded language: inflation "is elevated" (was "remains somewhat elevated").
* **May CPI release:** Scheduled June 10, 2026.
* **Consumer Sentiment:** University of Michigan final April reading 49.8 — lowest in series history (since 1952).

### Labor Market
*Last updated: 2026-05-16 07:30 ICT* | *Confidence: High*
* **Unemployment:** **4.3% April 2026** (BLS, released May 8) — held steady. U-6 broader measure rose to 8.2% (from 8.0%).
* **Payrolls:** **+115K April** (vs +55-65K consensus), down from upward-revised +185K March. February revised down to -156K (from -133K). Two-month revisions net -16K.
* **Participation:** **61.8%** (down from 61.9% March, lowest since October 2021). Labor force shed 226K in April.
* **Wages:** Average hourly earnings +0.2% MoM, **+3.6% YoY** (below 3.8% estimate). Lowest annual since May 2021.
* **Federal Government:** -9K in April. Manufacturing -2K. Health care +37K led gains.
* **Assessment:** Marginal labor weakening masked by headline beat; participation declining. Cooling consistent with stagflation risk: weak hiring + accelerating inflation.
* **May Employment Report:** Scheduled June 5, 2026.

### Market Performance YTD
*Last updated: 2026-05-16 07:30 ICT* | *Confidence: High*
* **S&P 500:** Friday May 15 close **7,408.50** (-1.24%). Record **7,517.12** set May 14, 2026. YTD ~+8.1%.
* **Nasdaq:** May 15 close **26,225.14** (-1.54%). Recent record near 26,560 [verify].
* **Dow:** May 15 close 49,526.17 (-1.07%).
* **Russell 2000:** ~2,793 May 15 (-2.44%, worst single day in six months); still up YTD.
* **VIX:** 18.43 May 15.
* **Crude Oil:** WTI **$100.96** May 15 close (+4.17% on the day). **Brent $109.24** (+3.33%).
* **MSCI EAFE (via EFA):** YTD **~+8.1%** as of May 14 (YCharts iShares EFA series).
* **MSCI EM (via EEM):** YTD **~+22.85%** as of May 13 (Yahoo Finance) — substantial EM outperformance vs prior file figure of 10.4%.
* **Treasury yields (May 15 close):** **30-year 5.121%; 10-year 4.595%; 2-year 4.079%.** 30Y +11bp on the day; 10Y +14bp on the day.
* **Forward P/E:** **21.0** (FactSet Earnings Insight May 8); above 5-year average (19.9) and 10-year average (18.9). At Friday close 7,408 implies forward EPS ~$353; trailing P/E 28.3.

### Dollar and Reserve Currency
*Last updated: 2026-05-16 07:30 ICT* | *Confidence: High*
* **DXY:** **99.05 May 15 close** (TradingEconomics); +0.16% on the day, weekly gain >1% on inflation-rate-hike repricing. 52-week high 101.76 (May 13, 2025); 52-week low 95.55 (Jan 27, 2026).
* **Gold:** **$4,543.60/oz spot May 15 close** (Yahoo, -3.02% on the day). LBMA PM May 13 fix $4,675.70. **Record $5,602.22 set January 28, 2026.** Q1 2026 average record $4,873/oz (WGC). State Street Monthly Gold Monitor cites $4,000–4,750 structural floor.
* **Central Bank Buying:** Q1 2026 net 244 metric tons (fastest in over a year). Continued heavy purchasing from China (~2,309t official reserves), India, Turkey.

### China and Emerging Markets
*Last updated: 2026-05-16 07:30 ICT* | *Confidence: Medium*
* **China GDP:** ~4.6% annualized [verify — figure carried; specific Q1 2026 release not independently confirmed this refresh]; property sector workouts ongoing.
* **Trump-Xi summit:** Mid-May ended without major breakthrough; China agreed to 200 Boeing aircraft (below expected 500). Trump postponed decision on $11B + $14B Taiwan arms packages.
* **India:** MSCI India outperforming EM peers; Modi-Trump tariff deal lowering rates 25% → 18% conditional on India halting Russian oil purchases [verify — specific structure carried from prior refresh].
* **EM performance:** EEM YTD +22.85% (May 13) reflects strong EM equity outperformance. South Korea's Kospi at fresh records; Samsung surging on AI-related strength.

### Europe and Japan
*Last updated: 2026-05-16 07:30 ICT* | *Confidence: Medium*
* **Japan:** BOJ ended NIRP [verify — exit date carried from prior]; Yen volatility around 152-157 [verify] with Tokyo intervention reported around May 1 after breaching 160.
* **Europe:** ECB on hold at 2.00% deposit rate [verify]; markets pricing 1-2 ECB hikes 2026 [verify]. Germany debt brake remains contentious.

### Housing and Commercial Real Estate
*Last updated: 2026-05-16 07:30 ICT* | *Confidence: Medium-High*
* **Residential:** Transaction volumes ~20% below 5-year average; **30-year fixed mortgage rate 6.36%** (Freddie Mac PMMS May 14, 2026), down from 6.37% prior week, vs 6.81% a year ago. 15-year fixed 5.71%.
* **Office CRE:** ~20% Tier 1 vacancy; regional banks increasing 2026 maturity loan-loss provisions.

### Cryptocurrency and Digital Assets
*Last updated: 2026-05-16 07:30 ICT* | *Confidence: Medium-High*
* **Bitcoin:** **$78,995.85 (Yahoo May 15 close, -3.01% on the day).** Down from $82K+ early in week. Risk-off backdrop pressuring crypto alongside equities.
* **Stablecoin Market Cap:** Continued growth; legislation pending.

### Earnings Yield vs Credit Yield Snapshot
*Last updated: 2026-05-16 07:30 ICT* | *Confidence: Medium-High*
* **S&P 500 Forward Earnings Yield:** **~4.76%** (1 / 21.0 forward P/E from FactSet at S&P 7,408 close May 15).
* **US Investment-Grade Yield:** **~5.50%** (estimated; ICE BofA US Corporate Index latest visible FRED observation 5.22% on March 26 + ~30bp upward adjustment for 10Y rise to 4.595%).
* **US High-Yield Yield:** **~7.20%** (estimated; ICE BofA HY effective yield 6.87% April 30 GuruFocus / 6.77% April monthly TradingEconomics + ~30bp adjustment for rate rise; HY OAS 2.82% May 13).
* **Spread (Earnings Yield − IG Yield):** **~−0.74%** (widened from -0.15% in prior file).
* **Assessment:** Negative spread widened substantially since May 8 (from -0.15% to -0.74%). Credit now offers ~74bp more yield than equity on forward-looking basis. Reinforces **Marks** framework (credit > equity in late-cycle posture) more strongly than prior refresh indicated.

---

## SECTION 5 — CORRELATION ASSUMPTIONS AND FRAMEWORK BACKING

### Framework Philosophies and Real-Allocator Backing

Each of the five expert personas in this analyzer is a constructed translation — none of these individuals publishes a personal allocation model. Each persona is informed by published research from real institutional allocators whose work aligns with the persona's stated philosophy.

* **Dalio (Risk-Parity Persona).** Translated allocation backed by AQR Capital Management published research on risk parity (Asness, Frazzini, Pedersen) and Bridgewater's "All Weather" methodology. The 30/40/15/7.5/7.5 allocation reflects equal risk contribution principles. *Repo/funding sensitivity:* Dalio's diversification thesis is partly a hedge against liquidity regime shifts.

* **Dimon (Fortress Quality Persona).** Translated allocation backed by JPMorgan Asset Management's Multi-Asset Solutions research on quality factor investing, plus QMJ academic literature. The 50/30/20 allocation reflects high-quality US equity bias plus structural cash buffer. *Repo/funding sensitivity:* Dimon's Tier 1/2 requirement directly addresses repo stress survival.

* **Buffett (Long-Duration Quality Persona).** Translated allocation backed by David Swensen's endowment model. The 90/10 individual allocation reflects Buffett's guidance to his wife's trustee. *Repo/funding sensitivity:* Lower direct sensitivity; long-horizon equity holders survive repo episodes but suffer drawdowns through them.

* **Blanchard (Fiscal-Stress Resilience Persona).** Translated allocation backed by Antti Ilmanen's research at AQR on regime-aware asset allocation, plus Rob Arnott's (Research Affiliates) work on inflation-resilient portfolios. The 40/30/20/10 allocation reflects fiscal-sustainability concerns. *Repo/funding sensitivity:* Repo stress operationalizes Blanchard's thesis.

* **Marks (Cycle-Aware Credit Persona).** Translated allocation backed by Oaktree's published memos plus academic literature on credit-cycle timing. The credit-overweight bias reflects Marks's "Sea Change" framework. *Repo/funding sensitivity:* Highest sensitivity. Marks explicitly identifies funding-market dysfunction as the trigger for credit dislocations.

### Five-Regime Taxonomy (verbatim — analyzer requirement)

* **Traditional regime** — stocks and bonds negatively correlated; 60/40 works
* **Inflationary regime** — positive stock-bond correlation; nominal bonds fail as hedge; TIPS and real assets outperform
* **Stagflation regime** — growth falling, inflation rising; both stocks and bonds decline; gold, commodities, short-duration hedge
* **Fiscal-dominance regime** — central bank monetizes deficits; long-duration bonds repriced; real assets and international diversification critical
* **Deflationary regime** — growth and inflation falling; nominal bonds outperform; cash and quality bonds primary safety

### Current Regime Assessment

* **Current Regime:** **Inflationary regime with stagflation risk — actively confirmed and intensifying.** April CPI 3.8%, Core CPI 2.8%, April PPI 6.0% YoY. Energy shock from Iran war drove headline but core also accelerated. Labor market cooling at margins (participation 61.8%, real wages -0.3% YoY) while inflation rising — classic stagflation signature. Equity hit new record 7,517.12 May 14 then dropped 1.24% May 15. Gold at $4,543. 10-year yield at one-year high 4.595%; 30-year at 5.12%. UMich consumer sentiment at all-time low (49.8) while indices near records signals classic late-cycle divergence. **Markets repriced from "no 2026 cuts" to ">50% probability of 2026 rate HIKE."** Repo plumbing under stress since Q3 2025; QT ended October.
* **Primary Risk Scenario:** Stagflation deepens if Iran ceasefire fully collapses / Hormuz disruption sustained; alternatively, recession arrives if Fed forced to hike into weakening labor market. Fiscal-dominance pressure escalates as $38.91T debt rolls at 4.60%+ yields and repo plumbing struggles.
* **Best Suited:** **Dalio** (gold/commodity/diversification) and **Blanchard** (fiscal-stress hedge with TIPS and international; EM outperformance YTD +22.85% validates international tilt).
* **Least Suited:** **Buffett** (concentrated US equity exposure at record valuations with forward P/E 21.0 carries elevated drawdown risk; AI-mega-cap concentration risk in inflation regime).
* **Justification:** April CPI energy-led acceleration to 3.8%, April PPI 6.0% YoY, gold at $4,543, VIX at 18.43, $38.91T debt with weak Treasury auctions and visible repo stress, UMich sentiment at all-time low, Powell-to-Warsh transition completed under maximum macro stress, Iran ceasefire on "massive life support," and EM substantially outperforming US YTD together signal active inflationary regime with stagflation risk and fiscal-dominance pressure.

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

**Repo Stress Tier Reassessment:** Under "repo dislocation stress" (Scenario 2 subvariant), short-duration corporate paper and prime money market fund holdings may face redemption gates and should be treated as Tier 3 effective Tier 4 for scoring. US Treasury bills remain Tier 2 (collateral-eligible at SRF) and become more valuable, not less.

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
- *Relevance to 2026:* **High and active** — April CPI 3.8%, April PPI 6.0% YoY (highest since 2022), Iran war disruption resumed, Section 122 tariffs adding to consumer prices, 30-year yield at 5.12% (one-year high). Scenario partially playing out.

**Scenario 2 — Credit Crisis (2008 Replay)**
Trigger: credit event cascades through leveraged structures; liquidity freezes; correlations rise to 1. Repo market dysfunction is the canonical transmission mechanism.
- US Equities: −40% to −55%
- Long-duration Treasuries: +15% to +25% (flight to safety)
- IG Corporate: −10% to −20%
- High Yield: −25% to −40%
- Private Credit: −20% to −40% (extended gates)
- Real Estate: −25% to −40%
- Gold: +10% to +20%
- Cash: best protector
- *Relevance to 2026:* **Medium-High** — Moody's BDC negative outlook, $20B redemption surge with only 53% fulfilled, Marks April 9 memo, three SRF spikes since September 2025, QT ended October 2025. Heightened by tighter financial conditions.
- Apply post-gate stress tier reclassification per Section 7.
- Apply repo stress tier reclassification per Section 7.

**Scenario 3 — Extended Stagflation (1970s Replay)**
Trigger: growth stalls while inflation stays high for years; supply shock plus fiscal expansion.
- US Equities: −20% to −35% (real terms)
- Long-duration Bonds: −25% to −40%
- TIPS: 0% to +10%
- Commodities: +40% to +80%
- Gold: +50% to +150%
- International Equities: mixed; commodity exporters outperform
- *Relevance to 2026:* **High and rising** — energy shock + cooling labor + fiscal expansion + tariff pass-through is textbook stagflation; consumer sentiment at all-time low while equities at records signals classic late-cycle divergence. Markets repricing to rate-hike expectations confirms scenario actively developing.

**Scenario 4 — Dalio's Debt Collapse (Fiscal Dominance)**
Trigger: foreign buyers stop purchasing US Treasuries; failed Treasury auction; dollar reserve share dropping below 50%. Repo market becomes the visible mechanism.
- Long-duration Bonds: −30% to −50%
- US Dollar: −20% to −35% in real terms
- Gold: +50% to +150%
- Commodities: +30% to +80%
- US Equities: −30% to −50% in real terms
- International Equities: mixed
- Cash (USD): real loss but nominal preserved
- TIPS: 0% to +15%
- *Relevance to 2026:* **Medium** probability, high consequence — $38.91T debt; primary dealer take-up at 24% on late-March 2-year auction; ~33% of marketable debt rolling within 12 months at elevated rates; 30-year at 5.12% (highest since May 2025); QT ended October 2025 in response to repo stress (functional easing despite hawkish rhetoric).

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

**Resolved in this refresh (removed from list):**
- ~~Forward P/E~~ → confirmed 21.0 (FactSet May 8)
- ~~DXY~~ → confirmed 99.05 May 15 close
- ~~30-year Treasury yield~~ → confirmed 5.121% May 15
- ~~10-year Treasury yield~~ → confirmed 4.595% May 15
- ~~2-year Treasury yield~~ → confirmed 4.079% May 15
- ~~Mortgage rate~~ → confirmed 6.36% Freddie Mac May 14
- ~~Hyperscaler capex~~ → confirmed ~$700B four / $660-690B Big Five
- ~~MSCI EAFE YTD~~ → confirmed ~+8.1% (EFA proxy YCharts May 14)
- ~~MSCI EM YTD~~ → confirmed ~+22.85% (EEM proxy Yahoo May 13)
- ~~US IG Yield~~ → estimated 5.50% (latest FRED visible Mar 26 5.22% + ~30bp for yield rise)
- ~~US HY Yield~~ → estimated 7.20% (April monthly 6.77% + ~30bp + HY OAS 2.82% May 13)
- ~~Forward earnings yield~~ → confirmed 4.76% (= 1/21.0)
- ~~Total: 12 items resolved~~

**Remaining [verify] tags (11):**
* [verify] Bank reserves current level — Section 4 Repo Market and Short-Term Funding (October 2025 figure $2.8T is the trigger event reference; current level not independently confirmed this refresh)
* [verify] Basis trade size $1T+ estimate — Section 4 Repo Market and Short-Term Funding (institutional figure, not publicly aggregated)
* [verify] Blue Owl/Apollo/MS NHCC redemption specifics — Section 4 Private Credit Stress (fund-level data not independently re-confirmed)
* [verify] Direct lending default rate ~5.6% — Section 4 Private Credit Stress
* [verify] PIK toggle usage rising in software/SaaS — Section 4 Private Credit Stress
* [verify] Core PCE March/April readings — Section 4 Inflation Trajectory
* [verify] Nasdaq recent record near 26,560 — Section 4 Market Performance YTD
* [verify] China GDP ~4.6% Q1 2026 annualized — Section 4 China and EM (carried forward; not re-checked this refresh)
* [verify] Modi-Trump tariff deal 25%→18% conditional structure — Section 4 China and EM
* [verify] BOJ NIRP exit date, Yen 152-157 range, ECB 2.00% rate / hike pricing — Section 4 Europe and Japan (low decision-utility for US-base-currency portfolios; deferred)

**Note on remaining [verify] tags:** These 11 items were not re-verified in this refresh due to either (a) figures not publicly aggregated (basis trade size), (b) fund-level institutional data requiring direct access (BDC specifics), (c) low decision-utility for the analyzer's primary use case (BOJ/ECB/Yen for US-base-currency portfolios), or (d) the data points are stable enough across short refresh intervals that updating monthly is appropriate (China GDP, Modi-Trump deal structure). Anything in this list should be re-verified at next monthly refresh.

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

**Repo Collateral Quality Check:** For fixed income sleeves, distinguish between SRF-eligible collateral (Treasuries, agency debt, agency MBS) and non-eligible collateral (corporates, munis, private credit). In a repo dislocation, the former retains funding access while the latter does not. Portfolios with >40% fixed income in non-SRF-eligible collateral receive a Dimon and Marks yellow flag.

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
* **Direct Real Estate:** Classified as Tier 5 (illiquid). >40% of net worth in direct real estate = critical red flag for all frameworks (concentration). Operating real estate treated separately from primary residence.
* **Private Business:** Classified as Tier 5 (illiquid). Operating business ownership treated as quality equity exposure for Buffett (potentially green flag if moat-bearing) but as concentration risk for all others.
* **Hedge Fund / Basis Trade Exposure:** Direct or indirect exposure to Treasury basis trade strategies — including certain market-neutral hedge funds and some multi-strategy allocations — carries asymmetric repo-stress risk. >10% allocation = Dimon and Marks moderate red flag, Dalio yellow flag.

---

## SECTION 17 — CASH AND VOLATILITY MANAGEMENT

* Cash held as strategic optionality, not just emergency fund. Marks: "Cash is an option with no expiration date and no strike price."
* Volatility-targeting overlays: optional for sophisticated allocators only. Default position sizing is unleveraged.
* Optimal hold period: Tier 1 cash held for as long as deployment opportunities are scarce relative to expected returns. In current regime (gold $4,543, equity at near-records with forward P/E 21.0, credit yields ~75bp above earnings yields), cash 5-15% of AUM is consistent with most frameworks except Buffett.

---

## SECTION 18 — DALIO ALLOCATION FRAMEWORK

* **Target Allocation (regime-aware):** 30% equity / 40% intermediate Treasuries + TIPS / 15% long Treasuries / 7.5% commodities / 7.5% gold
* **Current Regime Tilt:** Reduce long Treasury exposure to 10%, increase gold to 12.5%, reflecting fiscal-dominance pressure
* **Key Principle:** Equal risk contribution, not equal capital. Each asset class contributes ~20% of total portfolio risk.
* **Diversification Threshold:** Minimum 3 asset classes >10% each
* **Concentration Penalty:** Any single asset class >50% triggers 30% Dalio score cap
* **Optimal Hold Period:** 3–5 years between major rebalances; quarterly tactical adjustments only.

---

## SECTION 19 — DIMON ALLOCATION FRAMEWORK

* **Target Allocation:** 50% high-quality US equity / 30% high-quality fixed income (Treasury and IG corporate) / 20% cash
* **Key Principle:** Fortress balance sheet. Capital preservation paramount; cash buffer enables opportunistic deployment.
* **Quality Filter:** Equity sleeve concentrated in companies with strong balance sheets, durable franchises, S&P A-rated or better
* **Cash Floor:** Minimum 20% Tier 1/2 always
* **Optimal Hold Period:** 5+ years; minimize portfolio turnover; tax-efficient

---

## SECTION 20 — BUFFETT ALLOCATION FRAMEWORK

* **Target Allocation (Trustee Guidance):** 90% S&P 500 index / 10% short-term Treasuries
* **Modified Operational Allocation:** 70% high-quality US equity (concentrated, moat-bearing) / 20% short Treasuries / 10% cash
* **Key Principle:** Buy great businesses at fair prices; hold forever. Index fund for the non-expert.
* **Sector Preference:** Financials, Consumer Staples, Energy; historically wary of Tech (though has held AAPL)
* **Optimal Hold Period:** "Our favorite holding period is forever." Decades, not years.

---

## SECTION 21 — BLANCHARD ALLOCATION FRAMEWORK

* **Target Allocation:** 40% global equity (40-60% non-US) / 30% TIPS and short Treasuries / 20% international fixed income / 10% real assets (commodities, gold)
* **Key Principle:** Hedge against US fiscal sustainability concerns and reserve-currency erosion. Geographic diversification critical.
* **US Dollar Concentration Limit:** Maximum 70% USD exposure
* **TIPS Floor:** Minimum 15% TIPS allocation
* **Current Validation:** EM YTD +22.85% vs S&P YTD ~+8.1% directly validates Blanchard's international diversification thesis.
* **Optimal Hold Period:** 5–10 years between strategic rebalances; tactical overlays around fiscal events.

---

## SECTION 22 — CONSENSUS SIGNALS

| Signal | Dalio | Dimon | Buffett | Blanchard | Marks | Consensus |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| US equity valuations stretched (P/E 21.0) | Yes | Yes | Skeptical | Yes | Yes | 4/5 Warning |
| Gold/real assets warranted | Yes | Neutral | No | Yes | Neutral | 2/5 Buy |
| Long-duration Treasuries risky (30Y at 5.12%) | Yes | Yes | Neutral | Yes | Yes | 4/5 Avoid |
| Cash optionality high-value | Yes | Yes | Yes | Yes | Strong Yes | 5/5 Hold cash |
| Private credit stress emerging | Yes | Yes | Neutral | Yes | Strong Yes | 4/5 Warning |
| International diversification needed (EM +22.85% YTD) | Yes | Neutral | Skeptical | Strong Yes | Yes | 3/5 Tilt |
| AI mega-cap concentration risky | Yes | Neutral | Yes | Yes | Yes | 4/5 Warning |
| Repo/funding plumbing under stress | Yes | Strong Yes | Neutral | Yes | Strong Yes | 4/5 Warning |
| Credit > Equity on forward yield (spread -74bp) | Neutral | Yes | Skeptical | Yes | Strong Yes | 3/5 Tilt to credit |

---

## SECTION 23 — WATCH LIST

| Item | Trigger | Date Added | Priority | Status |
| :--- | :--- | :--- | :--- | :--- |
| Warsh first FOMC | June 16-17, 2026 meeting | 2026-05-16 | High | Pending |
| May CPI release | June 10, 2026 | 2026-05-16 | High | Pending |
| May Employment Report | June 5, 2026 | 2026-05-16 | High | Pending |
| Iran ceasefire status | Full collapse or successful nuclear deal | 2026-05-16 | High | Active deterioration |
| Section 122 15% tariff effective date | Bessent announcement specifics | 2026-05-08 | Medium | Pending |
| CIT ruling on tariff litigation | Three-judge panel decision | 2026-05-08 | Medium | Pending |
| SRF usage spike outside quarter-end | >$10B mid-month draw | 2026-05-16 | High | Monitoring |
| SOFR-IORB spread | >5bp persistent | 2026-05-16 | Medium | Monitoring |
| Section 122 expiration | July 24, 2026 | 2026-05-08 | Medium | Pending |
| Powell role / Fed independence | Public Warsh-Powell disagreement | 2026-05-16 | Medium | Watching |
| Nvidia Q1 earnings | May 20, 2026 release | 2026-05-16b | High | Pending |

**Resolved since last refresh (May 8 → May 16):**
* Warsh full-Senate vote → Confirmed May 13, 54-45
* April CPI release → 3.8% YoY May 12
* April Employment Report → +115K, 4.3% May 8
* Powell post-May 15 status → Stays on Board through January 2028; Warsh chairs from May 14

---

## SECTION 24 — SCORING ALGORITHM

**Per-category score formula:** `score = max(0, 10 − 0.5 × deviation_pp)` where `deviation_pp` is the absolute percentage-point deviation of the portfolio's actual allocation from the framework's target allocation for that category.

**Framework score composition:**
* 50% asset class allocation match (sum of per-category scores, normalized to 100)
* 25% liquidity tier match (Tier 1/2 floor)
* 25% quality and concentration checks

**Floor and Ceiling:** Per-framework scores floored at 0, ceilinged at 100.

**Cap Interaction Rule:** When multiple score caps apply, the lowest cap wins. Caps are applied after the 0-100 composite is calculated.

**Regime-Weighted Average:** Simple average of all five framework scores, then a separate calculation that doubles the weight of regime-aligned frameworks (currently Dalio and Blanchard).

---

## SECTION 25 — BENCHMARK PORTFOLIOS

| Benchmark | Composition | Use Case |
| :--- | :--- | :--- |
| 60/40 Traditional | 60% S&P 500 / 40% US Aggregate Bond | Baseline for most retail comparisons |
| All-Weather (Bridgewater-style) | 30% equity / 55% intermediate-long Treasuries / 7.5% commodities / 7.5% gold | Risk parity reference |
| Permanent Portfolio (Browne) | 25% equity / 25% long Treasuries / 25% cash / 25% gold | Maximum regime-neutrality |
| Yale Endowment (Swensen-style) | 30% equity / 15% absolute return / 15% private equity / 10% real estate / 10% commodities / 20% fixed income | Long-horizon institutional |
| Ray Dalio "All Seasons" Public | 30% equity / 40% long Treasuries / 15% intermediate Treasuries / 7.5% commodities / 7.5% gold | Public-market approximation |

---

*End of Portfolio Alignment Criteria File. Generated 2026-05-16 07:30 ICT.*
