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

- `bookings` – Booking reference, total amount, and booking date
- `tickets` – Ticket-level info including fare conditions
- `flights` – Flight IDs and aircraft info
- `ticket_flights` – Mapping tickets to flights
- `seats` – Seat configuration per aircraft

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

## Key Findings

- Some aircraft have significantly more seats but lower occupancy, leading to revenue loss.
- Ticket sales and revenue vary greatly by month and aircraft type.
- Certain fare classes show higher revenue potential, especially during peak periods.
- Several aircraft types consistently underperform in both occupancy and revenue.

## Recommendations
- Revise Pricing Strategy: Adjust pricing based on aircraft capacity, demand, and fare condition. Avoid both underpricing (loss) and overpricing (discouraging customers).
- Target Occupancy Optimization: Focus on increasing occupancy of medium-sized aircraft with optimal fare plans.
- Dynamic Pricing: Implement seasonal pricing based on booking trends and aircraft performance.
- Fleet Adjustment: Consider phasing out consistently underperforming aircraft types or routes.
- Maintain Quality & Safety: Profitability should not come at the expense of customer experience or regulatory compliance.


