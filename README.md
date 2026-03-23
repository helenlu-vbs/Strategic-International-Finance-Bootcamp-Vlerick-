# Strategic-International-Finance-Bootcamp-Vlerick-
# International Comparable Company Valuation

This repositoary contains example code for an exercise is developed for the Strategic International Finance Bootcamp at Vlerick Business School. We apply GBMs to conduct relative valuation in an international setting. The target variables include: 
- ln(EV2Sales)
- ln(EV2EBITDA)
- ln(PE)
EV: Enterprise Value = Market Capitalisation + Interest Bearing Debt - Cash & Cash Equivalent 
Sales: the most recent available annual sales (at the end of January, 2026)
EBITDA: Earnings before Interest, Taxes, Depreciation and Amortisation
PE: Price to Earnings Multiple
Market value of equity is the latest value as of the end of January 2026.
Accounting information is the most recent available information at the end of January 2026.

Features include:
- Coountry
- Industry (as in Refinitiv)
- Sales (in USD mn)
- SalesGrwth: [Sales_t / Sales_{t-2)]^(1/2) -1 ; if Sales_{t-2} is missing, use last year's sales growth
- ROA: EBIT/Total Assets
- ATR: Asset Turnover Ratio = Sales / Total Assets
- EBITDA_pct: EBITDA margin = EBITDA / Sales
- Capex2EBITDA: Reinvestment rate = Capital Expenditure / EBITDA (missing Capex replaced with 0)
- NetDebt2TotalAssets: Leverage Ratio = (Total interest bearing debt - Cash & Cash Equivalent) / Total Assets
- OpLev: Operating Leverage: [COGS (Cost of Goods Sold) + SG&A (Sales, General and Administraion)] / Total Assets
- Cash2TotalAssets: Cash & Cash Equivalent / Total Assets
- Rnd2Sale: R&D expenses / Sales (missing R&D replaced with 0)
- TaxRate: Total tax expenses (in P&L) / Profits before tax 
- PayoutRatio: total cash dividends / net profit before extradinary items
- Total CO2 Equivalent Emissions To EVIC USD in million: [Scope 1 + Scope 2] / Enterprise Value Including Cash in USD mn
- ESG Controversies Score: best = 100, worst = 0 
- ESG Score: best = 100, worst = 0
- CDS: CDS as of January 26, 2026 (Damodaran website)
<img width="865" height="30" alt="image" src="https://github.com/user-attachments/assets/e53e7f1f-c68d-479f-9448-f666da960168" />

