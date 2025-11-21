Delhi AQI Analysis (2022–2025)

This project analyzes the Air Quality Index (AQI) of Delhi over four years — 2022, 2023, 2024, and 2025.
The goal is to understand how AQI levels are changing over time and identify trends that might indicate improvement or deterioration in air quality.


---

Dataset

Column	  Description

date	    Daily date values (2022–2025)
aqi_level	 AQI value for each date


Data was cleaned and uploaded to a BigQuery table:

aqi_project.delhi_aqi_daily




> The dataset was originally stored in multiple Excel files (one per year) and then transformed into a consolidated format for BigQuery and visual dashboards.




---

Tech Stack

Excel (data cleaning & aggregation)

SQL / BigQuery (data storage and queries)

Visualization tool (Looker Studio / Power BI)



---

Objectives

Compare Delhi’s AQI across multiple years

Identify the year with the worst and best air quality

Analyze how minimum, maximum, and average AQI values change over time

Enable interactive filtering through dashboards



---

Dashboard Highlights

📄 Dashboard Report: ./Dashboard_Report.pdf

---

Queries Used (Example)

SELECT
  year,
  MIN(aqi) AS min_aqi,
  MAX(aqi) AS max_aqi,
  AVG(aqi) AS avg_aqi
FROM `dataset.table`
GROUP BY year
ORDER BY year;


---

Insights

2025 shows the lowest maximum AQI so far, indicating improvement.

2024 recorded the highest pollution spike (Max AQI: 494).

AQI fluctuations suggest unstable but slowly improving air quality.



---

Future Work

Add month-wise and season-wise breakdown

Predict future AQI using linear regression

Correlate weather, traffic, and festival events with AQI changes
