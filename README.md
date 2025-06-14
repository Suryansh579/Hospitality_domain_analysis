# 📊 Hospitality Revenue Dashboard - AtliQ Grands

## 🚀 Overview

This Power BI project provides an end-to-end interactive dashboard and analytical solution for **AtliQ Grands**, a luxury hotel chain in India. Due to increased competition and ineffective past decisions, AtliQ Grands experienced a decline in market share. This dashboard was built to assist the **Revenue Management Team** in making data-driven decisions to optimize bookings, increase occupancy, and enhance overall revenue performance.

---

## 🏨 Domain & Objective

- **Industry**: Hospitality  
- **Function**: Revenue Management  
- **Goal**: Deliver actionable insights and key performance metrics to help AtliQ Grands regain market share and improve operational efficiency.

---

## 📁 Dataset Description

The dashboard uses the following 5 CSV files:

1. **`dim_date.csv`**  
   - Provides daily date-level granularity with derived attributes like `week_no`, `day_type`.

2. **`dim_hotels.csv`**  
   - Details about each hotel such as `property_id`, `category` (Luxury/Business), and `city`.

3. **`dim_rooms.csv`**  
   - Contains information on room types and their classes (`Standard`, `Elite`, `Premium`, `Presidential`).

4. **`fact_aggregated_bookings.csv`**  
   - Aggregated booking metrics like `successful_bookings` and `capacity` at room-category and hotel level.

5. **`fact_bookings.csv`**  
   - Granular booking information including `booking_date`, `check_in_date`, `booking_status`, `revenue_generated`, and `revenue_realized`.

---

## 📐 Data Modeling & DAX Implementation

### 🔧 Calculated Columns

| Column Name | Description |
|-------------|-------------|
| `wn` | Week number from date |
| `day type` | Categorizes days into `Weekday` or `Weekend` based on DAX logic |

---

### 📊 Key Measures & KPIs

| Measure Name | Description |
|--------------|-------------|
| `Revenue` | Total revenue realized |
| `Total Bookings` | Total number of bookings |
| `Total Capacity` | Sum of all room capacities |
| `Total Successful Bookings` | Count of successful bookings |
| `Occupancy %` | Ratio of successful bookings to room capacity |
| `Average Rating` | Average customer rating |
| `No of Days` | Total days in data (May–July = 92) |
| `Cancellation %` | Cancelled bookings percentage |
| `No Show Rate %` | No show bookings percentage |
| `Realisation %` | 1 - (Cancellation % + No Show Rate %) |
| `Booking % by Platform` | Proportional booking count per platform |
| `Booking % by Room Class` | Booking distribution by room class |
| `ADR` | Average Daily Rate = Revenue / Total Bookings |
| `RevPAR` | Revenue per Available Room = Revenue / Total Capacity |
| `DBRN` | Daily Booked Room Nights = Total Bookings / No of Days |
| `DSRN` | Daily Sellable Room Nights = Total Capacity / No of Days |
| `DURN` | Daily Utilized Room Nights = Checked Out Bookings / No of Days |

---

### 📈 Week-over-Week (WoW) Change Metrics

These metrics help track performance trends weekly:

- `Revenue WoW change %`
- `Occupancy WoW change %`
- `ADR WoW change %`
- `RevPAR WoW change %`
- `Realisation WoW change %`
- `DSRN WoW change %`

Each metric uses `SELECTEDVALUE()` and `CALCULATE()` filters on week number to compare current and previous weeks.

---

## 📌 Dashboard Features

- Fully interactive filters for **city**, **hotel category**, **room class**, and **booking platform**
- Dynamic KPIs and visuals for **Revenue**, **Occupancy**, **Bookings**, **Cancellation Trends**
- Time-series line charts to show **WoW changes**
- Drill-downs by **date**, **hotel**, and **room category**

---

## 💡 Additional Insights

Beyond stakeholder requirements, the dashboard also uncovers:

- Booking behavior by **platform preference**
- Revenue leakage due to **cancellations** and **no-shows**
- Customer satisfaction trends through **rating analysis**
- Utilization metrics (**DBRN**, **DSRN**, **DURN**) to optimize operational planning

---

## 📘 Technologies Used

- Power BI Desktop  
- DAX (Data Analysis Expressions)  
- Data Modeling with star schema  
- CSV as data source

---

## 👤 Role & Contributions

As the sole data analyst on the project, I:

- Engineered the entire **data model**
- Developed all **DAX measures and calculated columns**
- Created an interactive and intuitive **Power BI dashboard**
- Generated actionable insights to empower the **Revenue team**

---

## 📎 License

This project is intended for educational and demonstration purposes only.

---

## 📬 Contact

For any queries or collaboration, feel free to connect via [LinkedIn](https://linkedin.com) or email.
