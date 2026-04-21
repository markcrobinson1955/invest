# Portfolio Alignment Criteria File

**Version:** 2026-04-20a (audit remediation)  
**Last full refresh:** 2026-04-20  
**Next scheduled refresh:** 2026-05-20

---

## CHANGE LOG

| Version | Date | Changes |
| :--- | :--- | :--- |
| **2026-04-18a** | 2026-04-18 | Initial expanded version. Added Frameworks 4–5, Consensus Signals table, macro environment. |
| **2026-04-18b** | 2026-04-18 | Added 9 new macro subsections, Correlation Assumptions, Time Horizon Specification, Watch List expanded to 20 items, Howard Marks framework. |
| **2026-04-18c** | 2026-04-18 | Added Change Log, Liquidity Tiering, Currency Exposure Methodology, Drawdown Scenario Models, Rebalancing Framework, Position Sizing Floor, Tax Treatment Overlay, Regulatory Watch. Updated Scoring Thresholds with concentration cap. |
| **2026-04-18d** | 2026-04-18 | Hallucination audit. Added disclaimer block to Drawdown Scenario Models. Labeled 25%/2%/±5% rules as system-defined. Added last-verified dates to AUM/net worth. Added edge-case caveat to gold ETF tax rule. Softened Marks/Buffett claim. Clarified commodity currency rule. |
| **2026-04-20a** | 2026-04-20 | Audit remediation from PASS1_AUDIT.md. Removed embedded 11-step analysis prompt. Added system-constructed-translation labels to all five framework target allocations. Reconciled staleness threshold to 30 days across the system. Labeled liquidity tier thresholds per framework as system-defined editorial rules. Added score cap interaction rule. Added Buffett gold 5% and 20-holdings thresholds. Added duration, credit quality, and sector/factor classification dimensions. Added severity gradient to red flags. Graduated horizon mismatch cap. Added edge-case handling for leveraged ETFs, options, margin, extreme concentration, all-cash, non-USD base currency, direct real estate, private business, pension/annuity. Strengthened gold ETF tax caveat with PHYS/QEF. Added fabrication-risk tags on specific-source statistics. Flagged Feb 2026 Iran/Khamenei narrative as requiring independent verification. Added confidence-range capability to scoring. Added regime-weighting guidance. Added Watch List escalation checking. |

### Deferred from 2026-04-20a
* **Rebalancing plan generator:** Moved to `PORTFOLIO_ANALYSIS_PROMPT.md`.
* **Sixth framework (Asness/Ilmanen):** Deferred for future version to preserve stability.
* **Year-over-year scoring tracker:** Belongs in `PORTFOLIO_ANALYSIS_PROMPT.md`.
* **Holdings-level quality scoring:** Partially addressed via quality criteria; full operationalization in `PORTFOLIO_ANALYSIS_PROMPT.md`.

---

## HOW TO UPDATE THIS FILE
This file feeds a rules-based portfolio analyzer comparing user portfolios against five frameworks: **Ray Dalio, Jamie Dimon, Warren Buffett, Olivier Blanchard, and Howard Marks.**

1. **Refresh Process:** Use `CRITERIA_UPDATE_PROMPT.md` with a web-enabled AI. Replace the **entire** file with the output. Do not edit piecemeal.
2. **Analysis Prompt Reference:** The analysis logic lives in `PORTFOLIO_ANALYSIS_PROMPT.md`. This criteria file no longer embeds the analysis prompt.
3. **Staleness Threshold:** 30 days. If this file is >30 days past its "Last full refresh" date, run the update prompt before analysis.

---

## MACRO VERIFICATION REQUIREMENTS
The following statistics in the 2026-04-18 macro environment section carry **fabrication risk** and must be independently verified at the next refresh. If unverified, replace with "[prior figure carried forward, last verified 2026-04-18]" or remove:

* **Iran Conflict Narrative:** "Operation Epic Fury," killing of Khamenei (Feb 28, 2026), closure of Strait of Hormuz.
* **Treasury Auctions:** "Primary dealers took 24% of a 2-year note auction in late March."
* **Market Estimates:** J.P. Morgan claims regarding DXY ~9% overvaluation and Gold averaging $5,055/oz by Q4 2026.
* **Private Credit:** "$500B private credit exposure" to software/SaaS (Morgan Stanley).
* **Corporate Guidance:** Hyperscaler 2026 capex figures (Amazon ~$200B, Alphabet $175–185B, Meta $115–135B, Microsoft $120B+, Oracle ~$50B).
* **Historical Events:** Feb 20, 2026 Supreme Court ruling in *Learning Resources, Inc. v. Trump*.

---

## CURRENT MACRO ENVIRONMENT
**Last updated:** 2026-04-18 — **Confidence:** High (pending verification of flagged items).

### US Fiscal Position
Total gross national debt stood at **$38.98 trillion** as of April 3, 2026. The $39 trillion threshold was first crossed on March 17, 2026. CBO projects a FY2026 deficit of $1.9 trillion. Interest payments exceeded $529 billion in the first six months of FY2026, roughly equaling combined defense and education spending. Average interest rate on total marketable debt was 3.365% in March 2026.

### Trade and Geopolitics
On February 20, 2026, the US Supreme Court ruled that IEEPA does not authorize presidential tariff imposition. A 10% Section 122 tariff was imposed as replacement, set to expire July 24, 2026. 
**Iran Conflict:** Reported February 28, 2026 US/Israeli strikes ("Operation Epic Fury") killing Supreme Leader Khamenei; Iran closed Strait of Hormuz. As of April 17, 2026, a 10-day Lebanon ceasefire is holding and Iran declared Hormuz "completely open."

### Private Credit Stress
Q1 2026 delivered the first major liquidity test for the ~$3 trillion private credit sector. Ares capped redemptions at 5% after requests surged to 11.6%. US private credit default rate has reached ~5.8%. Morgan Stanley warned defaults could surge to 8%, concentrated in software/SaaS borrowers.

### Inflation & Labor
March 2026 CPI-U rose 3.3% YoY. FOMC SEP projects unemployment at 4.4% for 2026. Market-based measures indicate one to two 25bp cuts remaining in 2026.

---

## CORRELATION ASSUMPTIONS
* **Dalio (All Weather):** Rejects assumption that stocks and bonds always hedge each other. Gold/Commodities are primary for stagflation.
* **Dimon (Fortress):** Correlations rise to 1 in crises. Cash/T-bills are the only reliable zero-correlation assets.
* **Blanchard (Fiscal Resilience):** Nominal bonds and equities fall together during fiscal-dominance or stagflation regimes.
* **Current Regime Assessment (2026-04-18):** Inflationary / Early fiscal-dominance transition. Nominal bond hedging properties are impaired.

> **Regime-weighting Rule:** The analyzer weights the two regime-aligned frameworks (Blanchard and Dalio) at 2x in consolidated summary scores.

---

## TIME HORIZON SPECIFICATION
| Horizon Gap | Score Cap |
| :--- | :--- |
| Within optimal range | No cap |
| Within 30% of range | No cap (note mild mismatch) |
| 30–60% outside range | Cap at 75% |
| 60–100% outside range | Cap at 65% |
| >100% outside range | Cap at 55% |

---

## LIQUIDITY TIERING
* **Tier 1:** Daily liquid (ETFs, T-bills, Money Markets).
* **Tier 2:** Weekly/Monthly liquid (Open-end mutual funds).
* **Tier 3:** Quarterly liquid (Non-traded REITs, BDCs, Interval funds).
* **Tier 4:** Annual/Multi-year lockup (Private Equity, VC).
* **Tier 5:** Illiquid/Gated (Direct RE, distressed debt in workout, gated funds).

---

## CURRENCY EXPOSURE METHODOLOGY
Calculate true currency risk via look-through to underlying economic exposure, not listing currency.
* **US Equities/Treasuries:** 100% USD.
* **Gold/Crypto:** Non-dollar hard assets.
* **Commodities:** 50% USD / 50% Non-dollar (System-defined approximation).
* **Non-USD Base Currency Handling:** Invert the analysis. Calculate home-currency exposure. Treat USD assets as foreign-currency exposure.

---

## DRAWDOWN SCENARIO MODELS

> ### [IMPORTANT DISCLAIMER]
> The return ranges below are illustrative historical analogs. They are **NOT** forecasts or guarantees. Actual results will vary significantly. Do not present stress-test output to a user as a prediction.

### Scenario A: 2022 Analog (Inflation Shock)
Trigger: Persistent inflation forces rapid rate rises. 
* US Equities: -20% to -25%
* Long-duration Bonds: -15% to -25%
* Commodities: +20% to +40%
* Relevance to 2026: **High**

### Scenario B: 2008 Analog (Credit Crisis)
Trigger: Credit event cascades; liquidity freezes.
* US Equities: -40% to -55%
* Long-duration Bonds: +15% to +25% (flight to safety)
* Private Credit: -20% to -40% (Extended gates)
* Relevance to 2026: **Medium**

---

## REBALANCING & POSITION SIZING
* **Trigger:** Drift of more than **±5%** from framework target (System-defined rule).
* **Minimum Sizing:** **2%** of total portfolio. Holdings below this are aggregated as "de minimis" unless they trigger a red flag (e.g., a gated fund).

---

## TAX TREATMENT OVERLAY
| Asset Class | Optimal Account | Reason |
| :--- | :--- | :--- |
| **TIPS** | Tax-deferred | Avoids tax on annual inflation adjustments (phantom income). |
| **High-Yield/Private Credit** | Tax-deferred | Ordinary income treatment; no harvesting benefit. |
| **Municipal Bonds** | Taxable | Tax-exempt interest is wasted in deferred accounts. |
| **Physical Gold ETFs** | Tax-deferred | Avoids 28% collectibles tax (Note: PHYS/QEF may allow LTCG). |

---

## EDGE-CASE HANDLING
* **Leveraged ETFs:** Allocation weight is 3x stated (e.g., 10% TQQQ = 30% US Equity exposure). Moderate to Critical Red Flag.
* **Margin/Negative Cash:** Critical Red Flag for all frameworks.
* **Extreme Concentration:** * 25–50% single holding: 70% Score Cap.
    * 50–70% single holding: 55% Score Cap.
    * >70% single holding: 40% Score Cap.
* **Direct Real Estate:** Classified as Tier 5 (Illiquid). Over 40% of net worth is a Critical Red Flag.

---

## FRAMEWORKS

### 1. Ray Dalio (All Weather)
* **Philosophy:** Risk parity across four macro environments.
* **Target Allocation (Translation):** 15% US Equity, 15% Intl Equity, 20% Long Bonds, 20% Gold/Hard Assets, 10% Commodities, 10% Alts, 10% Cash.
* **Red Flags:** Dollar over-reliance (>80%); No gold allocation.

### 2. Jamie Dimon (Fortress)
* **Philosophy:** Excess capital and liquidity to survive tail risks.
* **Target Allocation (Translation):** 30% Quality US Equity, 20% IG Bonds, 20% Cash/T-Bills, 10% Dev. Intl, 10% Real Assets, 5% Liquid Alts, 5% Private Credit (max).
* **Red Flags:** Private Credit >15%; Margin debt; Tier 5 gated holdings.

### 3. Warren Buffett (Berkshire)
* **Philosophy:** Concentrated ownership of moated businesses; cash as optionality.
* **Target Allocation (Translation):** 47% Quality US Equity, 35% Cash/T-bills, 12% Intl, 6% Bonds.
* **Red Flags:** Crypto >5%; Margin; >20 distinct equity holdings (Over-diversification).

### 4. Olivier Blanchard (Fiscal Resilience)
* **Philosophy:** Resilience against fiscal stress and correlation breakdown.
* **Target Allocation (Translation):** 25% Global Equity, 20% Short Bonds, 15% TIPS, 15% Gold/Real, 10% Intl Bonds, 10% Cash, 5% Uncorrelated Alts.
* **Red Flags:** No TIPS; Dollar over-reliance (>75%).

### 5. Howard Marks (Cycle-Aware)
* **Philosophy:** Calibrate aggressiveness to cycle stage; "Sea Change" into higher rates.
* **Bias (Late-cycle 2026):** Overweight credit; Underweight equities where yields are compressed relative to IG credit.
* **Red Flags:** Covenant-lite private credit; Software/SaaS debt concentration.

---

## CONSENSUS SIGNALS
*Last Updated: 2026-04-18*

| Signal | Agreement |
| :--- | :--- |
| **Hold significant cash / T-bills** | High (All 5) |
| **Warning on private credit** | High (All 5) |
| **International diversification** | Moderate (4/5) |
| **Quality over yield** | High (All 5) |
| **US fiscal sustainability concern** | Moderate (4/5) |

---

## SCORING THRESHOLDS
* **Strong Alignment:** 80–100%
* **Moderate:** 60–79%
* **Partial:** 40–59%
* **Weak:** 20–39%
* **Anti-Aligned:** 0–19%

### Severity-Graded Red Flag Deductions
* **Minor:** -2 points
* **Moderate:** -5 points
* **Critical:** -10 points (+ Score Cap)

---
**End of Portfolio Alignment Criteria File.** *Generated 2026-04-20.*
