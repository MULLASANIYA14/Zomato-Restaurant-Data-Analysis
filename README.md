# 🍽️ Zomato Restaurant Analysis Project

## 📌 Project Overview
This end-to-end data analytics project analyzes Zomato restaurant data to uncover customer preferences, restaurant performance, pricing trends, and delivery patterns across multiple countries and cities.

The project was built using:
- SQL → Data cleaning & business analysis
- Excel → Interactive dashboard creation
- Tableau → Data visualization
- Power BI → Business intelligence reporting

---

## 🎯 Business Problem
Zomato wants to understand:

- Which countries have the highest number of restaurants
- Which cuisines are most popular
- Which cities have highest/lowest ratings
- Pricing distribution of restaurants
- Online delivery adoption
- Table booking trends

This helps businesses improve customer satisfaction and make better strategic decisions.

---

## 📂 Dataset Information
Dataset includes:

- Restaurant ID
- Restaurant Name
- Country
- City
- Cuisine
- Ratings
- Votes
- Average Cost for Two
- Online Delivery
- Table Booking
- Opening Date
- Currency

---

## ⚙️ Project Workflow
### 1. Data Cleaning
- Removed duplicates
- Handled missing values
- Standardized columns
- Created lookup tables

### 2. SQL Analysis
- Created calendar table
- Converted currency into USD
- Performed KPI analysis
- Generated business insights

### 3. Dashboard Development
Created dashboards in:
- Microsoft Excel
- Tableau
- Power BI

---

## 📊 Key KPIs
- Total Restaurants
- Total Countries
- Total Cities
- Total Cuisines
- Average Ratings
- Total Votes
- Online Delivery %
- Table Booking %

---

## 🔍 Key Insights
✅ India has the highest number of restaurants  

✅ Identified top-performing cuisines  

✅ Found top 5 cities with highest ratings  

✅ Identified bottom 5 cities with lowest ratings  

✅ Created price segmentation:
- Low
- Medium
- High
- Luxury

✅ Analyzed online delivery trends  

✅ Analyzed table booking trends  

---

## 🛠️ Tools & Technologies
- MySQL
- Microsoft Excel
- Power BI
- Tableau
- Pivot Tables
- Power Query
- Data Visualization

## 📊 DAX Measures Used
Some important DAX calculations:

### Total Restaurants
```bash
Total Restaurants = COUNT('Restaurants'[RestaurantID])
```

### Average Rating
Average Rating = AVERAGE('Restaurants'[Rating])

### Online Delivery Count
Online Delivery Count = 
CALCULATE(
    COUNT('Restaurants'[RestaurantID]),
    'Restaurants'[Has_Online_Delivery] = "Yes"
)

### Year-over-Year Growth
YoY Growth = 
CALCULATE(
    [Total Restaurants],
    SAMEPERIODLASTYEAR('Calendar'[Date])
)

---

## 📈 Dashboards Included
## Excel Dashboard
Interactive KPI dashboard with slicers and charts

### <img width="1265" height="721" alt="Excel Dashboard" src="https://github.com/user-attachments/assets/2e77da1e-f03f-428b-bae2-36a364b4ee72" />



## 📈 Tableau Dashboard Features
* Dynamic country and city filters
* Time-series growth analysis
* Rating heatmap visualization
* Cross-country price comparison
* Interactive drill-down functionality

### <img width="1266" height="707" alt="Tableau Dashboard" src="https://github.com/user-attachments/assets/739886ae-f8eb-42a3-b902-ea5caaf9ff3a" />

## 📊 Power BI Dashboard Features
* KPI Cards (Total Restaurants, Avg Rating)
* Year-wise Restaurant Growth
* Country-wise Distribution Map
* Rating Distribution Analysis
* Online Delivery Comparison
* Interactive Filters & Slicers

### <img width="1142" height="683" alt="PowerBi Dashboard" src="https://github.com/user-attachments/assets/a11664e2-ff0b-4b2b-b8aa-4fc658853dad" />


## 🗃 SQL Analysis Performed
Key queries performed:

* Restaurant count by Year, Quarter, Month
* Country-wise restaurant distribution
* Average rating by country
* Online delivery trend analysis
* Aggregation using GROUP BY and JOIN

## Sample SQL Query
```sql
SELECT 
    cal.Year,
    cal.Quarter,
    cal.MonthFullName AS Month_Name,
    COUNT(*) AS Number_of_Restaurants
FROM main m
JOIN calendar cal
    ON cal.Datekey_Opening = m.Datekey
GROUP BY cal.Year, cal.Quarter, cal.MonthFullName
ORDER BY cal.Year, cal.Quarter;

```

---

## 🚀 Project Outcome
This project helped derive actionable business insights that can help restaurant businesses improve pricing strategies, customer engagement, and operational decisions.


## Project Structure
zomato-restaurant-data-analysis │ ├── ZOMATO_PROJECT_INSIGHTS.sql ├── ZOMATO_ANALYSIS_EXCEL.xlsx ├── ZOMATO_ANALYSIS_POWERBI.pbix ├── TABLEAU_ZOMATO_DASHBOARD.twbx ├── POWERBI_ZOMATO_DASHBOARD.png ├── TABLEAU_ZOMATO_DASHBOARD.png ├── ZOMATO_ANALYSIS_EXCEL_DASHBOARD.png └── README.md

---

## 👤 Author
Saniya Mulla
LinkedIn Profile Link -https://www.linkedin.com/feed/
