# sleep_health_and_lifestyle

## Table of Contents
-  [Project Overview](#-project-overview)
- [Dataset Overview](#-dataset-overview)
- [Tools Used](#-tools-used)
- [Key Insights](#-key-insights)
- [Visualization](#-visualizations)
- [SQL Queries](#-sql-queries)
- [Profile](#--profile)

## Project Overview  
This project analyzes mobile phone sales data sourced from Kaggle.  
The goal is to uncover customer purchasing trends, payment preferences, and product performance across different demographics and locations.  

Dashboards and reports were built using *Power BI, Excel, and SQL* to provide actionable business insights.  

---

## 📂 Dataset Overview  
- *Source:* [Kaggle - Sleep, Health and Lifestyle Dataset](https://www.kaggle.com/datasets/uom190346a/sleep-health-and-lifestyle-dataset)   
- *Format:* CSV  
- *Size:* 1000+ transactions  

### Records (first 3 transactions)
| InvoiceNo | StockCode | Description  | Quantity | InvoiceDate | UnitPrice | CustomerID | Country |
|-----------|-----------|--------------|----------|-------------|-----------|------------|---------|
| 537226    | 22728     | mobile a     | 6        | 12/1/2010   | 3.75      | 15311      | UK      |
| 537227    | 22729     | mobile b     | 8        | 12/1/2010   | 5.00      | 15312      | UK      |
| 537228    | 22730     | mobile c     | 2        | 12/1/2010   | 7.50      | 15313      | UK      |

---

## ⚙ Tools Used  
- *Power BI* → Dashboard & Visual Analytics  
- *Excel* → Pivot Tables & Aggregations  
- *SQL* → Data Extraction & Queries  
- *GitHub* → Portfolio & Project Documentation

## Key Insights
- *Total Revenue:* 40.22M  
- *Top Gender by Sales:* Female & Other (13.47M each)  
- *Top Payment Method:* Credit Card (11.30M)  
- *Best-Selling Model:* "huge" (283K revenue)  
- *Top Location by Sales:* Lake Amanda (186K)  
- *Top Mobile Model:* Huge model (282.86K revenue).  
- *Gender Split:* Sales are evenly distributed across Male, Female, and Other.  
- *Online Payments:* Strong growth, generating 10.28M in revenue.  

---

## Visualization

<img width="1396" height="725" alt="Screenshot 2025-09-22 112548" src="https://github.com/user-attachments/assets/f80a3e73-d58a-47ca-945a-ab99b6b62394" />

---

## SQL
The following SQL queries were used to extract key insights from the dataset
   
```sql
---Find the most expensive brand----
SELECT TOP 1 Brand, MAX(UnitPrice) AS HighestPrice
FROM mobile_sales
GROUP BY Brand
ORDER BY HighestPrice DESC;
```

## Profile
