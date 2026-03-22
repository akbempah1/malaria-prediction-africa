# Malaria Prediction in Sub-Saharan Africa

![Python](https://img.shields.io/badge/Python-3.10-blue) ![scikit-learn](https://img.shields.io/badge/scikit--learn-1.3-orange) ![WHO](https://img.shields.io/badge/Data-WHO%20%2B%20World%20Bank-green) ![Africa](https://img.shields.io/badge/Focus-44%20Countries-red)

**Predicting malaria incidence across 44 African countries using GDP, rural population, and health expenditure — Random Forest regression achieving R²=0.789 with WHO and World Bank live data.**

> Author: Afriyie Karikari Bempah, PharmD | [LinkedIn](https://linkedin.com/in/afriyiekarikaribempah) | [GitHub](https://github.com/akbempah1)

---

## Overview

This project builds a regression model to predict malaria incidence across Sub-Saharan Africa using socioeconomic and health system variables. Data is pulled live from two public APIs — WHO GHO and World Bank — and merged into a single panel dataset covering 44 countries from 2000 to 2023.

---

## Key Findings

| Finding | Implication |
|---|---|
| **Africa malaria incidence fell 40% since 2000** | Bed nets, artemisinin treatment, and donor funding are measurably working |
| **Random Forest R²=0.789 vs Linear R²=0.474** | Non-linear socioeconomic interactions drive malaria burden |
| **GDP per capita is the strongest predictor** | Poverty is the primary structural driver of malaria risk |
| **Niger underpredicted** | Extreme seasonality not captured by annual socioeconomic features |
| **Rwanda and Ghana outperform predictions** | Community health programs deliver outcomes beyond GDP expectations |

---

## Model Performance

| Model | R² | RMSE |
|---|---|---|
| Linear Regression | 0.474 | 1.313 |
| Ridge Regression | 0.474 | 1.313 |
| **Random Forest (Tuned)** | **0.785** | **0.840** |

---

## Technical Approach

- **Multi-API data pipeline** — WHO GHO + World Bank merged on country code and year
- **Log transformation** — applied to malaria incidence and GDP for linearity
- **Three model comparison** — Linear, Ridge, Random Forest
- **GridSearchCV tuning** — 12 parameter combinations, 5-fold CV
- **Country-level 2023 predictions** — actual vs predicted for all 44 countries

---

## Skills Demonstrated

- Multi-source API integration and data merging
- Log transformation for skewed regression targets
- Regression modeling (Linear, Ridge, Random Forest)
- Feature importance analysis
- Residuals analysis and model diagnostics

---

## How to Run

```bash
git clone https://github.com/akbempah1/malaria-prediction-africa.git
pip install pandas numpy matplotlib seaborn scikit-learn requests jupyter
jupyter notebook malaria_prediction.ipynb
```

No API keys required.

---

## Portfolio Series

- [Project 1 — Medicare Drug Spending](https://github.com/akbempah1/medicare-drug-spending-analysis)
- [Project 2 — FDA Adverse Events](https://github.com/akbempah1/fda-adverse-events-analysis)
- [Project 3 — Hospital Readmissions](https://github.com/akbempah1/hospital-readmissions-prediction)
- [Project 4 — Pharma Portfolio](https://github.com/akbempah1/pharma-stock-portfolio-analysis)
- [Project 5 — Credit Risk Scoring](https://github.com/akbempah1/credit-risk-scoring)
- [Project 6 — Africa Disease Burden](https://github.com/akbempah1/africa-disease-burden-analysis)
- **Project 7 — Malaria Prediction** ← you are here

---

*Data sourced from WHO GHO and World Bank APIs. Analysis is independent and not affiliated with either organization.*
