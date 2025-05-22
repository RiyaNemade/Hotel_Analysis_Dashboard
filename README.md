# 🏥 Hospital Management Analysis - Power BI Dashboard

## 📊 Project Objective

The goal of this project is to analyze hospital booking data to uncover trends, optimize resource utilization, and improve overall hospital performance using an interactive Power BI dashboard. This analysis helps hospital management make data-driven decisions in areas such as revenue, occupancy, cancellations, platform performance, and regional operations.

---

## 📁 Dataset Overview

The dataset contains hospital room booking data across different cities, room categories, booking platforms, and dates. Key columns include:

- Booking ID, Booking Date, City, Room Category
- Booking Platform, Total Rooms, Total Bookings
- Revenue Generated, Revenue Realized
- Occupancy Rate, Cancellation Rate

---

## 🔧 Step-by-Step Process

### 1️⃣ Data Cleaning (Performed in Power Query)

- Removed unnecessary or duplicate columns (e.g., booking ID after aggregation).
- Converted date columns into appropriate date format.
- Replaced null or blank values with "Others" or 0 based on context.
- Standardized column names for consistency (e.g., Booking_Date, Total_Bookings).

### 2️⃣ Data Transformation

- Created calculated Measure:
  - Occupancy Rate = Total_Bookings / Total_Capacity
  - Cancellation Rate = Cancelled_Bookings / Total_Bookings
  - MOM % = DIVIDE([MTD Revenue]-[Previous month revenue],[Previous month revenue])
- Extracted Day of Week, Month, and Year from the booking date.

### 3️⃣ Data Modeling

- Built a star schema with the following structure:
  - Fact Table: Fact_Booking, fact_aggregated_Booking
  - Dimension Tables: Calender, dim_date, dim_hotel, dim_room
- Managed relationships between tables using foreign keys (e.g., DateKey, CityID)

---

## 📊 Dashboard Design

Two interactive dashboards were created using slicers, KPI cards, charts, and maps:

### 📄 Page 1: Booking Overview

**Page Navigation Name**: Booking Overview

#### 📌 Key Features:
- KPIs: Total Bookings (233K), Revenue Realized (2B), Occupancy Rate (57.9%)
- Line Chart: Revenue Realized by Day
- Bar Chart: Total Bookings vs Total Capacity by City
- Bar Chart: Daily Booking Trends
- Map Visual: Total Bookings by City (Geographic View)
- Area Chart: Revenue Generated vs Revenue Realized by Property

### 📄 Page 2: Performance Insights

**Page Navigation Name**: Performance Insights

#### 📌 Key Features:
- KPIs: Occupancy Rate, Cancellation Rate
- Treemap: Total Guests by Booking Platform
- Donut Chart: Cancellation Rate % by Platform
- Bar Chart: Total Bookings by Day
- Column Chart: Occupancy Rate by City

---

## 📈 Key Insights:

| Insight | Explanation |
|--------|-------------|
| 🏨 Occupancy Rate is at 57.9% | Indicates scope to improve utilization of hospital rooms. |
| 💰 Revenue Realized: ₹2 Billion | Signifies strong earnings, but gap between generated vs realized revenue highlights payment collection inefficiencies. |
| ❌ Cancellation Rate is 24.83% | High cancellation rate requires better customer communication or booking platform review. |
| 🌆 Delhi has the highest occupancy (60.5%) | Reflects optimal usage of hospital capacity in that region. |
| 📅 Weekends show highest bookings (22K on Sunday/Monday) | Indicates higher patient intake at week start. |
| 🌐 Majority of bookings (112K) come from "Others" platform group | Implies dependency on less-tracked platforms; need for partnership strategy. |
| 🛑 MakeMyTrip and Tripster show highest cancellation rates (14.4%) | Indicates reliability issues with certain platforms. |
| 🌆 Mumbai has the highest number of total bookings (43K), but still has 32K unutilized capacity.
| 🌐 Sunday and Monday are peak booking days (22K each). | optimized staffing and promotional offers based on high/low traffic days.

---

## 🧩 Tools & Skills Used

- Power BI Desktop
- Power Query (M language)
- Data Modeling (Star Schema)
- DAX (for KPIs and Measures)
- Data Cleaning & Transformation
- Visual Storytelling & Dashboard Design

---

## 🎯 Real-World Impact

This dashboard can help hospital administrators:
- Optimize resource allocation city-wise
- Improve booking channel performance
- Reduce cancellations through proactive strategy
- Track revenue health over time
- Make informed marketing and pricing decisions

---

## 📸 Dashboard Snapshots

![Dash1](https://github.com/user-attachments/assets/5887d5c5-91fd-43bf-aa8f-b1b0f38e6935)
![Dash1](https://github.com/user-attachments/assets/6f2790a6-e0c5-4f6f-a559-8ce651f22696)

