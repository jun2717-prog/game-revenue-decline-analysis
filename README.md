# game-revenue-decline-analysis
Analysis of declining game revenue despite user growth using SQL, Python, and ML

# Game Revenue Decline Analysis

## Overview
This project analyzes a 13-year decline in daily game revenue despite consistent user growth. 
Using SQL, Python, and machine learning, it identifies session duration as the strongest driver 
of revenue and shows that internal metrics alone cannot fully explain the drop.

## Key Findings
1. **Revenue declined 51.4%** over 13 years — from a peak of $83K/day (2011) to $40K (2022), 
   with partial recovery to $52K by 2024.
2. **More users, less money** — Daily Active Users grew +55.6%, while revenue per user 
   dropped 56.9% ($0.73 → $0.32).
3. **Session duration is the root cause (r = 0.93)** — the strongest correlate with revenue. 
   Sessions shortened 19.3% (60.8 → 49.1 mins).
4. **Influencers and social media show no meaningful link to revenue** (r ≈ 0.05) — the 2021 
   dip in both was coincidental, not causal.

## Methodology
- **Data Cleaning, Analysis, ML Model & Visualization (SQL + Python):** [Game-revenue-decline-analysis-jupiter.ipynb](Game-revenue-decline-analysis-jupiter.ipynb)
- **Full Presentation:** *(coming soon — PDF to be added)*

## Tools Used
- **SQL** — Data cleaning and validation
- **Python** (pandas, matplotlib, scikit-learn) — Analysis, visualization, ML modeling
- **Tableau** — Interactive dashboards

## Model Performance
|Model|MAE|R²|MAPE| 
| **Gradient Boosting** | $14,700 | 0.5013 | 37.2% |
| XGBoost               | $16,100 | 0.4062 | 42.8% |
| Linear Regression     | $18,700 | 0.1866 | 47.2% |
| Random Forest         | $22,300 | 0.0020 | 65.5% |

Gradient Boosting was selected as the best-performing model across all evaluation metrics.
