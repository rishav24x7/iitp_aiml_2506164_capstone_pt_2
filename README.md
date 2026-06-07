# Part 2 — RFM Segmentation & Retention Strategy

**D2C Customer Churn Intelligence & Retention** · Capstone Part 2 of 4

This repository segments the customer base using **Recency / Frequency / Monetary** scoring fused with
behavioural signals, and recommends a budget-aware retention action for each segment. **No machine-learning
model is used** — segmentation is rule/score-based and fully explainable.

## Business context

The brand wants targeted retention instead of blanket discounting. Segmentation answers *who* to act on and
*how*, before any predictive model exists. The target `churn_next_60d` (no purchase in the 60 days after the
`2025-09-30` snapshot) is used **only to validate** that segments separate risk — never to build them.

## Repository structure

```
d2c-churn-part2-rfm/
├── rfm_segmentation.ipynb    # Main notebook (run top-to-bottom, outputs included)
├── segments.csv              # Generated: customer_id, segment_name + RFM & behavioural features (2,400 rows)
├── retention_strategy.md     # Generated: per-segment actions + budget prioritisation
├── manual_review_cases.md    # Generated: 12 real customers needing a human decision
├── segment_overview.png      # Generated charts
├── revenue_at_risk.png
├── data/                     # The 7 source CSVs + DATA_DICTIONARY.md
├── requirements.txt
└── README.md
```

## Setup & run

```bash
python -m venv .venv && source .venv/bin/activate     # Windows: .venv\Scripts\activate
pip install -r requirements.txt
jupyter nbconvert --to notebook --execute --inplace rfm_segmentation.ipynb
```

Reads from the relative `data/` folder. Running it regenerates `segments.csv`, both markdown reports, and the charts.

## Method

1. **RFM features** built from raw pre-snapshot orders (drops `_DUP` duplicates; 180-day window). Validated
   against the provided `rfm_modeling_snapshot.csv` — recency r=1.00, frequency 0.996, monetary 0.978.
2. **1-5 quintile scoring** of R (reversed), F, M.
3. **Non-RFM signal fusion:** return rate, negative-ticket rate, web sessions, discount reliance, plus loyalty
   tier and the CRM `manual_priority_bucket`.
4. **8 segments** assigned by ordered rules (see notebook §4).
5. **Budget prioritisation** by *revenue-at-risk* = customers × churn rate × avg monetary.

## Segments (churn shown only as validation)

| Segment | Customers | Churn % | Strategy |
|---|---|---|---|
| Champions | 288 | 9.4 | Reward & advocate — no discount |
| New / Promising | 69 | 21.7 | Onboard to 2nd purchase |
| High-Value but Unhappy | 193 | 24.4 | Service recovery before any offer |
| Loyal Customers | 595 | 28.2 | Deepen & cross-sell |
| Need Attention | 226 | 42.5 | Low-cost nurture |
| Discount-Dependent | 194 | 53.1 | Wean off discounts |
| At-Risk High-Value | 376 | 70.7 | High-touch win-back (top budget priority) |
| Dormant | 459 | 88.2 | Cheap automated win-back only |

Segments built **without** the label still span a 9%→88% churn gradient — strong evidence the design captures
real risk. See `retention_strategy.md` for budget order and `manual_review_cases.md` for the 12 human-decision cases.
