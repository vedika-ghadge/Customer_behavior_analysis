🛍️ Customer Behavior Analysis – End-to-End Data Analytics Project

Analyzing 3,900 retail customer records to understand who buys, what they buy, and how discounts and subscriptions affect spending, using Python, PostgreSQL, and Power BI.

📌 Overview

This project covers the full analytics workflow: loading and cleaning data in Python, exploring it, answering business questions with SQL, building an interactive Power BI dashboard, and presenting the findings.

Business questions answered:

Which customer groups generate the most revenue?
Do subscribers spend more than non-subscribers?
Which products have the best ratings and the highest discount dependency?
How do new, returning, and loyal customers differ?

📂 Dataset

Detail	Description
File	shopping_data.csv
Size	3,900 rows × 16 columns (18 after feature engineering)
Missing values	None
Domain	Retail / fashion shopping behavior (US customers)

Key columns: Customer ID, Age, Gender, Item Purchased, Category, Purchase Amount (USD), Location, Size, Color, Season, Review Rating, Subscription Status, Discount Applied, Previous Purchases, Payment Method, Frequency of Purchases.

Engineered columns:

age_group – customers split into 4 equal groups by age (Young Adult, Adult, Middle-Aged, Senior)
purchase_frequency_days – purchase frequency converted into a number of days

🛠️ Tools & Technologies

Purpose	Tools
Data loading, EDA & cleaning	Python (Pandas) in Jupyter Notebook
Database	PostgreSQL (SQLAlchemy, psycopg2)
Dashboard	Power BI
Presentation	Gamma

🔄 Project Steps

Load Data – Read the CSV into a Pandas DataFrame.
EDA – Checked structure, summary statistics, and missing values.
Data Cleaning – Standardized column names (lowercase, underscores) and renamed Purchase Amount (USD) to purchase_amount.
Feature Engineering – Created age_group and purchase_frequency_days.
Load to PostgreSQL – Wrote the cleaned data to a customer table in the customer_behavior database.
SQL Analysis – Wrote queries using aggregations, subqueries, CTEs, CASE, and window functions (ROW_NUMBER).
Dashboard – Built an interactive Power BI dashboard.
Presentation – Summarized the findings in a Gamma deck.

🔎 SQL Analysis

The queries in Customer_behavior_sql_queries.sql answer:
Total revenue by gender
Customers who used a discount but still spent above the average purchase amount
Top 5 products by average review rating
Subscribers vs non-subscribers: customer count, average spend, total revenue
Top 5 products by discount rate
Customer segmentation: New, Returning, Loyal
Top 3 most purchased products in each category
Whether repeat buyers (more than 5 previous purchases) are likely to subscribe
Revenue contribution by age group

📈 Dashboard

<img width="1462" height="912" alt="Screenshot 2026-10-13 005415" src="https://github.com/user-attachments/assets/aaf2c39a-42d1-4ccd-a281-2d7dd90e928a" />


Built in Power BI (Customer_Behavior_Dashboard.pbix) with KPI cards, charts, and filters for exploring revenue and customer behavior.

🔍 Key Insights

Total revenue is about $233K, with an average purchase of about $60.
Male customers generate about 68% of revenue ($157.9K vs $75.2K for female customers).
Clothing is the top category (about $104K), followed by Accessories (about $74K).
Subscribers do not spend more per order: average spend is about $59.5 for subscribers vs $59.9 for non-subscribers. Subscribers are only 27% of customers, so there is room to grow the subscription base.
About 43% of purchases used a discount, so discount dependency is high.
Spending is spread evenly across seasons and age groups, with no single segment dominating.
Highest-rated products: Gloves, Sandals, Boots, Hat, and T-shirt.

Recommendations:

Review whether the subscription program offers enough value, since it does not lift order value.
Look for ways to attract more female customers, who bring in a much smaller share of revenue.
Test reducing discounts on products with a high discount rate to protect margin.

▶️ How to Run

Clone the repo

bash
   git clone https://github.com/your-username/customer-behavior-analysis.git
   cd customer-behavior-analysis
Install dependencies

bash
   pip install pandas sqlalchemy psycopg2-binary jupyter
   
Create the database – In PostgreSQL, create a database named customer_behavior.
Set your database credentials – Edit the connection details in the notebook (or use environment variables).
Run the notebook – Open Customer_Shopping_Analysis.ipynb and run all cells. This cleans the data and loads it into the customer table.
Run the SQL queries – Execute Customer_behavior_sql_queries.sql in pgAdmin or any PostgreSQL client.
Open the dashboard – Open Customer_Behavior_Dashboard.pbix in Power BI Desktop.

📁 Project Structure
├── shopping_data.csv
├── Customer_Shopping_Analysis.ipynb
├── Customer_behavior_sql_queries.sql
├── Customer_Behavior_Dashboard.pbix
├── images/
│   └── dashboard.png
└── README.md

👤 Author
[Vedika Ghadge] Aspiring Data Analyst 

📧 [vedikaghadge613@gmail.com ] 

💼 [[https://www.linkedin.com/in/vedika-ghadge-827395327/?isSelfProfile=true](url)] 

🐙 [[https://github.com/vedika-ghadge](url)]
