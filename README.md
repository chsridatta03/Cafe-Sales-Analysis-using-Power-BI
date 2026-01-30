# Cafe Sales Analysis – Excel and Power BI

## Project Overview
This project analyzes cafe sales transaction data to evaluate revenue performance, product contribution, customer purchasing behavior, and operational effectiveness.

The project follows a realistic analytics workflow:
- Data cleaning and validation in **Excel**
- Data modeling, analysis, and dashboarding in **Power BI**

The final output is a one-page executive dashboard designed to support business decision-making.

---

## Table of Contents
- [Project Overview](#project-overview)
- [Business Objective](#business-objective)
- [Data Description](#data-description)
- [Tools Used](#tools-used)
- [Data Cleaning in Excel](#data-cleaning-in-excel)
- [Power BI Analysis](#power-bi-analysis)
- [Business Questions and Answers](#business-questions-and-answers)
- [Dashboard Design](#dashboard-design)
- [Key Insights](#key-insights)
- [Recommendations](#recommendations)
- [Repository Structure](#repository-structure)
- [References](#references)

---

## Business Objective
The objective of this project is to answer core business questions:
- How is overall revenue performing?
- Which items and channels drive revenue?
- How do customers behave per transaction?
- Are there differences between weekday and weekend sales?
- What data quality issues affect reporting accuracy?

The dashboard is designed for management review and operational planning.

---

## Data Description
The dataset represents transaction-level café sales data.

### Key Fields
- Transaction ID  
- Transaction Date  
- Item  
- Quantity  
- Price Per Unit  
- Total Spent  
- Location  
- Payment Method  

Each row represents a single item within a transaction.

---

## Tools Used
- **Microsoft Excel**
  - Data cleaning and validation
  - Handling missing and invalid values
  - Logical derivations using formulas
- **Power BI Desktop**
  - Data modeling
  - DAX measures and calculated columns
  - Interactive dashboard creation
- **GitHub**
  - Version control
  - Project documentation

---

## Data Cleaning in Excel
All data cleaning was completed in Excel before loading into Power BI.

### Cleaning Actions
- Standardized categorical fields:
  - Item
  - Location
  - Payment Method

 
  

- Removed invalid records:
  - Missing Transaction Date
  - Quantity ≤ 0
  - Total Spent ≤ 0
- Filled missing numeric values only when logically derivable
- Flagged unresolved values as `Unknown`
- Converted all columns to appropriate data types
- Performed column-level missing value analysis

<img width="1440" height="540" alt="image" src="https://github.com/user-attachments/assets/21b3308a-6e0c-46ff-b04c-bec1af7525c9" />


<img width="255" height="227" alt="Screenshot 2026-01-29 220038" src="https://github.com/user-attachments/assets/c16d3d65-abd5-4ffb-9b45-cdb8e0c9dec5" /> -> <img width="309" height="282" alt="Screenshot 2026-01-29 220410" src="https://github.com/user-attachments/assets/69b4fabf-bd88-4d71-8dbc-ae805a9645b6" />

<img width="578" height="325" alt="Screenshot 2026-01-29 220921" src="https://github.com/user-attachments/assets/a9faabdc-171b-437f-bf54-9494376ce19a" /> -> <img width="483" height="264" alt="image" src="https://github.com/user-attachments/assets/2c882de7-be6e-41a5-bb41-c956d11afb96" />

**Guiding principle:**  
No assumptions and no random imputation. Only business-justified logic was applied.

---

## Power BI Analysis

### Data Model
- Single fact table
- Cleaned Excel data used as source
- No unnecessary relationships
<img width="673" height="507" alt="image" src="https://github.com/user-attachments/assets/830dd557-027b-4fd9-8159-6b5281281d36" />


### Calculated Columns
- Weekday / Weekend derived from Transaction Date
<img width="764" height="146" alt="image" src="https://github.com/user-attachments/assets/8be1214c-8ea9-4783-aa5c-3bf6bbd51a02" />
<img width="494" height="526" alt="image" src="https://github.com/user-attachments/assets/21bac3ed-6ab7-41bf-a6cd-128fc6aab59c" />



### DAX Measures
- Total Revenue  
- Total Transactions  
- Total Items Sold  
- Average Order Value  
- Revenue per Transaction  
- Items per Transaction  

All measures respect slicers and filter context.

---

## Business Questions and Answers

### 1. How is overall revenue performing?
Revenue remains stable across the analyzed period with no major volatility.

**Business meaning:**  
The business is operationally stable, but growth opportunities exist.

---

### 2. Is revenue growing over time?
Revenue fluctuates month to month without a strong upward trend.

**Business meaning:**  
Growth initiatives such as promotions or new offerings are required.

---

### 3. Which items contribute the most to revenue?
Higher-priced items such as Salad, Smoothie, and Sandwich generate the highest revenue.

**Business meaning:**  
Revenue is driven by item value, not just volume.

---

### 4. Do high-volume items also generate high revenue?
Items like Coffee sell frequently but contribute less to total revenue.

**Business meaning:**  
High sales volume does not equal high revenue contribution.

---

### 5. How do customers behave per transaction?
Customers typically purchase multiple items per transaction.

**Business meaning:**  
There is strong potential for cross-selling and bundled offers.

---

### 6. Which sales channel performs better?
In-store sales contribute the largest share of revenue.  
A portion of records contain `Unknown` location values.

**Business meaning:**  
In-store is the primary channel, but data capture quality must improve.

---

### 7. Are weekends different from weekdays?
Sales patterns differ between weekdays and weekends.

**Business meaning:**  
Staffing and promotions should be planned by day type.

---

### 8. Are there data quality risks?
Some records contain `Unknown` values and some transactions were excluded due to missing mandatory fields.

**Business meaning:**  
Insights are reliable, but improved data capture will increase confidence.

---

## Dashboard Design
The project delivers a single-page executive Power BI dashboard.

<img width="1323" height="577" alt="image" src="https://github.com/user-attachments/assets/be69c2c2-0420-410e-ba49-903239cd3b71" />


### Dashboard Components
- KPI cards for business health
- Monthly revenue trend
- Item-wise revenue performance
- Channel comparison (In-store vs Takeaway)
- Customer basket behavior metrics
- Data quality indicators

The dashboard is built for quick decision-making and clarity.

---

## Key Insights
- Revenue is stable but shows limited growth
- Premium items drive revenue more than high-volume items
- Customers frequently buy multiple items per visit
- In-store sales outperform takeaway
- Data quality gaps reduce channel-level confidence

---

## Recommendations
- Focus promotions on high-revenue items
- Introduce bundle offers to increase basket size
- Improve POS data capture for Location
- Plan staffing using weekday vs weekend trends
- Track `Unknown` values as a data quality KPI

---

## Repository Structure
