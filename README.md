
# ✈️ Travel Database Analysis
Data Analysis And Report For Enhancing Profit  In The Aviation Industry Using Python and SQL.
This project connects to a SQLite database `travel.sqlite`, checks for missing values in all tables, calculates total revenue by aircraft, and computes a derived metric using occupancy rates.

---

## 🛠️ Features

- Connects to an SQLite database and extracts table names.
- Iterates through all tables to identify missing values.
- Computes total revenue per aircraft by joining `ticket_flights` and `flights`.
- Derives a new metric: `Inc Total Annual Turnover`.

---

## 📁 Project Structure

travel-analysis/
├── travel.sqlite # SQLite database
├── occupancy_rate.csv # External occupancy data
├── analysis.py # Python script for analysis
├── README.md # Project documentation
