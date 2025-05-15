# 🧠 Customer Segmentation Analytics – AdventureWorks Case Study

**Author:** Minh Phan  
**Tools Used:** SQL (BigQuery), Jupyter Notebook (as SQL interface)

---

## 📌 Project Overview

This client-facing analytics project investigates customer behavior from the AdventureWorks 2012 database using SQL-based querying and visualization. The objective is to identify meaningful customer segments and provide actionable recommendations for retention and marketing optimization.

The analysis is structured across two notebooks:
- **Notebook 1:** Customer segmentation using RFM scoring (Recency, Frequency, Monetary).
- **Notebook 2:** Advanced SQL-based profiling based on geography, product preferences, and revenue patterns.

---

## 🎯 Objectives

- Segment customers based on their purchasing behavior and transaction history.
- Identify high-value, high-frequency, at-risk, and inactive customer groups.
- Extract business insights from geographic and category-level data.
- Recommend data-driven actions for marketing and sales strategy refinement.

---

## 📦 Dataset Description

- **Source:** Microsoft AdventureWorks 2012 Database
- **Storage:** Google BigQuery
- **Access Tool:** Jupyter Notebook (for SQL code execution)

**Tables Used:**

- `Customer`
- `SalesOrderHeader`
- `SalesOrderDetail`
- `Product`
- `ProductCategory`
- `ProductSubcategory`
- `SalesTerritory`
- `TopTerritories` (custom logic output)

These tables were queried directly in BigQuery using standard SQL and joined to derive customer-level and segment-level metrics.

---

## 🧮 Methodology

### 1️⃣ RFM Analysis (`AdventureWork RFM Analytics.ipynb`)

- **Recency:** Days since last transaction
- **Frequency:** Number of orders placed
- **Monetary Value:** Total revenue generated per customer

Customers were ranked into quintiles (scores 1–5), and composite scores were used to classify them into behavioral segments:

- 🏆 Champions  
- 🔁 Loyal Customers  
- ⚠️ At-Risk Customers  
- 🚨 Hibernating Customers  
- 📈 Potential Loyalists

Each segment's revenue, category preference, and territory distribution were analyzed.

---

### 2️⃣ SQL-Based Profiling (`Customer_Segment_Analysis_Report.ipynb`)

This notebook leverages SQL to explore deeper insights including:

- Geographic concentration of customer types
- Monthly and seasonal sales behavior
- Product category engagement across territories
- Cross-category purchasing trends
- Top revenue-generating customers per region

SQL operations include:
- Complex `JOIN`s
- `GROUP BY` aggregations
- Window functions (`RANK`, `ROW_NUMBER`)
- Conditional filtering (`CASE`, `HAVING`)
- Subqueries and CTEs

---

## 📊 Key Insights

- The **top 10% of customers generate over 50% of total sales**.
- **Champions and Loyal Customers** favor high-end product categories like **Mountain Bikes** and **Road Frames**.
- **Territory 1 and 4** have the largest concentration of high-value customers.
- **Product Subcategories** such as Gloves and Tires have high cross-purchase frequency, suggesting upselling potential.
- **At-Risk customers** showed a 40% drop in order frequency over the last two quarters.

---

## 💡 Strategic Recommendations

### 🎯 For Champions:
- Offer **early access to new products**
- Launch **VIP loyalty programs**

### 🎯 For At-Risk Segments:
- Trigger **personalized win-back campaigns**
- Provide **time-sensitive discounts**

### 🎯 For Regular Buyers:
- Promote **product bundles** and cross-sell offers
- Use **territory-specific campaigns** based on local buying trends

---

## 🛠 Tools & Technologies

| Tool            | Purpose                            |
|-----------------|------------------------------------|
| SQL (BigQuery)  | Data extraction and transformation |
| Jupyter Notebook| SQL development and reporting      |
| Markdown        | Documentation and presentation     |

---

## 📈 Deliverables

- Clean and reproducible SQL queries in notebook format
- Segment-level summaries and charts (SQL-based visualization where available)
- Territory-specific breakdowns
- Actionable marketing strategies linked to each segment

---

## ✅ Business Impact

This analysis enables data-driven decision-making by:

- Identifying high-impact customer groups
- Reducing churn via tailored outreach
- Enhancing customer lifetime value (CLTV)
- Optimizing marketing budgets and targeting

---

## 📂 File Structure

```bash
📁 AdventureWorks-Segmentation
├── AdventureWork RFM Analytics.ipynb       # RFM scoring and segmentation
├── Customer_Segment_Analysis_Report.ipynb  # SQL-based customer profiling
└── README.md                               # Project documentation and summary
