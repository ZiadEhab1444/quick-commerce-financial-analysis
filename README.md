# Quick Commerce Financial Analysis

![Python](https://img.shields.io/badge/Python-3.13-blue?logo=python&logoColor=white)
![Power BI](https://img.shields.io/badge/Power%20BI-Dashboard-yellow?logo=powerbi&logoColor=black)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen)
![Data](https://img.shields.io/badge/Data-2022--2024-lightgrey)

A financial analysis comparing three publicly listed quick-commerce companies — **DoorDash (DASH)**, **Delivery Hero (DHER.DE)**, and **Jumia (JMIA)** — across 2022–2024, to answer a single investment question:

> **Which company represents the best investment opportunity in Quick Commerce?**

---

## Methodology

**Data sources:** Financial statements pulled via `yfinance` (income statement, balance sheet, cash flow). GMV and Adjusted EBITDA sourced manually from annual reports — DoorDash 10-K, Delivery Hero Annual Report, Jumia 20-F.

**Currency standardization:** Delivery Hero reports in EUR. All figures converted to USD using average annual EUR/USD exchange rates (2022: 1.053 | 2023: 1.082 | 2024: 1.085). This reflects real economic value per period rather than a single snapshot rate.

**Scope note:** Full quick-commerce segment isolation was not achievable from public filings for any of the three companies. All analysis uses group-level figures as the best available public proxy. This is a data availability constraint, not an analytical choice.

**Metrics analyzed:** Revenue growth, gross margin, operating margin, Adjusted EBITDA margin, net income, operating cash flow, cash runway, and GMV-level unit economics.

---

## Key Findings

### DoorDash — Operating Leverage at Scale
Revenue grew from $6.6B to $10.7B (27.6% 2-year CAGR), entirely organic — no acquisitions. More importantly, the gap between gross margin and operating margin closed from 62 points in 2022 to 49 points in 2024, while Adjusted EBITDA margin expanded from +5.5% to +17.7%. Operating Cash Flow reached $2.13B in 2024 — a 5.8x increase in two years — with no external funding required. DoorDash became the only company in this analysis to achieve positive Net Income in 2024 (+$123M).

### Delivery Hero — Turnaround in Progress, Not Yet Complete
Operating Cash Flow turned positive in 2024 (+$693M) after two years of heavy burn, and operating margin crossed into positive territory (+3.6%). However, Net Income remained -$957M due to structural costs below the operating line — $641M in restructuring charges and $317M in interest expense. The 2024 cash recovery was partly supported by the Talabat IPO, not purely operational improvement. Delivery Hero is a turnaround story, not a maturity story.

### Jumia — Structural Fragility in Underdeveloped Markets
Revenue declined two consecutive years (-8.3% in 2023, -10.1% in 2024). Active customers fell from 7.3M to 5.4M. Cash runway was 4 months in 2022 — the company was close to insolvency. Despite a gross margin of ~59% (the highest of the three), operating margin sat at -38% to -94%. The gross margin is structurally hollow: fulfillment and logistics costs in underdeveloped African markets consume everything above the gross profit line. Jumia is a survival story, not an investment opportunity.

---

## Investment Scorecard

| Metric | DoorDash | Delivery Hero | Jumia |
|---|:---:|:---:|:---:|
| Revenue Growth (2-Yr CAGR) | 🥇 27.6% | 🥈 21.5% | 🥉 -9.2% |
| Gross Margin % (2024) | 🥈 48% | 🥉 27% | 🥇 59%* |
| Operating Margin Direction | 🥈 closing | 🥇 fastest close | 🥉 stagnant |
| Adj. EBITDA Margin (2024) | 🥇 +17.7% | 🥈 +5.6% | 🥉 -30.6% |
| Net Income (2024) | 🥇 +$123M | 🥉 -$957M | 🥈 -$99M |
| Operating Cash Flow (2024) | 🥇 +$2.13B | 🥈 +$693M | 🥉 -$57M |
| Cash Runway Risk | 🥇 None | 🥈 Improving | 🥉 Fragile |
| Cash Balance Growth | 🥇 +$2.04B | 🥈 +$1.59B† | 🥉 -$16M |

*Jumia's gross margin is operationally hollow — consumed by fulfillment costs in underdeveloped markets.  
†Delivery Hero's 2024 cash recovery was partly supported by the Talabat IPO.

**Total Score (lower = better):** DoorDash 10 / Delivery Hero 17 / Jumia 21

---

## The Verdict

**DoorDash (DASH)** is the clear investment choice.

It is the only company in this analysis to achieve all three milestones of investment-grade maturity simultaneously:

1. **Profitability** — Positive Net Income of +$123M in 2024. First among the three to cross this threshold.
2. **Cash generation** — Operating Cash Flow of $2.13B in 2024, up from $367M in 2022. A 5.8x increase driven entirely by core operations.
3. **Scale with improving margins** — GMV scaled from $53.4B to $80.2B while Adjusted EBITDA Margin expanded from +5.5% to +17.7%. This is operating leverage working at scale.

---

## Dashboard

The analysis is visualized in a four-page Power BI dashboard.

### Revenue Story
![Revenue Story](PIC/Revenue%20Story.png)

### Profitability Trajectory
![Profitability Trajectory](PIC/Profitability%20Trajectory.png)

### Cash Position
![Cash Position](PIC/Cash%20Position.png)

### Investment Scorecard
![Investment Scorecard](PIC/Investment%20Scorecard.png)

---

## Project Structure

```
quick-commerce-financial-analysis/
│
├── README.md
│
├── NoteBooks/
│   └── Quick-Commerce_Financial_Analysis.ipynb   # Full analysis — Phases 1–3
│
├── DATA/
│   └── qc_financial_data.xlsx                    # Master dataset (9 rows × 17 columns)
│
├── DashBoard/
│   └── Quick-Commerce Financial Analysis.pbix    # Power BI dashboard (4 pages)
│
└── PIC/
    ├── Revenue Story.png
    ├── Profitability Trajectory.png
    ├── Cash Position.png
    └── Investment Scorecard.png
```

---

## How to Run

**Requirements:** Python 3.x, Jupyter Notebook

```bash
pip install pandas numpy yfinance openpyxl
```

Open `NoteBooks/Quick-Commerce_Financial_Analysis.ipynb` and run cells sequentially. The notebook pulls live data from `yfinance` — figures may differ slightly from those in this README if financial statements are restated after publication.

**Phases in the notebook:**
- Phase 1 — Data collection via yfinance
- Phase 2 — Cleaning, FX conversion, derived metrics
- Phase 3 — Analysis: revenue growth, profitability, cash position, investment scorecard

---

## About

Built as a portfolio project targeting Data and Business Analyst roles in the e-commerce and quick-commerce space. All data is publicly available. Analysis period: 2022–2024.
