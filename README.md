# ✈️ Airline Revenue & Occupancy Analysis

---

##  Overview

This project analyzes data from a travel database (`travel.sqlite`) to understand booking trends, aircraft utilization, and revenue patterns. The goal is to improve occupancy rates and profitability by identifying data-driven insights into seat utilization, ticket pricing, and aircraft-specific metrics.

---

##  Business Problem

The airline operates a diverse fleet of aircraft, ranging from small business jets to medium-sized commercial aircraft. However, airlines facing significant financial challenges due to:

- Stricter environmental regulations
- Increased fuel and labor costs
- Rising interest rates and flight taxes

To maintain profitability without sacrificing passenger satisfaction or safety, we aim to:

- Improve occupancy rates
- Optimize ticket pricing
- Identify high and low-performing aircraft

---

## Dataset

The project uses an SQLite database `travel.sqlite`, which includes tables such as:

- `aircraft_data` – Aircraft Code, model, range
- `airports_data` – Airport code, airport name, city, Coordinates, Time zone
- `boarding_passes` – Ticket number, flight ID, boarding number, seat number
- `bookings` – Booking reference, total amount, and booking date
- `tickets` – Ticket-level info, including fare conditions
- `flights` – Flight IDs and aircraft info
- `ticket_flights` – Mapping tickets to flights
- `seats` - Aircraft code, seat number, fare conditions

---

## Tools & Technologies

- **Python**
- **SQLite** (via `sqlite3`)
- **Pandas**
- **Matplotlib / Seaborn** 


---

## 📊 Exploratory Data Analysis (EDA)

- Connects to an SQLite database and extracts table names.
- Iterates through all tables to identify missing values.
- Computes total revenue per aircraft by joining `ticket_flights` and `flights`.
- Derives a new metric: `Inc Total Annual Turnover`.
.
---

## Key Findings

- Some aircraft have significantly more seats but lower occupancy, leading to revenue loss.
- Ticket sales and revenue vary greatly by month and aircraft type.
- Certain fare classes show higher revenue potential, especially during peak periods.
- Several aircraft types consistently underperform in both occupancy and revenue.

---

## Recommendations
- Revise Pricing Strategy: Adjust pricing based on aircraft capacity, demand, and fare conditions. Avoid both underpricing (loss) and overpricing (discouraging customers).
- Target Occupancy Optimization: Focus on increasing the occupancy of medium-sized aircraft with optimal fare plans.
- Dynamic Pricing: Implement seasonal pricing based on booking trends and aircraft performance.
- Maintain Quality & Safety: Profitability should not come at the expense of customer experience or regulatory compliance.

---
# vendor Performance Analysis - Retail Inventory & Sales

_Analyzing vendor efficiency and profitability to  support strategic decision in purchasing and inventory management._

---

# Overview
This project evaluates vendor performance and retail inventory dynamics to drive strategic insights for purchasing, pricing, and inventory optimization. A complete data pipeline was built using SQL for ETL, Python for analysis and hypothesis testing.

---
# Business Problem
Effective inventory and sales management are critical in the retail sector. This project aims to:
-Identify underforming brands needing pricing or promotional adjustments
-Determine vendor contributes to sales and profits
-Analyze the cost-benefit of bulk purchasing 
-Investigate inventory turnover inefficiencies
-Statistically validate differences in vendor profitability


---

# Dataset

-Multiple CSV files located in `/data/` folder (sales, vendors, inventory)
-Summary table created from ingested data and used for analysis

---

# Tools and Technology

-SQL (CTE, Joins, Filtering)
-Python (Pandas, Matplotlib, Seaborn)
-Github

---
# Project Structure
```
vendor-Performance-analysis/
├── README.md/ 
├── scripts/ # Python scripts for ingestion and     analysis
│ ├── ingestion_db.py
│ └── get_vendor_summary.py
├── code/ 
│ ├── exploratory_data_analysis.ipynb
│ └── vender_performance_analysis.ipynb
├── report/ 
├── requirements.txt 

```
---
# Data Cleaning and Preparation<

-Remove transactions with
  -Gross Profit <0
  -Profit Margin <0
  -Salles Quantity <0
-Created summary tables with vendor-level metrics
-Converted data types, handled outliers

---
# Exploratory Data Analysis

**Negative or Zero Values Detected:**
-Gross Profit : Min -52,002.78 (LOSS)
-Profit Margin : Min -∞ (Sales at zero)
-Unsold Inventory : Indicating slow-moving stock

**Correlation Analysis**
-Strong between Purchase Quantity and Sales Quantity(0.99)
-Weak between  Purchase Quantity and Profit
-Negative between Profit Margin and Sales Price(-0.179)

---
# Key Findings 

- **Brands for Promotions**: 198 brands with low sales but high profit margins
- **Top Venders**: Top 10 venders equals to 65.69% of purchases. This infers risk of over-reliance.
-**Bulk Purchasing Impact**: 72% cost savings per unit in large orders
-**Inventory Turnover**: $2.71M worth of unsold inventory
-**Vender Probitability** 
    -High Vendors : Mean Margin = 31.17%
    -Low Vendors  : Mean Margin = 41.55%
-**Hypothesis Testing** Statistically significant difference in profit margin --> distinct vensors Strategies



---
#  Recommendations
-Diversify vendor base to reduce risk 
-Optimize bulk order strategies
-Reprice slow-moving, high-margin brands 
-Clear unsold inventory strategically 
-Improve marketing for underforming vendors

---

**Dilli Adhikari**  
📧 Email: [d.adhikari2049@gmail.com](mailto:d.adhikari2049@gmail.com)  
🔗 LinkedIn: [linkedin.com/in/dilip-adhikari/](https://www.linkedin.com/in/dilip-adhikari/)







