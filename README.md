# Instacart Market Basket Analysis & Reorder Prediction
### Scalable Data Pipeline & ML with PySpark and Databricks

## 📌 Project Overview
This project involves building a complete Big Data pipeline to analyze over **32 million grocery orders**. The goal was to uncover consumer shopping patterns and build a machine learning model to predict whether a customer will reorder a product based on their shopping behavior.

## 🛠 Tech Stack
* **Language:** Python (PySpark)
* **Environment:** Databricks Community Edition
* **Storage:** Delta Lake (Medallion Architecture)
* **ML Library:** PySpark MLlib
* **Query Language:** Spark SQL

## 🚀 Key Achievements
### 1. Large-Scale Data Engineering
* Ingested and managed a **32.4 Million row dataset**.
* Implemented a **Medallion Architecture** (Raw -> Bronze -> Silver) using Delta Tables.
* Handled data quality issues by imputing **200,000+ missing values** and sanitizing malformed records using `try_cast` logic.

### 2. Market Basket & Behavioral Analysis
* **Peak Shopping Times:** Identified that shopping peaks between **10:00 AM and 4:00 PM**, particularly on weekends.
* **Product Associations:** Used **SQL Self-Joins** to find the most frequent product pairings (e.g., Organic Bananas and Organic Strawberries).
* **Loyalty Stats:** Calculated department reorder ratios, finding that **Dairy/Eggs (67%)** and **Produce (65%)** have the highest customer retention.

### 3. Machine Learning Model
* **Model:** Logistic Regression.
* **Features:** Day of week, hour of day, days since last order, and cart position.
* **Accuracy:** **59.81%** on a test set of 1 million rows.
* **Key Insight:** Discovered that **Cart Position** is the strongest predictor of a reorder (Negative Coefficient: -0.037), meaning essential items are usually added to the cart first.

## 📊 Visualizations


<img width="2012" height="800" alt="visualization-5" src="https://github.com/user-attachments/assets/5adea659-5dbb-42c1-93b9-9540ff5ef7e9" />
<img width="2012" height="800" alt="visualization-4" src="https://github.com/user-attachments/assets/dceb1baf-c1f3-4d88-a59d-1e6d0e5c797b" />

<img width="2012" height="800" alt="visualization" src="https://github.com/user-attachments/assets/e7846d00-5564-4f7b-abf7-4ba54e90e820" />

<img width="2012" height="800" alt="visualization-2" src="https://github.com/user-attachments/assets/8015e197-b99c-4f1c-9e2c-a6f510447875" />


* **Hourly Heatmap:** Shows peak traffic zones.
* **Department Pie Chart:** Shows Produce and Dairy dominating sales.
