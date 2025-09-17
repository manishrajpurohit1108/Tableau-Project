# 🏨 Hotel Booking Data Analysis - Tableau Project

## 📌 Project Overview
This project analyzes hotel booking data to uncover insights about **customer booking patterns** and **cancellation behavior**.  
The analysis was done in **Tableau**, and the project is structured into **two dashboard pages**:  
- **Bookings Analysis Page** → Focus on overall bookings by various factors.  
- **Cancellations Analysis Page** → Focus on cancellation trends and root causes.  

---

## 🎯 Problem Statement / Goal  
The objective of this project is to analyze hotel booking data and provide actionable insights related to bookings, cancellations, customer types, market segments, and hotel categories.

The dashboards help in monitoring booking trends, cancellation patterns, customer behavior, and geographic contributions to support data-driven decision-making for reducing cancellations and improving hotel performance.

---

## 📂 Dataset Details  
- **Dataset Name:** Hotel Booking  
- **Source:** [Dataset](https://github.com/manishrajpurohit1108/Tableau-Project/blob/main/hotel_booking.csv) from Kaggle (1 lakh+ rows)
- **Columns (36 total):** 
 
The dataset contains booking information for **City Hotels** and **Resort Hotels** with attributes like:  
- Hotel type, lead time, arrival date  
- Stay duration (weekdays & weekends)  
- Number of adults, children, babies  
- Market segment & distribution channel  
- Deposit type, room type (reserved vs assigned)  
- ADR (Average Daily Rate), customer type  
- Cancellation flags and reservation status
- Name, email, phone number and last 4 digits of card of the guest  

---

## 🛠️ Data Preparation
Steps taken before visualization:  
1. **Loaded dataset** into Tableau.  
2. **Data Cleaning**:  
   - Removed rows with negative ADR values (impossible cases → data error).  
3. **Data Type Checks**: Ensured each field had correct data type (Date, String, Number).  
4. **New Column Created**:  
   - **Booking Start Date** (combined from Arrival Year, Month, Week Number, Day).  
5. **Calculated Fields Created**:  
   - **Total Bookings** → Count of all bookings.  
   - **Total Cancellations** → Count where `is_canceled = 1`.  
   - **Average Daily Rate (ADR)** → `AVG([adr])`. (Sum of all lodging transactions by customer during their stay / Total stay duration -nights)  
   - **Average Stay Duration (Nights)** → `AVG([stays_in_week_nights] + [stays_in_weekend_nights])`.  
   - **Cancellation Rate %** → `(Total Cancellations / Total Bookings) * 100`.  

---

## 📌 Dashboard Design

### 🔹 Common Features (Both Pages)
- **KPIs (Cards at Top)**:  
  - Total Bookings  
  - Cancellation Rate %  
  - Average Daily Rate (ADR)  
  - Average Stay Duration (Nights)  
- **Trend (Line) Chart**: Monthly trend of **Total Bookings vs Cancellations**.  
- **Filters**:  
  - Year  
  - Month  
  - Hotel Type  
  - Customer Type  
- **Navigation Button**: Switch between Page 1 (Bookings) and Page 2 (Cancellations).  

---

### 📍 Page 1: Bookings Analysis
Shows overall booking trends and breakdowns:  
- **Bookings by Market Segment** → Lollipop Bar Chart  
- **Bookings by Country** → Map  
- **Bookings by Hotel Type** → Donut Chart  
- **Bookings by Customer Type** → Donut Chart  
- **Bookings by Room Type** → Line Chart with Markers  

📸 *Dashboard Screenshot:*  
![Bookings Dashboard (Page 1)](https://github.com/manishrajpurohit1108/Tableau-Project/blob/main/Dashboard%20Page%201.png)  

---

### 📍 Page 2: Cancellations Analysis
Focuses on cancellations across multiple dimensions:  
- **Cancellations by Market Segment** → Lollipop Bar Chart  
- **Cancellations by Country** → Map  
- **Cancellations by Hotel Type** → Donut Chart  
- **Cancellations by Customer Type** → Donut Chart  
- **Cancellations by Room Type** → Line Chart with Markers  

📸 *Dashboard Screenshot:*  
![Cancellations Dashboard (Page 2)](https://github.com/manishrajpurohit1108/Tableau-Project/blob/main/Dashboard%20Page%202.png)  

---

## 🔑 Key Insights
- **City Hotels** received more bookings compared to Resort Hotels, but also faced higher cancellation rates.
- The overall **cancellation rate** is **~37%**, which is significantly high for the industry. 
- **Transient customers** (individual travelers) contributed the highest number of cancellations compared to contract or group customers however had the highest bookings as well. 
- Bookings from **Online Travel Agencies (OTA/TA-TO segment)** dominated overall reservations but also contributed the largest share of cancellations.
- **Direct and Corporate bookings** showed comparatively lower cancellation rate, making them more reliable channels. 
- Cancellations are higher for certain **room types** (especially Type A).    
- Some countries show disproportionately high cancellation percentages.  

---

## 🛠️ Tools Used
- **Tableau** (Dashboarding & Visual Analytics)  

---

## 📁 Project Tableau File:
[Project File](https://github.com/manishrajpurohit1108/Tableau-Project/blob/main/Hotel%20Booking%20Analysis%20Project.twbx)
