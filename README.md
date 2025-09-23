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
To analyze lifestyle, demographic, and health factors that influence sleep quality and the prevalence of sleep disorders (Insomnia & Sleep Apnea). 
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

### Sleep Duration & Quality
- Average sleep duration is **~7.1 hours**, which aligns with recommended guidelines.  
- However, many individuals still report **sleep disorders**, indicating **quality matters more than quantity**.  

### Stress & Sleep
- Average stress level: **~5.4 (out of 10)**.  
- Higher stress levels are commonly linked with lower sleep quality and presence of disorders like **insomnia**.  

### Sleep Disorders
- **~40%** of participants have a sleep disorder.  
- **Insomnia and Sleep Apnea** are almost equally prevalent.  
- Participants without disorders generally report **better sleep quality and more consistent sleep duration**.  

### Occupation Influence
- **Healthcare professionals (Nurses & Doctors)** form the largest group.  
- These roles are often associated with **shift work, long hours, and high stress**, which may contribute to **sleep problems**.  

### Gender Balance
- Dataset is nearly balanced: **189 Males vs. 185 Females**


---

## Visualization
<img width="931" height="101" alt="image" src="https://github.com/user-attachments/assets/c049963c-31dd-4203-baa7-eeff94cff4e5" />
<img width="943" height="479" alt="image" src="https://github.com/user-attachments/assets/5c38b213-e9f9-41ca-9fcb-f5410e5bf5b0" />


---

## SQL
The following SQL queries were used to extract key insights from the dataset
   
```sql
---Average Sleep Duration by Occupation---
SELECT 
    Occupation,
    ROUND(AVG([Sleep Duration]), 2) AS Avg_Sleep_Hours
FROM SleepData
GROUP BY Occupation
ORDER BY Avg_Sleep_Hours DESC;
```

```sql
---Sleep Disorder Distribution by Gender---
SELECT 
    Gender,
    [Sleep Disorder],
    COUNT(*) AS Num_People
FROM SleepData
GROUP BY Gender, [Sleep Disorder]
ORDER BY Gender, Num_People DESC;
```

## Profile
