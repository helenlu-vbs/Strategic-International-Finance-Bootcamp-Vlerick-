# Strategic International Finance Bootcamp – Vlerick Business School
## International Comparable Company Valuation

This repository contains example code for an exercise developed for the Strategic International Finance Bootcamp at Vlerick Business School. We apply gradient boosting models (GBMs) to conduct relative valuation in an international setting.

## Target variables

- `ln(EV2Sales)`
- `ln(EV2EBITDA)`
- `ln(PE)`

Where:

- **EV (Enterprise Value)** = Market Capitalisation + Interest-Bearing Debt − Cash & Cash Equivalents  
- **Sales** = the most recent available annual sales (as of the end of January 2026)  
- **EBITDA** = Earnings Before Interest, Taxes, Depreciation and Amortisation  
- **PE** = Price-to-Earnings multiple  

The market value of equity is the latest available value as of the end of January 2026.  
Accounting information is the most recent available information as of the end of January 2026.

## Features

- **Industry** (as defined by Refinitiv)
- **Sales** (in USD mn)
- **SalesGrwth**: $`\left(\frac{\mathrm{Sales}_t}{\mathrm{Sales}_{t-2}}\right)^{1/2} - 1`$; if $`\mathrm{Sales}_{t-2}`$ is missing, use the previous year's sales growth
- **ROA**: EBIT / Total Assets
- **ATR**: Asset Turnover Ratio = Sales / Total Assets
- **EBITDA_pct**: EBITDA margin = EBITDA / Sales
- **Capex2EBITDA**: Reinvestment rate = Capital Expenditure / EBITDA (missing CapEx replaced with 0)
- **NetDebt2TotalAssets**: Leverage ratio = (Total Interest-Bearing Debt − Cash & Cash Equivalents) / Total Assets
- **OpLev**: Operating leverage = \[COGS (Cost of Goods Sold) + SG&A (Selling, General and Administrative Expenses)\] / Total Assets
- **Cash2TotalAssets**: Cash & Cash Equivalents / Total Assets
- **Rnd2Sale**: R&D Expenses / Sales (missing R&D replaced with 0)
- **TaxRate**: Total tax expense (in the income statement) / Profit before tax
- **PayoutRatio**: Total cash dividends / Net profit before extraordinary items
- **Total CO2 Equivalent Emissions to EVIC (USD mn)**: \[(Scope 1 + Scope 2)\] / Enterprise Value Including Cash (USD mn)
- **ESG Controversies Score**: best = 100, worst = 0
- **ESG Score**: best = 100, worst = 0
- **CDS**: CDS as of January 26, 2026 (Damodaran website)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/helenlu-vbs/Strategic-International-Finance-Bootcamp-Vlerick-/blob/main/notebooks/Comparables_GBM_2026.ipynb)
