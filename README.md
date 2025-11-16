# FinPay Analytics Dashboard — Google Pay Inspired

**Author:** Yash Kamble  
**Tech:** Power BI, Power Query, DAX  
**Dataset:** Synthetic fintech transactions (120K+ rows)

---

## Project Summary
FinPay is an end-to-end Power BI analytics dashboard inspired by Google Pay. The solution demonstrates data modeling (star schema), DAX measures for business KPIs, UI/UX design, and actionable fintech insights such as top merchants, payment-method performance, promo impact, and time-based trends.

---

## Repo Structure
FinPay-Analysis/
├── data/
│ ├── raw/ # original dataset (transactions_large.csv)
│ └── transformed/ # exported CSVs from Power BI (fact + dims)
├── powerbi/ # FinPay_Dashboard.pbix (Power BI file) or Release asset
├── docs/ # optional: Project report / presentation
├── scripts/ # optional: dataset generation or ETL scripts
├── README.md
├── LICENSE
└── .gitignore


---

## Dashboard Pages & Purpose
- **Overview** — Executive KPIs, category & merchant summaries.
- **User Insights** — Active users, retention, device & country splits.
- **Merchant Insights** — Merchant revenue, success rates, top performers.
- **Payments** — Payment method share, failures, revenue split.
- **Trends** — Revenue & transaction trends, MOM%, promo impact, hour-day heatmap.

---

## Key Features
- Star schema: `fact_transactions` + `dim_user`, `dim_merchant`, `dim_payment_method`, `dim_country`, `dim_device`, `dim_date`
- DAX measures: Total Revenue, Transaction Count, Avg Ticket, GP Revenue, Promo Txns, Promo Conversion, Revenue MOM%, Txn MOM%
- Pareto analysis: identify top 20% merchants driving ~80% revenue
- Interactive slicers: date, country, payment method, category, promo
- Heatmap for hour/day peak analysis
- Clean UI: themed pages, rounded KPI cards, consistent layout

---

## How to run / reproduce
1. If PBIX is included: open `powerbi/FinPay_Dashboard.pbix` in Power BI Desktop.  
2. If only transformed CSVs: open Power BI → Get Data → CSV and load files from `data/transformed/`.  
3. Ensure relationships: `dim_date[Date]` → `fact_transactions[transaction_ts]` (1:*), and each dim to fact on their key.
4. Refresh visuals and use slicers to explore.

---

## Data (short)
Main raw columns:
`Transaction_ID, User_ID, Merchant_ID, amount, currency, payment_method, status, transaction_ts, category, country, device_type, is_promo_used`

Transformed tables (in `data/transformed/`):
- `fact_transactions.csv` — cleaned fact table (one row per transaction)
- `dim_user.csv`, `dim_merchant.csv`, `dim_payment_method.csv`, `dim_country.csv`, `dim_device.csv`, `dim_date.csv`

---

## DAX Measures (highlight)
See `docs/dax_measures.md` for full list and code. Examples:
- `Total Revenue = SUM(fact_transactions[amount])`
- `Transaction Count = COUNTROWS(fact_transactions)`
- `Revenue MOM%` and `Txn MOM%` using `YearMonth` logic.

---

## Screenshots

#### Overview Page
![Overview Page](docs/screenshots/Overview.png)

#### User Insights
![User Insights](docs/screenshots/Users.png)

#### Merchant Insights
![Merchant Insights](docs/screenshots/Merchants.png)

#### Payments Analysis
![Payments Analysis](docs/screenshots/Payments.png)

#### Trends Dashboard
![Trends Dashboard](docs/screenshots/Trends.png)

![Full Trends](docs/screenshots/FullTrends.png)



---

## Data Dictionary
See `docs/data_dictionary.md` for column descriptions.

---

## License
MIT — see `LICENSE` file.

---

## Contact
Yash Kamble — link to LinkedIn / email (www.linkedin.com/in/yashodip-kamble-a0571b246)

