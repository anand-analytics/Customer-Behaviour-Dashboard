# Customer-Behaviour-Dashboard

## 📌 Project Overview
This project reflects a professional, company-level workflow for a data analyst. It covers the **complete data analytics life cycle**, including defining a business problem, data cleaning in Python, advanced querying in MySQL, and building an interactive dashboard in Power BI.

## ❓ Business Problem Statement
A leading retail company noticed changes in purchasing patterns across demographics and sales channels. The objective was to analyze customer data to answer the overarching question: **"How can the company leverage shopping data to identify trends, improve customer engagement, and optimize marketing strategies?"**

## 🛠️ Tech Stack & Tools
* **Python (Jupyter Notebook):** Data manipulation, cleaning, and exploratory data analysis (EDA).
* **MySQL:** Advanced data analysis and answering business questions.
* **Power BI:** Building a sleek, interactive dashboard to track KPIs.

## 🔄 Workflow Diagram
![Workflow Diagram](https://github.com/anand-analytics/Customer-Behaviour-Dashboard/blob/main/Workflow.png)

## 🔄 Project Workflow

### 1. Data Preparation & EDA (Python)
The initial analysis focused on cleaning the `customer_shopping_behavior.csv` dataset, which includes details like demographics, purchase history, and review ratings.
* **Missing Value Imputation:** Null values in `review_rating` were replaced with the median rating **within each specific category** to maintain data accuracy.
* **Standardization:** All column names were converted to **snake casing** (lowercase with underscores) for consistency and easier referencing in SQL.
* **Feature Engineering:** Created an `age_group` column to segment customers into four equal-sized groups and a `purchase_frequency_days` column to convert textual frequencies (e.g., "Weekly") into numeric days.
* **Redundancy Check:** Dropped the `promo_code_used` column as it was redundant with `discount_applied`.

### 2. Advanced Analysis (MySQL)
The cleaned data was loaded into a MySQL database. Several complex business questions were answered through SQL:
* **Revenue Demographics:** Calculated revenue splits by gender and age groups.
* **High-Value Discount Users:** Identified customers who used discounts but still spent more than the average purchase amount.
* **Product Performance:** Ranked products by review ratings and determined which items rely most heavily on discounts to sell.
* **Customer Segmentation:** Used **CTEs and CASE statements** to segment the 3,900 customers into "New," "Returning," and "Loyal" based on purchase frequency.
* **Top Products per Category:** Leveraged **window functions** (`ROW_NUMBER()`) to identify the top three best-selling items within every category.

### 3. Interactive Dashboard (Power BI)
A professional dashboard was built to allow management to track KPIs instantly.
* **Key Metrics:** Developed measures for Total Number of Customers, Average Purchase Amount, and Average Review Rating.
* **Visualizations:** Included revenue by category, sales by age group, and a subscription status breakdown.
* **Interactivity:** Added multiple slicers (Gender, Subscription Status, Category, Shipping Type) to allow for deep-dive exploratory analysis.

## 💡 Key Insights
* **Revenue Drivers:** Young adults represent the most valuable demographic for the business.
* **Shipping Impact:** Customers using express shipping tend to have a higher average spend than standard shipping users.
* **Loyalty Gap:** While repeat buyers are numerous, a significant portion has not yet subscribed to the loyalty program, suggesting the subscription offer may need optimization.

## 📊 Dashboard Preview
![Dashboard Screenshot](https://github.com/anand-analytics/Customer-Behaviour-Dashboard/blob/main/Dashboard.png)

