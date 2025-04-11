# 🚑 AMB-KPI Dashboard - Power BI Project

## 📁 Project Overview

This repository includes a dynamic **Power BI dashboard** titled `AMB-KPI.pbix`, which provides comprehensive insights into ambulance service key performance indicators (KPIs). The dashboard is designed to support operational decision-making through real-time metrics visualization.

## 🧰 Features

- 📆 Trend analysis by day and month
- 🚑 Ambulance count metrics
- 📦 Order tracking per ambulance
- 📍 Distance traveled insights
- 📐 Custom DAX measures for performance evaluation
- 🎯 KPI cards and interactive visuals

## 📌 Key DAX Measures (Examples)

```DAX
-- Total Ambulance Cars
Ambulance Car Count =
DISTINCTCOUNT(Data[Ambulance Plate])

-- Daily Average Orders per Ambulance Car
Daily Avg Orders Per Car =
DIVIDE(COUNTROWS(Data), DISTINCTCOUNT(Data[Ambulance Plate]))

-- Monthly Average Distance Covered
Monthly Avg Distance =
AVERAGEX(
    VALUES(DATE(YEAR(Data[Call Date]), MONTH(Data[Call Date]), 1)),
    DIVIDE(SUM(Data[Distance]), DISTINCTCOUNT(Data[Ambulance Plate]))
)
```

## 📂 Files Included

- `AMB-KPI.pbix` – Power BI report file containing all visuals and DAX measures.

## 🧑‍💻 How to Use

1. Clone or download this repository.
2. Open the `.pbix` file using **Microsoft Power BI Desktop**.
3. Customize visuals or integrate additional data sources as needed.

## 📝 Author

- Dr. Mohamed Wahid Suleiman  
- Data Analysis Engineer @ Microsoft  
- Associate Professor of Educational Technology

---

For any inquiries or suggestions, feel free to reach out.