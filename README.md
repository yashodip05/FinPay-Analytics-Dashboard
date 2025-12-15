🎨 FinPay Analytics Dashboard

Google Pay–Inspired | Built in Power BI

📌 Project Overview

FinPay Analytics Dashboard is a complete end-to-end Power BI project built using a 120K+ synthetic fintech dataset, modeled and visualized using a design inspired by Google Pay.

The dashboard analyzes:

User behavior

Merchant performance

Payment success/failure

Promo usage

Trends (MoM%)

Hour/day activity patterns

Skills demonstrated:

✔ Data cleaning & modeling
✔ Fact–Dimension schema design
✔ DAX measure creation
✔ MoM%, Pareto, and heatmap visuals
✔ UI/UX following Google Pay theme
✔ Business insights storytelling

📂 Project Structure
FinPay-Analysis/
├── data/
│   ├── raw/
│   │    └── transactions_large.csv
│   └── transformed/
│        ├── dim_user.csv
│        ├── dim_merchant.csv
│        ├── dim_date.csv
│        ├── dim_country.csv
│        ├── dim_device.csv
│        ├── dim_payment_method.csv
│        └── fact_transactions.csv
│
├── powerbi/
│   └── FinPay_Dashboard.pbix
│
├── docs/
│   ├── data_dictionary.md
│   └── screenshots/
│        ├── Overview.png
│        ├── Users.png
│        ├── Merchants.png
│        ├── Payments.png
│        ├── Trends.png
│        └── Banner.png
│
├──.gitignore
├── LICENSE
└── README.md

📊 Dashboard Pages
1️⃣ Overview Page
Total Revenue
Transaction Count
Avg Ticket
Promo Conversion Rate
Payment Method Share
Category Revenue (Pareto)
Revenue Trend
📸 Screenshot:
➡️ <img src=""C:\Users\Yash Kamble\Desktop\FinPay Analysis\docs\screenshots\Screenshot 2025-12-15 at 4.45.32 PM.jpg"" width="600">

2️⃣ User Insights
Active users trend
Returning users
Promo vs Non-Promo users
Users by device
Users by country
Top users by revenue
Hour vs Day heatmap
📸 Screenshot:
➡️ <img src="docs/screenshots/Users.png" width="600">

3️⃣ Merchant Insights
Top merchants by revenue
Merchant category performance
Merchant activity patterns
Promo usage impact
📸 Screenshot:
➡️ <img src="docs/screenshots/Merchants.png" width="600">

4️⃣ Payment Insights
Transaction success rate
Failed transaction reasons
Refunds
Revenue by payment method
📸 Screenshot:
➡️ <img src="docs/screenshots/Payments.png" width="600">

5️⃣ Trends Page
Revenue MoM%
Transaction MoM%
Promo vs Non-Promo revenue
Revenue by payment method
Hour/Day activity heatmap
📸 Screenshot:
➡️ <img src="docs/screenshots/Trends.png" width="600">

📘 Data Dictionary
👉 Click: docs/data_dictionary.md

🔧 How to Use This Project
1. Clone the repository
git clone https://github.com/yashodip05/FinPay-Analysis.git

2. Open the Power BI file
📄 PBIX File:
👉 powerbi/FinPayDashboard.pbix

3. Load the Transformed Data
All CSVs used in the model:
👉 data/transformed/

Raw data:
👉 data/raw/transactions_large.csv

4. Explore & Modify
You may add:
✔ New visuals
✔ Additional DAX measures
✔ Themes
✔ More data sources

🏷 Repository Topics
powerbi
data-analysis
data-visualization
analytics-dashboard
fintech
google-pay
dax
business-intelligence
portfolio-project

📜 License
MIT License
👉 LICENSE

👤 Author
Created by: Yashodip Kamble
If you found this useful, please ⭐ star the repository!

⭐ Want to Support?
Star the repo
Share on LinkedIn & tag @Yashodip Kamble
Fork & build your own version
