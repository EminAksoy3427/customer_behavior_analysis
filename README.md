# Customer Shopping Behavior Analysis 🛒📊

## 📌 Project Overview
This project is an end-to-end data analytics study of **3,900 customer transaction records**. The goal was to analyze spending patterns, customer segments, and product preferences to drive strategic business decisions in marketing and inventory management.

The analysis follows a full data pipeline: **Data Cleaning & Engineering (Python)**, **Exploratory Analysis (SQL)**, and **Visual Reporting (Power BI)**, with a final strategic report generated using **NotebookLM**.

---

## 📂 Dataset
* **Source:** Customer Shopping Behavior Dataset
* **Volume:** 3,900 Rows, 18 Columns.
* **Key Features:**
    * **Demographics:** Age, Gender, Location, Subscription Status.
    * **Transactions:** Item Purchased, Category, Purchase Amount (USD), Season, Shipping Type.
    * **Behavior:** Discount Applied, Previous Purchases, Frequency of Purchases, Review Rating.

---

## 🛠️ Tech Stack & Tools
* **Python:** Data cleaning, null imputation, feature engineering (Pandas), and database connection (SQLAlchemy, Psycopg2).
* **SQL (PostgreSQL):** Structured querying to extract key business metrics and customer segmentation.
* **Power BI:** Interactive dashboard for visualizing KPIs and trends.
* **NotebookLM:** Used to synthesize findings into a strategic business presentation.

---

## 🔄 Project Workflow

### 1. Data Processing (Python)
* **Ingestion:** Loaded raw CSV data into Pandas.
* **Cleaning:** Imputed 37 missing values in `Review Rating` using category medians to preserve data integrity.
* **Engineering:**
    * Created `age_group` (Young Adult, Adult, Middle-aged, Senior) for demographic targeting.
    * Converted `frequency_of_purchases` into `purchase_frequency_days` for numerical analysis.
    * Standardized column names to `snake_case` for database compatibility.
* **Loading:** Integrated with PostgreSQL to load the cleaned dataset directly into the database.

### 2. Data Analysis (SQL)
Executed complex queries to answer business questions, including:
* **Revenue by Gender:** Analyzed spend distribution between Male and Female customers.
* **Customer Segmentation:** Classified users into **New**, **Returning**, and **Loyal** segments based on purchase history.
* **Value Analysis:** Identified "High-Spending Discount Users" (customers who use discounts but still spend above the average).
* **Product Performance:** Ranked top products by rating and identified items most frequently purchased with discounts.

### 3. Visualization (Power BI)
Built a "Customer Behavior Dashboard" tracking:
* **KPIs:** Average Purchase Amount ($59.76), Average Rating (3.75), Total Customers (3.9K).
* **Charts:** Revenue by Category, Sales by Age Group, and Subscriber Ratios.

---

## 💡 Key Results & Insights
* **Demographics:** Male customers contributed **55%** of revenue, compared to **45%** from females.
* **Customer Value:** Subscribers have a significantly higher average spend (**$185**) compared to non-subscribers (**$70**), highlighting the critical importance of the subscription model.
* **Loyalty Loop:** Repeat buyers with **>5 purchases** show a strong correlation with subscription status, identifying them as the ideal target for VIP rewards.
* **Shipping Preferences:** Customers using Express shipping have a higher average purchase value (**$90**) than those using standard shipping (**$60**).

---

## 🚀 How to Run

### Prerequisites
* Python 3.x
* PostgreSQL
* Power BI Desktop

### Steps
1.  **Clone the Repo:**
    ```bash
    git clone [https://github.com/yourusername/customer-behavior-analysis.git](https://github.com/yourusername/customer-behavior-analysis.git)
    ```
2.  **Run Python Script:**
    * Install dependencies: `pip install pandas sqlalchemy psycopg2-binary`
    * Update database credentials in `Customer_Behavior_Analysis.ipynb`.
    * Run the notebook to clean data and load it into your local SQL database.
3.  **Execute SQL Analysis:**
    * Open `customer_behavior_analysis_sqlqueries.sql` in your SQL client (pgAdmin/DBeaver).
    * Run the queries to generate insights.
4.  **View Dashboard:**
    * Open the `.pbix` file (if included) to interact with the visualizations.

---

## 📢 Author
* **Name:** [Muhammet Emin Aksoy]
* **Role:** MIS Student
* **Contact:** [eminaks27qgmail.com]
