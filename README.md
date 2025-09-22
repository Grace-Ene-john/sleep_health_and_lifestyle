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
| Person ID | Gender | Age | Occupation         | Sleep Duration | Quality of Sleep | Physical Activity Level | Stress Level | BMI Category | Blood Pressure | Heart Rate | Daily Steps | Sleep Disorder |
|-----------|--------|-----|--------------------|----------------|------------------|-------------------------|--------------|--------------|----------------|------------|-------------|----------------|
| 1         | Male   | 27  | Software Engineer  | 6.1            | 6                | 42                      | 6            | Overweight   | 126/83         | 77         | 4200        | None           |
| 2         | Male   | 28  | Doctor             | 6.2            | 6                | 60                      | 8            | Normal       | 125/80         | 75         | 10000       | None           |
| 3         | Male   | 28  | Doctor             | 6.2            | 6                | 60                      | 8            | Normal       | 125/80         | 75         | 10000       | None           |

---

## ⚙ Tools Used  
- *Power BI* → Dashboard & Visual Analytics  
- *Excel* → Pivot Tables & Aggregations  
- *SQL* → Data Extraction & Queries  
- *GitHub* → Portfolio & Project Documentation

## Insights

## Sleep Duration & Quality
- Average sleep duration is **~7.1 hours**, which aligns with recommended guidelines.  
- However, many individuals still report **sleep disorders**, indicating **quality matters more than quantity**.  

## Stress & Sleep
- Average stress level: **~5.4 (out of 10)**.  
- Higher stress levels are commonly linked with lower sleep quality and presence of disorders like **insomnia**.  

## Sleep Disorders
- **~40%** of participants have a sleep disorder.  
- **Insomnia and Sleep Apnea** are almost equally prevalent.  
- Participants without disorders generally report **better sleep quality and more consistent sleep duration**.  

## Occupation Influence
- **Healthcare professionals (Nurses & Doctors)** form the largest group.  
- These roles are often associated with **shift work, long hours, and high stress**, which may contribute to **sleep problems**.  

## Gender Balance
- Dataset is nearly balanced: **189 Males vs. 185 Fema**


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
