An end-to-end data analytics project analyzing 3,900 customer records across 18 attributes to uncover shopping patterns, customer segments, and revenue drivers — built to mirror real-world business intelligence workflows.

📌 Project Overview
This project simulates a corporate-grade analytics pipeline — from raw data to actionable business recommendations — using Python, SQL, and Power BI.
AttributeDetail📦 Dataset3,900 customers · 18 features🛒 CategoriesClothing, Footwear, Outerwear, Accessories👥 DemographicsAges 18–70 · Male & Female💰 Total Revenue$233,081 · Avg. Purchase: $59.76

🗂️ Repository Structure
customer-behavior-analysis/
│
├── 📓 CUSTOMER_SHOPPING_BEHAVIOR_EDA.ipynb   # Data cleaning, EDA, DB load
├── 🗄️ SQL_queries.sql                        # 10 business SQL queries
├── 📊 customer_behavior_dashboard.pbix       # Power BI dashboard
├── 📁 customer_shopping_behavior.csv         # Raw dataset
└── 📄 README.md

🔄 Workflow
Raw CSV  →  Python (EDA & Clean)  →  SQL Database  →  Power BI Dashboard  →  Insights
1. 🐍 Data Preparation & EDA (Python)

Imported and explored 3,900 rows × 18 columns
Cleaned nulls, fixed data types, removed duplicates
Engineered new features: age_group, purchase_frequency_days
Visualized distributions, correlations, and purchase trends
Loaded cleaned data into SQL database via SQLAlchemy

2. 🗄️ Data Analysis (SQL)
Answered 10 business questions using advanced SQL:
#Business QuestionQ1Total revenue by genderQ2Discount users who still spent above averageQ3Top 5 products by review ratingQ4Average spend: Standard vs Express shippingQ5Subscriber vs non-subscriber spend comparisonQ6Top 5 products by discount usage rateQ7Customer segmentation: New / Returning / LoyalQ8Top 3 products per category (Window Function)Q9Repeat buyers and subscription likelihoodQ10Revenue contribution by age group
3. 📊 Visualization (Power BI)

Connected SQL database directly to Power BI
Built interactive dashboard with slicers by category, gender, season
Created DAX measures for KPIs: revenue, avg spend, segment counts
Enabled drill-through for product and demographic deep dives


🔑 Key Insights

👥 Loyal customers (11+ previous purchases) form the highest-value segment, driving repeat revenue at 2× the rate of new customers
🎽 Clothing is the top-selling category across all age groups
🎟️ Customers who used discounts still outspent the average — indicating promos attract genuine buyers, not just bargain hunters
📦 Standard shipping users show comparable spend to Express — no significant premium behavior difference
🔁 Customers with 5+ previous purchases are significantly more likely to hold an active subscription


🛠️ Tech Stack
ToolUsagePythonPandas, NumPy, Matplotlib, Seaborn, SQLAlchemySQLAggregations, CTEs, Window Functions, SubqueriesPower BIDAX, Data Modeling, Interactive DashboardDatabasePostgreSQL / MySQL / MS SQL ServerJupyterNotebook-based EDA and data pipeline

🚀 How to Run
1. Clone the Repository
bashgit clone https://github.com/your-username/customer-behavior-analysis.git
cd customer-behavior-analysis
2. Install Python Dependencies
bashpip install pandas numpy matplotlib seaborn sqlalchemy psycopg2
3. Run the Notebook
Open CUSTOMER_SHOPPING_BEHAVIOR_EDA.ipynb and run all cells.
This will clean the data and load it into your SQL database.
4. Set Up the Database

Create a database in PostgreSQL / MySQL / MS SQL Server
Update the connection string in the notebook:

pythonengine = create_engine("postgresql://username:password@localhost/your_db")
5. Run SQL Queries
Open SQL_queries.sql in your SQL client and execute the queries.
6. Open Power BI Dashboard
Open customer_behavior_dashboard.pbix and update the data source connection to your database.

📁 Dataset
The dataset contains 3,900 rows with the following features:
Customer ID · Age · Gender · Item Purchased · Category · Purchase Amount (USD) · Location · Size · Color · Season · Review Rating · Subscription Status · Shipping Type · Discount Applied · Promo Code Used · Previous Purchases · Payment Method · Frequency of Purchases

👤 Author
Abhishek Thale

💼 LinkedIn: https://www.linkedin.com/in/abhishek-thale-291477297/


⭐ If you found this project helpful, please star the repo!
