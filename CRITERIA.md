# Portfolio Alignment Criteria File

*Version: 2026-07-28b*

*Last full refresh: 2026-07-28*

*Next scheduled refresh: 2026-08-28*

---

## SECTION 1 — FILE PURPOSE AND SCOPE

This file is the sole data source for the Portfolio Alignment Analyzer. It contains the current macro environment, the five framework definitions with their target allocations and flags, the scoring algorithm, the drawdown scenarios, and the reference benchmarks. The analyzer reads this file and does not substitute general knowledge for any section that is missing or malformed.

Structure: Sections 1 through 25. Section 4 carries the dynamic macro data and is refreshed on a roughly monthly cadence. Sections 17 through 21 carry the five framework definitions. Section 24 carries the pinned scoring algorithm. Sections 6 through 16 and 25 are static editorial rules and change only on deliberate revision.

Every figure in Section 4 is either sourced to a dated release or carries a verify tag. Section 13 lists every verify tag in the file and must match the inline tags exactly.

---

## SECTION 2 — CHANGE LOG

| Date | Version | Description of Changes |
| :---- | :---- | :---- |
| 2026-05-08 | 2026-05-08a | Major v3 restructure to support analyzer 2026-05-08a. Added real-allocator backing per framework in Section 5. Pinned scoring algorithm in Section 24 with explicit deduction formula. Cut Climate and Demographics subsections from Section 4. Trimmed Watch List from 19 to 10 items. Trimmed Consensus Signals from 14 to 8 rows. |
| 2026-05-27 | 2026-05-27a | Major macro refresh. Warsh confirmed Fed Chair May 13. April CPI 3.8% headline / 2.8% core. CIT struck down Section 122 tariffs May 7. Iran war: naval blockade of Hormuz, US strikes May 25-26. Market levels to May 26. |
| 2026-07-01 | 2026-07-01a | Major macro refresh. Iran war ceasefire: Islamabad MOU signed June 17; CENTCOM lifted blockade June 18. WTI collapsed to ~$69-70. Warsh's first FOMC June 17 held 3.50-3.75% unanimous with hawkish dot-plot flip. May CPI 4.2% / 2.9% core. Regime reassessed: stagflation tilt reduced, reclassified to inflationary with fiscal-dominance overhang. **Defect introduced: Sections 17-25 were dropped from the working copy and replaced with a pointer note. Never committed to GitHub — the repo remained at 2026-05-08a.** |
| 2026-07-28 | 2026-07-28a | **Repair and refresh.** (1) **Sections 17-25 restored verbatim from the 2026-05-08a GitHub copy**, closing the structural defect that made the file unusable between July 1 and July 28. (2) **Added Section 1** — both prior versions began at Section 2, silently failing the analyzer's 1-25 numbering check. (3) Section 4 refreshed to July 28. (4) Framework Current Thesis paragraphs in Sections 17, 19, 20, and 21 patched where the May 8 text conflicted with current macro data. (5) Section 22 reviewed, no cell changes. (6) Section 23 Watch List fully rebuilt — 8 of 10 prior items had resolved. (7) Section 13 verify list reconciled. **Regime reassessed: stagflation risk restored to elevated on labor deterioration; see Section 5.** No changes to framework target allocations, red/green flag definitions, scoring algorithm, drawdown return ranges, or benchmark portfolios. |
| 2026-07-28 | 2026-07-28b | **Scoring engine overhaul following an audit of the analyzer prompt.** Section 24 rewritten: Component 1 renamed Structural Fit and given two modes, `allocation` (overlap-based) and `posture` (five 0-10 tests), selected by a new per-framework `Scoring Mode` line added to Sections 17-21. Marks (Section 21) moves to `posture` with five defined tests -- he states no static target allocation on doctrine, so the prior engine could not compute his 50-point component at all and improvised it silently on every run. Allocation math replaced with overlap_pct/2, removing the double-counting of deviations and the category-count asymmetry that scored a plain 60/40 at 0 against Buffett but 20 against Dalio. Caps defined as ceilings rather than multipliers. Green-flag partial credit defined by flag type, with qualitative flags constrained to three discrete states. Critical red flags now escalate the ceiling so compounding problems keep costing after the component floors. Added `Scoring Algorithm Version: 4.0`. **Scores are not comparable to any prior run.** No changes to framework target allocations, red/green flag definitions, drawdown scenarios, benchmark portfolios, or Section 4 macro data. |

---

## SECTION 3 — HOW TO UPDATE THIS FILE

This file is the primary reference for the Portfolio Analyzer. To update:

1. Conduct web searches for each dynamic subsection in Section 4.
2. Review the prior Watch List (Section 23) — note what resolved, and replace resolved items rather than letting the list decay.
3. Update Consensus Signals (Section 22) only when a framework's stance shifts based on new public commentary.
4. Check Sections 17-21 Current Thesis paragraphs against the refreshed Section 4. Where they conflict, patch the thesis paragraph. Do not touch target allocations, red flags, green flags, or hold periods — those are the scoring inputs and are deliberately static.
5. Increment version number, update "Last full refresh" date.
6. **Before committing: confirm Sections 1 through 25 are all present and the file ends with Section 25.** The July 1 refresh silently dropped Sections 17-25; this check exists because of that.
7. Reconcile Section 13 against every inline verify tag — no orphans in either direction.

---

## SECTION 4 — CURRENT MACRO ENVIRONMENT

*Where recent data is unavailable, prior figures carry forward only with verify tags. Inline verify tags must match the Section 13 list exactly.*

### US Fiscal Position

*Last updated: 2026-07-28* | *Confidence: Medium-High*

* **National Debt:** ~$39T+ [verify] (prior $39T+ Treasury Debt to the Penny early May; no fresh primary-source figure sourced to the day at this refresh — debt only grows, flagged for confirmation).
* **Deficit:** Net interest costs on track near $1.0 trillion FY2026, exceeding defense spending; net interest projected ~13.85–14.11% of outlays FY2026-27 (CBO, carry forward).
* **Treasury Auctions:** Bid-to-cover ratios remain soft; ~33% of publicly held marketable debt matures within 12 months.
* **Long-End Repricing — 30-year back above 5%:** 30-year Treasury yield ~5.12% (July 27), up from ~4.97% at the July 1 refresh and now sustained above the 5% threshold rather than briefly touching it. 10-year ~4.63%; 2-year ~4.30%. The long end has risen roughly 15bp since July 1 even as the front end was little changed — a curve steepening consistent with term-premium and fiscal-supply pressure rather than policy expectations.
* **Tariff Refunds:** ~$86.3B in IEEPA tariff refunds paid to date via CBP CAPE [verify], a direct fiscal cost of the February SCOTUS ruling.
* **Interest Burden:** Average interest rate on total marketable debt ~3.35% (carry forward). Net interest outlays up YoY through FY2026.

### Trade and Geopolitics

*Last updated: 2026-07-28* | *Confidence: High*

* **Tariff Authority — SCOTUS Ruling:** Feb 20, 2026 *Learning Resources v. Trump* 6-3 held IEEPA does not authorize tariff imposition.
* **Section 122 — EXPIRED AND REPLACED, NOT LAPSED:** The 10% global surcharge (Proclamation 11012) expired by operation of law at 12:01 a.m. EDT July 24, 2026, at its 150-day statutory ceiling. **A replacement took effect at the same minute.** On July 23 USTR issued its final action in the Section 301 forced-labor investigation initiated March 12, imposing additional duties of **10% or 12.5% on imports from 60 economies** (59 countries plus the EU) covering roughly 99.4% of US imports, across most of HTSUS Chapters 1-97, with product and country exemption annexes and tariff-rate quotas for certain textiles and apparel. The 10% tier applies to economies assessed as maintaining and enforcing a forced-labor import prohibition; 12.5% is the default tier.
* **Net effect on the effective tariff rate: roughly neutral to modestly higher, not the ~11% → ~7-8% drop the prior refresh contemplated.** Section 301 duties carry no statutory expiration and no rate cap, unlike Section 122. This converts a temporary, litigated tariff regime into a durable one on firmer legal ground — Section 301 has been upheld in prior challenges.
* **Other trade actions:** Brazil 25% Section 301 in effect. Section 338 proclamations signed July 20 imposing 50% tariffs on select Canadian goods (autos, alcohol, dairy, furniture), effective August 19, applying even to USMCA-qualifying goods. Pharmaceutical onshoring deadline July 31 — companies must reach agreements reducing the tariff to 20% or face a threatened 100% on branded pharma imports; EU branded pharma capped at 15% by the trade deal. A second Section 301 investigation covering excess industrial capacity in 16 economies has not yet produced tariffs. Section 232 sector tariffs (steel, aluminum, copper, autos, semis) unaffected throughout.
* **Iran War — CEASEFIRE COLLAPSED, THEN PARTIAL RE-PAUSE:** The June 17 Islamabad MOU broke down in early July. Following Iranian attacks on three commercial vessels in the Strait of Hormuz, the US struck Iran in retaliation on consecutive days; **President Trump, speaking at the NATO summit in Turkey, declared the ceasefire "over"** and characterized negotiation with Iran as futile. Sanctions relief granted under the MOU was reversed. WTI jumped from ~$69 to ~$75 and Brent from ~$72 to ~$79 within days, and crude rose roughly 20% across July at its peak. **As of July 27 both sides have again paused attacks** after Trump decided against a major escalation; oil fell more than 5% on that news and Treasury yields eased. The pattern since April has been repeated collapse-and-repair; treat any de-escalation as provisional.
* **Strait of Hormuz Status:** Transit remains disrupted and security-contingent rather than normalized. Flows have not returned to pre-war levels.

### Private Credit Stress

*Last updated: 2026-07-28* | *Confidence: High*

* **Moody's BDC Outlook:** Negative since April 7, 2026 — liquidity mismatches, elevated leverage, AI as a disruptive force.
* **Q2 2026 was the peak redemption quarter, and Q3 is easing.** Blackstone BCRED (~$94.6B total AUM, $42.8B NAV at June 30) saw repurchase requests of ~10% of shares in Q2, up from 7.9% in Q1, and gated at the customary 5% cap — its first-ever gate. On the July 23 Q2 earnings call, president Jon Gray said Q3 redemptions are **"down materially,"** attributing the Q2 spike partly to media noise, while acknowledging carryover of unfulfilled Q2 requests. Blackstone's credit business ended Q2 with **$84B of dry powder, nearly a third higher than at the start of the quarter**, and took $13.3B of inflows into global direct lending during the quarter. Non-investment-grade private credit returned ~1% gross in Q2, ~6.8-7% over the trailing twelve months.
* **Other Q2 gates (confirmed):** Apollo Debt Solutions ~~16.8% requested (~~$2.4B, largest since launch), capped at 5%. Cliffwater Corporate Lending ~17% requested, cap cut to 5% from 7%. Blue Owl OCIC/OTIC and HPS HLEND elevated. Partners Group similar.
* **Defaults / Credit Quality:** Ares Capital non-accruals rose 1.8% → 2.1% (Q1). Direct-lending default rate ~5.6% (Morgan Stanley), potential to reach 8% — above the 2–2.5% historical average. PIK-toggle usage rising in software/SaaS.
* **Assessment — stress is real but the acute liquidity phase has passed its peak.** The structural concerns Marks raised in April (retail liability base, direct-lending default trajectory, PIK usage) are intact. The run-on-the-fund tail that Q2 opened up has narrowed: the gates held, no forced-sale cascade materialized, dry powder rose, and Q3 demand is falling. This is a downgrade to the near-term liquidity-event probability, not to the credit-quality concern.
* **Marks Memo:** April 9 "What's Going On in Private Credit" — direct lending's first major test since 2008; structural liability-side risk from the retail investor base.

### Regulatory Watch

*Last updated: 2026-07-28* | *Confidence: High*

* **July FOMC in progress — decision not yet available.** The meeting runs July 28-29; the statement is due at 2:00 p.m. ET Wednesday July 29, followed by a Warsh press conference at 2:30. Consensus and the large majority of forecasters expect a hold at 3.50–3.75%, which would be the fifth consecutive hold. As of Friday July 24, **CME FedWatch showed ~62% probability of a hold and ~38% of a hike to 3.75–4.00%.** In the absence of forward guidance, the dissent count is the primary signal to watch for September. **Any analysis run on July 29 or later should verify the outcome before relying on this subsection.**
* **June FOMC (June 17, Warsh's first):** Held at 3.50–3.75%, unanimous 12-0. Dot plot flipped hawkish: median saw rates ending 2026 at ~3.8% (a hike), 9 of 18 projected at least one hike, 17 of 18 judged inflation risks to the upside. Year-end PCE projection raised to 3.6% headline / 3.3% core (from 2.7%); 2026 GDP trimmed to 2.2%; unemployment 4.3%. Warsh declined to submit his own dot, cut the statement to ~130 words, and dispensed with forward guidance. Minutes released July 8 confirmed the committee split evenly — half supporting hold or cut, half advocating a hike before year-end.
* **Warsh posture since:** At the ECB Sintra forum July 1 he said "prices are too high," rejected any tolerance for an inflation target above 2%, and declined to say whether a July hike was possible. After the softer June CPI he pushed back directly: some might read the data as mission accomplished, "that is not my view." He told Congress in July that FOMC members "have no tolerance for persistently elevated inflation" and criticized the Fed for letting inflation run above target for five years. He has also argued that one-time supply shocks from energy or AI-related demand are not automatically inflationary, and has established five task forces (communications, balance sheet, data, productivity/labor, inflation frameworks) reporting from late 2026 — a hike now would arguably prejudge their conclusions.
* **Fed Chair Transition Complete:** Warsh confirmed May 13 (54-45), sworn in May 22. Powell remains on the Board of Governors until 2028. DOJ criminal investigation into Powell ended April 24.
* **Crypto/Stablecoin:** Stablecoin Transparency Act remains in Senate committee.
* **Banking — Basel III Endgame:** Reduced severity vs the 2023 version; final implementation delayed to late 2026.

### AI Capital Expenditure

*Last updated: 2026-07-28* | *Confidence: Medium*

* **Q1 2026 Hyperscaler Capex Prints (April 29, carry forward):** Microsoft $190B FY2026; Alphabet $180-190B; Meta $125-145B; Amazon ~$200B. Combined four-hyperscaler 2026 capex tracking $650-725B [verify]. **Q2 prints land in the last days of July and are not yet reflected here** [verify].
* **AI Mega-Cap Leadership — leadership is rotating, not just concentrating.** Top 7 mega-caps ~38%+ of S&P 500 market cap. **Apple overtook Nvidia as the largest company by market capitalization in late July.** The Nasdaq Composite has fallen roughly 5% from its June 30 level on a semiconductor rout: Nvidia dropped on reports a Chinese firm may mass-manufacture key chipmaking equipment, and memory names (Micron, Sandisk) fell hard following a large Shanghai IPO by a Chinese memory rival. SK Hynix (-11%) and Samsung (-9%) followed in Asia. Software outperformed semis — ServiceNow and SAP both rallied on Q2 beats.
* **Bubble concern:** Marks's December 2025 memo "Is It a Bubble?" addressed AI parallels to prior bubbles; his follow-up "AI Hurtles Ahead" extends it. Dalio commentary connects the AI investment cycle to his Big Cycle/capital-war thesis.

### Inflation Trajectory

*Last updated: 2026-07-28* | *Confidence: High*

* **June CPI (released July 14) — sharp cooling, energy-driven:** Headline **3.5% YoY**, down from 4.2% in May and below the 3.8% consensus. Month-over-month **−0.4%**, the largest single-month decline since April 2020. Core **2.6% YoY**, down from 2.9%, and **flat month-over-month** against a 0.2% consensus. The energy index fell 5.7% on the month (gasoline −9.7%) but remains **+15.7% year-over-year**. Shelter +0.1% MoM, food +0.2%.
* **Read on the print:** the deceleration is almost entirely the energy base effect from the June ceasefire. With crude up roughly 20% during July before the late-month pause, the June reading is unlikely to mark a clean trend. Oxford Economics suggested May may prove the year's peak; that call is contingent on the Iran situation holding, which it did not through most of July.
* **April PCE:** 3.8% (12-month). June PCE due imminently and will test the disinflation story alongside Q2 GDP.
* **Real Wages:** Average hourly earnings +3.5% YoY against 3.5% headline CPI — real wage growth has flattened to approximately zero.
* **Consumer Sentiment:** University of Michigan May final 44.8 (all-time series low); June and July readings not confirmed at this refresh [verify]. Inflation expectations carried from May (1-yr 4.8% / 5-10 yr 3.9%) [verify]; Warsh described expectations as easing but "not good enough" in his July 1 Sintra remarks.
* **July CPI release scheduled August 12.**

### Labor Market

*Last updated: 2026-07-28* | *Confidence: High*

* **June jobs report (released July 2) — materially weaker than the prior refresh assumed.** Nonfarm payrolls **+57,000**, against a consensus of 115,000. **Prior months revised down sharply:** April cut 31,000 to +148,000, May cut 43,000 to +129,000 — 74,000 fewer jobs across the two months than previously reported. Private payrolls added only 49,000 against a 110,000 estimate. Leisure and hospitality shed 61,000.
* **The revisions invalidate the July 1 refresh's core labor claim.** That refresh recorded May payrolls at +172K and a three-month average of ~188K, and used "labor resilient" as a primary reason to downgrade stagflation risk. Post-revision, **the average monthly gain over the prior 12 months is approximately 36,000.** The labor market is not resilient; it is decelerating.
* **Unemployment:** 4.2% in June, down from 4.3% — but the decline was driven by people leaving the labor force. **Participation fell 0.3pp to 61.5%**; employment-population ratio down 0.2pp to 59.0%. Long-term unemployed 1.9 million, up 286,000 year over year.
* **Wages:** Average hourly earnings $37.64, +0.3% MoM, **+3.5% YoY**.
* **July employment report scheduled August 7.**

### Market Performance YTD

*Last updated: 2026-07-28* | *Confidence: High*

* **S&P 500:** 7,428.78 (July 27 close), essentially flat against the June 30 close of 7,449 and below the ~7,610 record set in early June. Broke a four-session losing streak on July 27.
* **Nasdaq Composite:** 24,876.91 (July 27) — **down roughly 5% from 26,214 at June 30** on the semiconductor rout.
* **Dow:** 52,747.32 (July 27), a third straight winning day, led by Sherwin-Williams (+8%) and Coca-Cola (+5%) on Q2 beats. The Dow-Nasdaq divergence is the defining index feature of July: rotation out of semis into value and defensives.
* **VIX:** elevated relative to the June range [verify].
* **Crude Oil:** WTI volatile through July on the ceasefire collapse and partial repair — roughly $69 at the start of the month, ~$75 mid-month, up ~20% at the July peak, then down more than 5% on July 27 as both sides paused. Brent tracked ~$4 higher [verify].
* **Treasury Yields:** 10-year ~4.63%; **30-year ~5.12%, sustained above 5%**; 2-year ~4.30%. Yields eased into the FOMC on easing oil and the pause in hostilities.
* **Gold:** ~$4,081/oz (July 27) — **down roughly 10% from ~$4,515 at June 30**, and well below the ~$5,595 record set January 28. Notably weak given the fiscal backdrop and the ceasefire collapse; the move tracks the unwinding of September rate-hike bets and a firm dollar rather than any improvement in fiscal fundamentals. State Street's cited $4,000–4,750 structural floor is now being tested at its lower bound.
* **MSCI EAFE YTD:** +6.1% [verify]; **MSCI EM YTD:** +10.4% [verify] (both carried, stale).
* **Forward P/E:** ~20.2–20.4 [verify], above the 5-year (19.9) and 10-year (19.0) averages. Forward 4-quarter EPS estimate ~$371. Q2 2026 earnings growth expected ~23% YoY, with Information Technology accounting for a record 44 positive EPS guidance updates.

### Dollar and Reserve Currency

*Last updated: 2026-07-28* | *Confidence: Medium*

* **DXY:** ~99 [verify] (carried).
* **Gold:** see Market Performance above — ~$4,081, down ~10% on the month.
* **Central Bank Buying:** Continued purchasing from China (~2,309t official reserves), India, Turkey (carry forward).

### China and Emerging Markets

*Last updated: 2026-07-28* | *Confidence: Medium*

* **China GDP:** ~4.6% annualized; property-sector workouts ongoing.
* **China — technology competition is now a market-moving factor.** A Chinese memory manufacturer's large Shanghai IPO and reports of domestic mass-manufacture of chipmaking equipment drove the late-July semiconductor selloff. This is a new transmission channel from Chinese industrial policy directly into US mega-cap earnings expectations.
* **India:** MSCI India outperforming EM peers; Modi-Trump tariff deal lowering rates 25% → 18% conditional on India halting Russian oil purchases. India is named in the July 24 Section 301 forced-labor action [verify].

### Europe and Japan

*Last updated: 2026-07-28* | *Confidence: Medium*

* **Japan:** BOJ ended NIRP; yen weakness a live theme on Fed-BoJ divergence [verify].
* **Europe:** ECB deposit rate 2.00%; markets pricing 1-2 ECB hikes 2026 [verify]. 10-year Bund ~3.13%. EU goods moved to the trade deal's 15% ceiling July 1 and are insulated from the Section 301 forced-labor tiers; EU carve-outs for aircraft, cork, and generic pharma take effect September 1. Germany debt brake remains contentious.

### Housing and Commercial Real Estate

*Last updated: 2026-07-28* | *Confidence: Medium*

* **Residential:** Transaction volumes ~20% below the 5-year average; mortgage rate ~6.30% [verify]. With the 30-year Treasury sustained above 5%, mortgage rates are unlikely to retreat.
* **Office CRE:** ~20% Tier 1 vacancy; regional banks increasing 2026 maturity loan-loss provisions.

### Cryptocurrency and Digital Assets

*Last updated: 2026-07-28* | *Confidence: Medium*

* **Bitcoin:** ~$58,500-60,000 at June 30, down ~20% in June from ~$76,755 in late May; **current level not confirmed at this refresh** [verify]. Spot BTC ETFs posted their worst month ever in June (−$4.5B; BlackRock IBIT −$3.55B alone); total ETF assets fell to ~$71B from ~$83B.
* **Ethereum:** ~$1,570-2,100 at June 30 [verify].
* **Stablecoin Market Cap:** Continued growth; legislation pending.

### Earnings Yield vs Credit Yield Snapshot

*Last updated: 2026-07-28* | *Confidence: Medium*

* **S&P 500 Forward Earnings Yield:** ~4.95% [verify] (1 / ~20.2 forward P/E). This has risen from ~4.76% at the July 1 refresh as the multiple compressed and forward EPS rolled forward.
* **US Investment-Grade Yield:** ~5.35% [verify] (10Y 4.63% + IG OAS estimate; no fresh primary print sourced this refresh).
* **US High-Yield Yield:** ~7.40% [verify] (10Y 4.63% + HY OAS ~2.8% [verify], still tight by historical standards).
* **Spread (Earnings Yield − IG Yield):** ~−0.40%.
* **Assessment:** Credit continues to offer materially higher yield than equity on a forward-looking basis, and the gap is roughly unchanged from the prior refresh. The negative spread continues to favor the **Marks** framework (credit over equity in a late-cycle posture). Note the reinforcing factor: with the 30-year sustained above 5%, the risk-free long end alone now competes directly with the equity earnings yield.

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

* **Current Regime:** Inflationary regime with fiscal-dominance overhang. **Stagflation risk is restored to elevated, reversing the July 1 downgrade.**

* **Why the July 1 call has been revised.** That refresh downgraded stagflation on two grounds: the energy shock had reversed, and growth was resilient. Both grounds have failed. The energy reversal was undone when the Iran ceasefire collapsed in early July and crude rose roughly 20% on the month before the late-July pause — and the pattern since April has been repeated collapse-and-repair, so the current pause carries no durability. The growth claim rested on payroll data that has since been revised away: the +172K May print became +129K, April fell to +148K, June came in at +57K against a 115K consensus, and **the trailing 12-month average monthly gain is now approximately 36,000**. Participation is falling. The July 1 file recorded a three-month average of ~188K; the correct figure was never close to that.

* **What genuinely improved.** Core CPI at 2.6% and flat month-over-month is a real improvement, not an artifact, and it is the single strongest argument against the stagflation read. Headline at 3.5% is energy base effect and should not be over-read. Private credit liquidity stress passed its peak in Q2 — BCRED's gate held without a forced-sale cascade, Q3 redemptions are down materially, and Blackstone's credit dry powder rose a third to $84B.

* **Primary Risk Scenario:** Sticky-inflation with decelerating growth — the stagflation configuration, now driven by labor deterioration rather than by the energy shock alone. Secondary: fiscal-dominance tail (medium probability, high consequence — $39T+ debt, 30-year sustained above 5%, weak auctions, ~33% of marketable debt rolling within 12 months, and now the added fiscal drag of ~$86B in tariff refunds). Tertiary: renewed energy shock on another ceasefire collapse. Note that Warsh's hawkish posture continues to suppress the near-term monetary-dominance vector — this Fed is not monetizing or cutting under pressure — but that same posture is what makes the stagflation squeeze bind: a Fed that will not cut into a weakening labor market.

* **Best Suited:** **Dalio** (real-asset diversification and fiscal-debasement hedge) and **Blanchard** (fiscal-stress and sticky-inflation resilience via TIPS and international).

* **This pairing is now a closer call than at any prior refresh, and the maintainer should review it.** Two facts cut against Dalio specifically: gold fell ~10% in July to ~$4,081 despite a collapsed ceasefire and a 30-year above 5%, which is the opposite of what the fiscal-debasement thesis predicts; and commodities have been directionally violent rather than trending. The counter-argument for retaining Dalio is that the restored stagflation risk is precisely the regime his gold-and-commodity leg is built for, and one month of gold weakness against a rate-repricing backdrop is not a thesis break. **Marks** has strengthened on the equity side (record concentration, a semiconductor rout, forward P/E ~20.2, a negative equity-versus-IG spread, and a risk-free 30-year above 5% competing directly with the earnings yield) but weakened on the credit side (the Q2 liquidity event did not cascade and Q3 demand is falling). Net, Marks is roughly where the July 1 refresh left him — a live candidate to displace Dalio, not yet displacing him.

* **Least Suited:** **Buffett** (concentrated US equity exposure at ~20.2x forward P/E with ~38%+ mega-cap concentration, now facing a demonstrated new downside channel in Chinese semiconductor competition; elevated drawdown risk if inflation forces the Fed's hand into a weakening labor market).

* **Justification:** June CPI 3.5% headline / 2.6% core, payroll trailing 12-month average ~36K after 74K of downward revisions, participation 61.5%, Iran ceasefire collapsed and only provisionally repaired, 30-year sustained ~5.12%, gold ~$4,081, forward P/E ~20.2, Nasdaq −5% on the month, and a Fed that held five straight meetings while half its committee wants to hike. Together these signal an inflationary regime with fiscal-dominance overhang and a restored stagflation tail.

* **Regime-Weighting Rule:** The analyzer applies 2x weighting to regime-aligned frameworks (**Dalio and Blanchard** at this refresh) in the regime-weighted summary view.

---

## SECTION 6 — TIME HORIZON SPECIFICATION

* **Definitions:**

  * Short-Term: < 3 years
  * Medium-Term: 3–7 years
  * Long-Term: > 7 years


* **Graduated Score Ceilings for Horizon Mismatches** (a ceiling on the final 0–100 score, never a multiplier — see Section 24):

  * Long-term portfolio with short-term need: **75 ceiling**
  * Short-term portfolio with long-term assets: **65 ceiling**
  * Immediate liquidity need with Tier 4/5 assets: **55 ceiling**

---

## SECTION 7 — LIQUIDITY TIERING

| Tier | Description | Examples |
| :---- | :---- | :---- |
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

**Scenario 1 — Inflation Shock (2022 Replay)** Trigger: persistent inflation forces rapid rate rises; tariff pass-through; energy spike.

- US Equities: −20% to −25%
- Long-duration Bonds: −15% to −25%
- TIPS: −5% to −10%
- Commodities: +20% to +40%
- Gold: +5% to +15%
- Cash: real loss but nominal preserved
- *Relevance to 2026:* **High** (upgraded from Medium-High) — the energy-spike leg is live again after the ceasefire collapse (crude +~20% in July), the Section 122 surcharge was replaced rather than allowed to lapse so tariff pass-through continues at a comparable or higher effective rate on a permanent legal footing, half the FOMC wants to hike, and the 30-year is sustained above 5%. Core CPI at 2.6% is the one restraint.

**Scenario 2 — Credit Crisis (2008 Replay)** Trigger: credit event cascades through leveraged structures; liquidity freezes; correlations rise to 1.

- US Equities: −40% to −55%
- Long-duration Treasuries: +15% to +25% (flight to safety)
- IG Corporate: −10% to −20%
- High Yield: −25% to −40%
- Private Credit: −20% to −40% (extended gates)
- Real Estate: −25% to −40%
- Gold: +10% to +20%
- Cash: best protector
- *Relevance to 2026:* **Medium** (downgraded from Medium-High) — Q2 was the peak redemption quarter and the system absorbed it. BCRED's first-ever gate held without forced sales, Q3 redemptions are down materially, Blackstone credit dry powder rose ~a third to $84B, and inflows into direct lending continued. The credit-quality concerns remain (direct-lending defaults ~5.6% and rising, Ares non-accruals 2.1%, PIK usage in software/SaaS) but the liquidity-cascade trigger has receded.
- Apply post-gate stress tier reclassification per Section 7.

**Scenario 3 — Extended Stagflation (1970s Replay)** Trigger: growth stalls while inflation stays high for years; supply shock plus fiscal expansion.

- US Equities: −20% to −35% (real terms)
- Long-duration Bonds: −25% to −40%
- TIPS: 0% to +10%
- Commodities: +40% to +80%
- Gold: +50% to +150%
- International Equities: mixed; commodity exporters outperform
- *Relevance to 2026:* **High** (upgraded from Medium, reversing the July 1 downgrade) — the growth-stalling leg, which the July 1 refresh judged broken, is intact after revisions: trailing 12-month payroll average ~36K, June +57K against 115K consensus, participation down to 61.5%. The supply shock re-engaged with the ceasefire collapse. Fiscal expansion continues. The restraint is core CPI at 2.6% — genuine disinflation in the non-energy basket is the main thing separating this from a textbook 1970s setup.

**Scenario 4 — Dalio's Debt Collapse (Fiscal Dominance)** Trigger: foreign buyers stop purchasing US Treasuries; failed Treasury auction; dollar reserve share dropping below 50%.

- Long-duration Bonds: −30% to −50%
- US Dollar: −20% to −35% in real terms
- Gold: +50% to +150%
- Commodities: +30% to +80%
- US Equities: −30% to −50% in real terms
- International Equities: mixed
- Cash (USD): real loss but nominal preserved
- TIPS: 0% to +15%
- *Relevance to 2026:* **Medium** probability, high consequence — $39T+ debt; ~33% of marketable debt rolling within 12 months; **30-year sustained above 5% rather than briefly touching it**, with the long end rising ~15bp since July 1 while the front end was flat, a term-premium signature; ~$86B in tariff refunds paid out. Warsh's hawkish posture continues to suppress the near-term monetization vector. One notable counter-indicator: gold fell ~10% in July, which is not what this scenario's early stages should look like.

**Scenario 5 — Marks's Credit Boom (Early-Cycle Recovery)** Trigger: recession clears excesses, credit spreads blow out, Fed pivots, disciplined buyer with cash and IG credit deploys at peak spreads.

- IG Corporate: +10% to +20%
- High Yield: +15% to +30%
- US Equities: +30% to +50% from trough
- Cash deployed into credit at peak spreads: outsized returns
- Gold: flat to −10%
- Long-duration Treasuries: −5% to −15%
- *Relevance to 2026:* **Medium-Low** — unchanged. The Q2 credit stress that might have pulled a deployment window forward did not cascade, and HY OAS ~2.8% is nowhere near the blowout this scenario requires. A 2027–2029 window remains the base case. Note that the dry powder is visibly accumulating: Blackstone credit alone holds $84B.

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
| :---- | :---- |
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

*The following items carry verify tags inline in the file and require independent verification at next refresh. Every list entry below must have at least one inline tag, and every inline tag must map to a list entry — no orphans in either direction. The mapping is many-to-one by design: four list entries each cover two inline tags (MSCI EAFE and EM; forward P/E, which appears in two subsections; HY yield and HY OAS; UMich sentiment and inflation expectations). Current count: 21 list entries covering 25 inline tags. Do not "fix" this to 1:1.*

* [verify] National Debt ~$39T+ — Section 4 US Fiscal Position
* [verify] Tariff refunds ~$86.3B paid via CBP CAPE — Section 4 US Fiscal Position
* [verify] India's rate tier under the July 24 Section 301 forced-labor action — Section 4 China and Emerging Markets
* [verify] Hyperscaler combined FY2026 capex $650-725B — Section 4 AI Capital Expenditure
* [verify] Q2 2026 hyperscaler capex prints (late-July earnings, not yet captured) — Section 4 AI Capital Expenditure
* [verify] UMich June and July sentiment / 1-yr and 5-10 yr inflation expectations (4.8% / 3.9% carried from May) — Section 4 Inflation Trajectory
* [verify] VIX current level — Section 4 Market Performance YTD
* [verify] Brent current spot — Section 4 Market Performance YTD
* [verify] MSCI EAFE YTD +6.1% and MSCI EM YTD +10.4% — Section 4 Market Performance YTD
* [verify] Forward P/E ~20.2-20.4 / Forward earnings yield ~4.95% — Section 4 Market Performance YTD and Earnings Yield vs Credit Yield
* [verify] DXY ~99 — Section 4 Dollar and Reserve Currency
* [verify] Yen weakness on Fed-BoJ divergence — Section 4 Europe and Japan
* [verify] ECB rate path market expectation (1-2 hikes 2026) — Section 4 Europe and Japan
* [verify] Mortgage rate ~6.30% — Section 4 Housing and CRE
* [verify] Bitcoin current level — Section 4 Cryptocurrency and Digital Assets
* [verify] Ethereum current level — Section 4 Cryptocurrency and Digital Assets
* [verify] US IG Yield ~5.35% — Section 4 Earnings Yield vs Credit Yield
* [verify] US HY Yield ~7.40% / HY OAS ~2.8% — Section 4 Earnings Yield vs Credit Yield
* [verify] Bridgewater AUM ~$100B–$150B — Section 17
* [verify] JPMorgan Q2 2026 results (reported mid-July, not captured) — Section 18
* [verify] Berkshire Q1 and Q2 2026 13F filings (not captured) — Section 19

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
* **Extreme Concentration (Score Ceilings** — a ceiling on the final 0–100 score, never a multiplier; see Section 24**):**
  * 25–50% single holding: **70 ceiling**
  * 50–70%: **55 ceiling**
  * Greater than 70%: **40 ceiling**
* **All-Cash Portfolio:** Buffett **50 ceiling** (no productive assets), Dalio **60 ceiling** (no diversification), Marks no ceiling (cash-as-optionality consistent with late-cycle posture). Dimon and Blanchard scored normally.
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
* **Scoring Mode:** `allocation` — see Section 24 Component 1.
* **Target Allocation (System-Constructed Translation, backed by AQR risk-parity research):** 30% Stocks, 40% Long-Term Treasuries, 15% Intermediate Treasuries, 7.5% Gold, 7.5% Commodities.
* **Current Thesis (2026, updated 2026-07-28):** Late stages of Big Debt Cycle. February 2 Dubai speech framed dynamics as approaching the "capital war" stage; March 14 Fortune commentary placed the US in transition from Stage 5 to Stage 6 ("the war stage"). Recommends gold (10–15%) as primary fiscal-dominance hedge. Warns abundant capital fueling AI build-out could dry up if foreign Treasury demand falters.
  * **Refresh note — the thesis is intact but the July tape is not cooperating.** The fiscal leg strengthened: the 30-year is sustained above 5.1% rather than briefly touching 5%, the long end rose ~15bp since July 1 while the front end was flat, and roughly $86B in tariff refunds added to the deficit. The real-asset leg weakened: gold fell ~10% in July to ~$4,081 despite a collapsed Iran ceasefire and a rising long end, and commodities have been directionally violent rather than trending (crude +~20% intramonth, then −5% in a session). Late-July equity action — a semiconductor rout driven by Chinese industrial competition, rotation into value and defensives — is consistent with his capital-war framing. Treat one month of gold weakness against a rate-repricing backdrop as noise rather than a thesis break, but flag it.
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
* **JPMorgan Assets:** ~$4.3T [last verified 2026-04-25]. 2025 full-year: managed revenue $185.6B, net income $57.0B, ROE 17%, ROTCE 20%. Q1 2026 net income $16.5B, EPS $5.94, revenue $50.5B (+10% YoY). **Q2 2026 results reported mid-July and are not captured at this refresh** [verify].
* **Investment Philosophy:** "Fortress Balance Sheet" — high capital ratios, massive liquidity, preparation for tail risks.
* **Scoring Mode:** `allocation` — see Section 24 Component 1.
* **Target Allocation (System-Constructed Translation, backed by JPMAM and AQR quality research):** 50% High-Quality US Equities, 30% Cash/Short-duration High-Quality Debt, 20% Alternative/Strategic Credit.
* **Current Thesis (2026, updated 2026-07-28):** The April 6 letter framed an "increasingly complex set of risks": geopolitical conflicts, persistent inflation risk, AI-related uncertainty, large global fiscal deficits, elevated asset prices. Warned a drawn-out Iran war could push energy and commodity prices higher in ways markets have not fully priced — producing "stickier inflation and ultimately higher interest rates."
  * **Refresh note — the Iran warning has been directly vindicated twice.** The war has now collapsed and partially repaired three times since April, and each cycle has moved crude 15-20%. His "stickier inflation, higher rates" prediction is visible in the 30-year sustained above 5% and in a Fed that has held five consecutive meetings with half its committee wanting to hike. The fiscal-deficit concern gained a concrete data point in the ~$86B of tariff refunds. The elevated-asset-price concern is live: forward P/E ~20.2 with a demonstrated new downside channel in Chinese semiconductor competition.
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

* **Who He Is:** Former Chairman/CEO of Berkshire Hathaway. As of January 1, 2026, **Greg Abel is CEO**; Ted Weschler manages the investment portfolio. Buffett continues as Chairman of the Board.
* **Optimal hold period:** 20+ years ("favorite holding period is forever").
* **Berkshire Cash Position:** ~$400B at meeting reference (May 2, 2026). Plus ~$300B in securities. **Q1 and Q2 2026 13F filings not captured at this refresh** [verify].
* **Investment Philosophy:** Value investing. High-conviction concentration in "moat" businesses at reasonable prices.
* **Scoring Mode:** `allocation` — see Section 24 Component 1.
* **Target Allocation (System-Constructed Translation, backed by Swensen long-horizon framework):** 90% Low-cost S&P 500 Index, 10% Short-term Treasuries (for individuals).
* **Annual Meeting May 2, 2026 — First Abel-led:**
  * Theme: "The Legacy Continues."
  * Abel **explicitly ruled out break-up**: "Absolutely not. We see our conglomerate structure working."
  * Abel on cash deployment: "We're not anxious to deploy capital into subpar opportunities."
  * AI cybersecurity flagged as significant risk; "not going to do AI for the sake of AI."
  * Buffett: "Greg is doing everything I did and then some."
* **Current Thesis (2026, updated 2026-07-28):** Continuity-first under Abel. The war-driven volatility and elevated valuations have not produced Buffett-criteria opportunities sufficient to deploy meaningful cash.
  * **Refresh note — the patience is looking better, and the framework's weakest point got weaker.** Forward P/E ~20.2 remains above both the 5-year and 10-year averages, and the late-July semiconductor rout demonstrated a concentration risk this framework's 90% index allocation cannot diversify away: Nvidia fell on reports of Chinese domestic chipmaking equipment, memory names fell on a Chinese competitor's Shanghai IPO, and Apple overtook Nvidia as the largest US company. The Nasdaq is down ~5% from June 30 while the Dow set new highs — the index-level result masks a violent rotation underneath. Holding ~$400B in cash against a 4.3% front end is now a materially better-paid decision than it was when rates were near zero.
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
* **Scoring Mode:** `allocation` — see Section 24 Component 1.
* **Target Allocation (Fiscal Stress Resilience, backed by Ilmanen regime-aware framework and Arnott inflation-resilient research):** 40% TIPS, 30% International Equities (Non-USD), 20% Short-duration Bonds, 10% Real Assets.
* **Current Thesis (2026, updated 2026-07-28):** Continued focus on fiscal sustainability when r > g, with the US trajectory increasingly explosive absent a primary surplus. April 2026 PIIE eurozone panel addressed how rising long-term defense commitments and industrial policy expose fiscal architecture weaknesses.
  * **Refresh note — this is the framework the current data most directly supports.** The r-versus-g gap widened on both sides during July: the 30-year is now sustained above 5.1% (r up), while the trailing 12-month payroll average fell to ~36K after 74K of downward revisions and participation dropped to 61.5% (g down). The long end rose while the front end was flat — a term-premium signature, which is precisely the mechanism his fiscal-sustainability work describes. The ~$86B in IEEPA tariff refunds is a direct, unbudgeted fiscal cost. The short-duration bias in his allocation has been the right call: the 2-year at ~4.30% has been far more stable than the 30-year through this repricing. His non-USD international leg is also supported by the Section 301 conversion — a permanent, uncapped tariff regime raises the structural US price level relative to trading partners.
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

*Source: Oaktree memo "What's Going On in Private Credit" (April 9, 2026); memo "Is It a Bubble?" (December 2025); memo "AI Hurtles Ahead" (2026, addendum to the December memo); Oaktree Conference 2026 podcast (March 24, 2026). Allocator backing: Oaktree's own published memos (Marks's primary output); Asness time-series momentum research applied to credit cycles.*

*Confidence: High.*

* **Who He Is:** Co-founder and Co-Chairman of Oaktree Capital Management.
* **Optimal hold period:** 2–5 years (cycle-aware tactical credit).
* **Oaktree AUM:** ~$223B [last verified 2026-04-25].
* **Investment Philosophy:** "Sea Change" — moving from a 40-year period of declining rates to a normal rate environment where credit offers equity-like returns with less risk.
* **Scoring Mode:** `posture` — see Section 24 Component 1. Marks declines to state a static target allocation on doctrine: correct positioning is a function of cycle stage, not a fixed weight. Inventing a numeric target for him would misrepresent the philosophy this analyzer claims to measure, so his structural fit is scored on five posture tests instead.
* **Target Allocation Bias (Cycle-Aware Credit, backed by Oaktree memos and Asness credit-cycle research):** Overweight Credit (Distressed, Senior Secured) relative to Equities; specific weighting depends on cycle stage assessment.
* **Posture Tests (five tests, 0–10 each, summing to Component 1's 50 points):**
  * **M1 — Credit vs equity tilt.** credit_share = all credit exposure (IG, HY, senior loans, distressed, private credit, credit funds) as a percentage of risk assets (credit + equity). Target band by Section 5 regime stage: late-cycle or stress → ≥55%; mid-cycle → 40–55%; early-cycle or recovery → 25–40%. Score 10 inside the band; deduct 0.4 per percentage point outside it; floor 0. **M1 is the primary test for absence of credit exposure.**
  * **M2 — Seniority quality.** senior_secured_share = senior secured and first-lien as a percentage of the credit sleeve. ≥70% → 10; 50–70% → 7; 30–50% → 4; <30% → 0.
  * **M3 — Credit liquidity.** tier45_credit = credit held in Tier 4–5 vehicles (non-traded BDCs, interval funds, gated or capped vehicles) as a percentage of the total portfolio. This is the liability-side risk his April 2026 memo identifies, and it is the test that most directly encodes his distinctive contribution. 0% → 10; ≤5% → 8; >5–10% → 5; >10–15% → 2; >15% → 0.
  * **M4 — Dry powder.** cash_tbills = Tier 1 cash and T-bills as a percentage of the portfolio, scored against how much optionality the cycle stage warrants. Late-cycle or stress → target ≥10%; mid-cycle → 5–10%; early-cycle or recovery → 2–7%. Score 10 inside the target; deduct 1.0 per percentage point below it; deduct 0.5 per percentage point above it (excess cash is a milder error than none, per "cash is an option with no expiration date"); floor 0.
  * **M5 — Cycle consistency.** Whether aggregate risk posture matches the cycle read: aggressiveness = equity% + high-yield/distressed% + (2 × leverage%). Compare against what the Section 5 regime prescribes — defensive regimes warrant ≤50, neutral 50–65, aggressive ≥65. Aligned → 10; one band off → 6; two bands off → 2; positioned opposite to the cycle read → 0.
  * **Anti-double-counting:** if total credit exposure is under 5% of the portfolio, score **M2 and M3 at 5 (neutral)** and let M1 carry the penalty. The same fact must not be charged three times.
* **Current Thesis (2026, updated 2026-07-28):** The April 9 memo distinguished direct lending (under stress) from broader private credit, emphasizing liability-side risk: a retail/mass-affluent investor base is structurally different from institutional capital and may behave differently under stress. Sea Change thesis intact: credit can deliver equity-like returns with less risk in the current rate environment.
  * **Refresh note — the credit call was tested in Q2 and partially answered; the equity call has strengthened.** Marks's liability-side thesis got its live test: Q2 was the peak redemption quarter, BCRED gated for the first time in its history at 5% against ~10% requested, Apollo Debt Solutions hit 16.8%, Cliffwater ~17%. **The gates worked.** No forced-sale cascade followed, Q3 redemptions are "down materially" per Blackstone's July 23 call, credit dry powder rose nearly a third to $84B, and direct-lending inflows continued at $13.3B in the quarter. The structural concern he identified was real and the mechanism behaved as the vehicles were designed to — which validates the diagnosis while lowering the near-term tail. The credit-quality concerns are undiminished: direct-lending defaults ~5.6% with a path to 8%, Ares non-accruals at 2.1%, PIK-toggle usage rising in software/SaaS. Meanwhile the Sea Change comparison has moved further in credit's favor: the forward equity earnings yield is ~4.95% against ~5.35% IG, and a risk-free 30-year Treasury above 5.1% now beats the equity earnings yield outright. His AI-bubble line of argument gained evidence in the late-July semiconductor rout.
* **Recent Commentary:** April 9 memo: financial cycles follow predictable patterns; the sub-investment grade yield premium "isn't a freebie, but rather compensation for bearing credit risk."
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
| :---- | :---- | :---- | :---- | :---- | :---- |
| Hold significant cash / T-bills | ✓ | ✓ | ✓ | ✓ | ✓ |
| Warning on private credit | ✓ | ✓ | ✓ | ✓ | ✓ |
| Quality over yield | ✓ | ✓ | ✓ | ✓ | ✓ |
| Avoid leverage / complexity | ✓ | ✓ | ✓ | ✓ | ✓ |
| US fiscal sustainability concern | ✓ | ✓ | ⚠ | ✓ | ✓ |
| AI / tech bubble concern | ✓ | ✓ | ✓ | — | ✓ |
| International diversification | ✓ | ✓ | ✓ | ✓ | — |
| Warning on long-duration bonds | ✓ | ✓ | — | ✓ | ✓ |

Legend: ✓ = recommends / warns in alignment; ⚠ = warns against or diverges; — = not a primary view.

*Last updated: 2026-07-28*

* **Highest-confidence signals (5/5 unanimous):** Hold significant cash/T-bills (reinforced by Berkshire ~$400B, and now better compensated with the front end at ~4.3%); Warning on private credit (tested in Q2 — see Section 21 refresh note); Quality over yield; Avoid leverage/complexity.
* **No cell-level changes this refresh.** The Q2 private-credit episode confirmed rather than altered the unanimous warning: the stress was real, the gates held, and the underlying credit-quality concern is unchanged. The long-duration warning is the row with the most new supporting evidence — the 30-year is sustained above 5.1% and rose while the front end was flat.

---

## SECTION 23 — CURRENT EVENTS WATCH LIST

*Fully rebuilt 2026-07-28. Eight of the ten items in the prior list had resolved between May 8 and July 28 (April CPI, April employment report, Warsh confirmation, CIT ruling, Section 122 expiration, June FOMC, Berkshire Q1 13F, and the US-Iran MOU — which resolved and then reversed). Maintained at 10 items with measurable triggers and high impact.*

1. **July FOMC Decision — July 29, 2026, 2:00 p.m. ET** — Immediate watch — Decision lands the day after this refresh. A hold is consensus (CME ~62%); a hike to 3.75–4.00% triggers immediate regime reassessment and repricing of every long-duration position. In the absence of forward guidance, **the dissent count is the signal**: three or more dissents in favor of a hike triggers a September-hike base case.

2. **June PCE and Q2 GDP (late July / early August)** — Immediate watch — Core PCE above 3.0% confirms the Fed's upgraded 3.3% year-end core projection and validates the hawkish half of the committee. Q2 GDP below 1.5% annualized combined with core PCE above 3.0% is the stagflation confirmation signal and would trigger a Section 5 regime reclassification from inflationary-with-stagflation-risk to stagflation proper.

3. **July Employment Report — August 7, 2026** — Immediate watch — The most important release on this list given the labor deterioration. **Payrolls below +25K, or another month of net downward revisions above 50K, triggers a stagflation regime reclassification.** Unemployment above 4.5%, or participation below 61.3%, triggers the same. A print above +125K with upward revisions would partially restore the July 1 resilience read.

4. **July CPI — August 12, 2026** — Immediate watch — Tests whether June's 3.5% was a genuine turn or an energy base effect. Given crude rose ~20% intramonth in July, headline back above 4.0% is the base case for an energy-driven reversal. **Core above 2.9% is the trigger that matters** — it would mean the June core improvement (2.6%, flat MoM) did not hold, removing the main argument against the stagflation read.

5. **Iran Ceasefire — Fourth Cycle** — Immediate watch — The MOU collapsed in early July and both sides re-paused July 27. The pattern since April is repeated collapse-and-repair on roughly monthly cadence. **Renewed Hormuz closure or WTI sustained above $90 triggers Scenario 1 and Scenario 3 probability upgrades and a commodity-leg reassessment for Dalio.** A durable formal agreement with verified Hormuz normalization triggers the reverse.

6. **Q2 2026 Hyperscaler Capex Prints (late July)** — Criteria refresh — Microsoft, Alphabet, Meta, Amazon report in the final days of July. **Any guidance cut to FY2026 capex triggers an AI-cycle reassessment across Dalio (capital-war thesis), Buffett (index concentration), and Marks (bubble thesis).** Combined FY2026 above $750B triggers the opposite.

7. **Chinese Semiconductor Competition** — Criteria refresh — New in this refresh. A Chinese memory rival's Shanghai IPO and reports of domestic chipmaking-equipment manufacture drove a ~5% Nasdaq decline in late July. **Sustained mega-cap concentration falling below 35% of S&P 500 market cap triggers a Section 15 flag-threshold review.** This is a structural channel from Chinese industrial policy into US index earnings and did not exist as a watch item before July.

8. **Section 301 Overcapacity Action (16 economies)** — Regulatory watch — The second Section 301 investigation has not yet produced tariffs, and the forced-labor action of July 24 shows USTR will act on the full timeline. **A finalized overcapacity action raises the effective tariff rate above the ~11% pre-expiry level and triggers a tariff pass-through reassessment.** Related near-term dates: pharmaceutical onshoring deadline July 31 (100% threatened on branded pharma absent agreement); Section 338 Canadian tariffs of 50% effective August 19.

9. **Private Credit — Q3 Redemption Confirmation** — Criteria refresh — Blackstone stated July 23 that BCRED Q3 redemptions are down materially. **Confirmation in Q3 reporting holds Scenario 2 at Medium. A reversal — any major BDC gating a second consecutive quarter, or HY OAS above 500bp — restores Medium-High and triggers a Marks cycle-stage upgrade.** Watch direct-lending default rate against the 8% path Morgan Stanley flagged.

10. **Long-End Treasury Behavior** — Criteria refresh — The 30-year is sustained above 5.1% and rose ~15bp since July 1 while the front end was flat. **A 30-year above 5.5%, a failed or badly-covered long-bond auction, or continued long-end rise while the front end falls, triggers a Scenario 4 probability upgrade from Medium.** Watch alongside gold: gold falling while the long end rises (the July pattern) is evidence against fiscal-dominance pricing and is the single strongest current argument for rotating the Dalio regime weight to Marks.

---

## SECTION 24 — SCORING THRESHOLDS (PINNED ALGORITHM)

**Framework Weights:**

* Simple average: Dalio 20%, Dimon 20%, Buffett 20%, Blanchard 20%, Marks 20%
* Regime-weighted average: 2x weight on regime-aligned frameworks per Section 5

**Scoring Algorithm Version: 4.0** — stamp this into every Save Block. Scores produced under different algorithm versions are not numerically comparable; the analyzer's delta report must suppress score deltas across a version change.

**Pinned Scoring Algorithm (per-framework, 0–100 scale):**

The score is the sum of three components, then capped.

**Component 1 — Structural Fit (0–50 points):**

Each framework declares a `Scoring Mode` line in its Section 17–21 entry. Compute Component 1 by the declared mode. Do not substitute one mode for the other.

---

**Mode `allocation`** — used by Dalio, Dimon, Buffett, Blanchard.

Build the category space: the framework's target categories, plus one catch-all `Other` with a target of 0. Map every holding to exactly one category, so actuals sum to 100.

- overlap_pct = Σ over all categories of min(actual_pct, target_pct)
- allocation_score = overlap_pct / 2

Equivalently, allocation_score = 50 × (1 − TVD/100) where TVD = ½ Σ|actual_pct − target_pct|. The two forms are identical; use whichever is easier to narrate.

This measures how much of the portfolio actually sits where the framework wants it. It counts each misallocation once — a 30pp equity overweight is the same fact as the 30pp shortfall elsewhere, and must not be charged twice — and it is independent of how many categories a framework declares, so scores are comparable across frameworks.

Worked example for Dalio:

- Targets: 30 Stocks / 40 LT Treasuries / 15 Int Treasuries / 7.5 Gold / 7.5 Commodities
- Portfolio actuals: 60 Stocks / 30 LT Treasuries / 10 Cash (Other)
- Overlap: min(60,30)=30, min(30,40)=30, min(0,15)=0, min(0,7.5)=0, min(0,7.5)=0, min(10,0)=0
- overlap_pct = 60
- allocation_score = 60 / 2 = **30 points**

Check via TVD: Σ|dev| = 30+10+15+7.5+7.5+10 = 80; TVD = 40; 50 × (1 − 0.40) = 30. Same answer.

---

**Mode `posture`** — used by Marks.

Some frameworks deliberately decline to state a static target allocation because their doctrine is that correct positioning depends on cycle stage. Fabricating a fixed target for them misrepresents the philosophy the analyzer claims to measure. Those frameworks instead declare five posture tests in their Section 17–21 entry, each scored 0–10.

- posture_score = sum of the five test scores (0–50, no normalization required)

Each test states its own measurement and banding in the framework's entry. Where a band depends on cycle stage, read the stage from the Section 5 regime classification — this is what makes posture mode cycle-aware rather than static.

**Anti-double-counting rule:** where several tests would penalize the same underlying fact, only the primary test may penalize it; the others score neutral (5). Each framework entry names which test is primary for which fact.

---

**Component 2 — Green Flags (0–25 points):**

Each framework lists 4 green flags; each is worth up to 6.25 points. Every flag is one of three types, and the type determines how partial credit works. Classify the flag first, then score it.

**Type A — threshold** (e.g. "Cash/T-bills 25%+"):
- score = min(6.25, (actual / threshold) × 6.25)
- Example: threshold 25%, actual 20% → (20/25) × 6.25 = 5.0 points

**Type B — band** (e.g. "Cash/T-bills 20–30%"):
- Inside the band → full 6.25
- Outside → deduct 0.625 per percentage point beyond the nearer edge, floor 0
- Example: band 20–30%, actual 34% → 4pp beyond → 6.25 − 2.5 = 3.75 points

**Type C — qualitative** (e.g. "Demonstrated moat businesses", "Minimal turnover"):
- Score exactly one of three values: **6.25** (clearly present), **3.125** (partially or ambiguously present), **0** (absent)
- No other value may be awarded. Free-form continuous judgement on qualitative flags is the single largest source of run-to-run score drift; the three-state rule exists to bound it.
- State which state was chosen and the evidence for it in the technical report.

**Component 3 — Red Flags (0–25 points):**

Start at 25 points. Apply deductions:

- Minor red flag: −2 points
- Moderate red flag: −5 points
- First Critical red flag: −10 points AND set a 50 ceiling
- Each additional Critical red flag: a further −5 points AND lower the ceiling by 10 (50 → 40 → 30), floor the ceiling at 20

Floor this component at 0. The escalating ceiling exists because the component alone saturates: without it, a portfolio with four Critical flags would score identically to one with two, removing any penalty for compounding problems.

**Total Raw Score:** sum of the three components. Floor 0, ceiling 100.

**Apply Caps — a cap is a CEILING, not a multiplier:**

A cap limits the final score to at most that value: `final_score = min(final_score, cap)`. A 70 cap on a score of 90 yields 70; on a score of 30 it yields 30, unchanged. Caps are never multiplied through. When several apply, **the lowest ceiling wins.**

- Critical red flag: 50 ceiling, escalating per Component 3
- Horizon mismatch: graduated 75 / 65 / 55 per Section 6
- Single holding >25%: graduated 70 / 55 / 40 per Section 16
- Margin / negative cash: 50 ceiling across all frameworks
- All-cash: 50 Buffett, 60 Dalio (Marks no ceiling; Dimon and Blanchard normal)

When multiple caps apply: name all in Section 2 narrative; state which ceiling won and whether it actually bound the score.

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

*End of Portfolio Alignment Criteria File. Generated 2026-07-28.*
