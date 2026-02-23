# Public Transport Trips – Exploratory Data Analysis (EDA)

This project presents a comprehensive exploratory data analysis (EDA) of **MetroMove Transit Solutions**, a fictional public transportation provider operating buses, trains, ferries, and trams across multiple cities. The goal is to transform raw, inconsistent trip records into actionable insights that support operational efficiency, revenue optimization, and improved passenger experience.

---

## **Project Overview**

MetroMove manages thousands of daily trips but lacked visibility into:

- Passenger behaviour  
- Transport mode performance  
- Revenue patterns  
- Route efficiency  
- Time‑based demand fluctuations  

This project cleans, analyzes, and visualizes **1,000 public transport trip records**, uncovering patterns that can guide data‑driven decision‑making.

---

## **Business Context**

MetroMove’s mission is to deliver **efficient, affordable, and timely** public transportation.  
However, messy and incomplete data limited their ability to:

- Understand demand  
- Optimize scheduling  
- Improve pricing  
- Allocate fleet resources effectively  

This EDA provides the foundation for smarter operational planning.

---

##  **Project Objectives**

- Clean and standardize trip data  
- Explore passenger usage patterns  
- Evaluate transport mode performance  
- Analyze fare, duration, and revenue relationships  
- Identify peak periods and route popularity  
- Provide insights and recommendations for optimization  

---

##  **Dataset Description**

The dataset contains **1,000 rows** and **12 columns** (reduced to 10 after cleaning).

### **Key Fields**

| Column | Description |
|--------|-------------|
| `Trip_ID` | Unique trip identifier |
| `Mode_of_Transport` | Bus, Train, Ferry, Tram |
| `Departure_Station` / `Arrival_Station` | Route endpoints |
| `Departure_Time` | Timestamp of departure |
| `Passenger_Count` | Number of passengers |
| `Fare_Amount` | Fare charged |
| `Trip_Duration_Minutes` | Duration of trip |
| `Trip_Date` | Date of trip |
| `Day_of_Week` | Derived from Trip_Date |

---

##  **Tools & Technologies**

- **Python**
- **Pandas** – data cleaning & manipulation  
- **NumPy** – numerical operations  
- **Matplotlib & Seaborn** – visualizations  
- **Missingno** – missing data diagnostics  
- **Jupyter Notebook** – analysis environment  

---

##  **Data Cleaning & Preparation**

###  Standardization
- Normalized transport mode names  
- Fixed inconsistent station names (whitespace, casing)  
- Converted date/time fields to proper datetime formats  

###  Missing Value Treatment
Median imputation applied to:
- `Passenger_Count`
- `Fare_Amount`
- `Trip_Duration_Minutes`

###  Feature Engineering
New features created:
- `Revenue`
- `Route`
- `Fare_per_Passenger`
- `Hour_of_Day`
- `Is_Weekend`

###  Outlier Detection
- IQR method  
- Visualized using histograms and boxplots  

---

##  **Key Performance Indicators**

| KPI | Value |
|-----|--------|
| **Total Trips** | 1,000 |
| **Total Passengers** | 49,039 |
| **Total Revenue** | \$1,248,668.18 |
| **Average Trip Duration** | 94.59 minutes |

---

##  **Time Series Insights**

### **Daily & Hourly Patterns**
- Strong weekday usage  
- Peak demand on **Thursday**  
- Sharp weekend decline  
- Morning peak: **8–9 AM**  
- Evening peak: **6–9 PM**, strongest around **21:00**  

### **Mode‑Specific Time Patterns**
- **Tram** dominates evening travel  
- **Train** shows classic commuter peaks  
- **Bus** strongest mid‑day  
- **Ferry** steady throughout the day  

---

##  **Univariate Analysis**

### **Numerical Columns**
- Passenger count, fare, and duration show standardized patterns  
- Revenue is right‑skewed  
- No strong relationship between trip duration and revenue  

### **Categorical Columns**
- **Bus** and **Ferry** are most used  
- **Central** is the top departure station  
- **Airport** is the most common arrival station  
- Weekday usage dominates  

---

##  **Bivariate & Multivariate Insights**

### **Transport Mode Performance**
- Trip durations similar across all modes  
- Fares appear standardized (~25 units median)  
- **Bus** generates the highest revenue  
- **Tram** contributes the least  

### **Trip Characteristics**
- Revenue strongly driven by **passenger count**, not duration  
- Fare per passenger remains low and consistent  
- Flat fare structure indicated by horizontal clustering  

### **Route Popularity**
- **South Point → Airport (Ferry)** is the most popular route  
- Most high‑volume routes are bus‑dominated  

### **Correlation Summary**
- Revenue moderately correlates with:
  - Passenger_Count (0.66)
  - Fare_Amount (0.67)
- Trip duration has minimal impact on revenue or demand  

---

##  **Summary of Findings**

### **Demand Patterns**
- Strong weekday usage  
- Thursday is the busiest day  
- Weekend demand drops significantly  
- Clear morning and evening rush hours  

### **Mode Insights**
- **Bus**: highest revenue  
- **Train**: strong commuter profile  
- **Tram**: evening‑focused  
- **Ferry**: stable and consistent  

### **Revenue Trends**
- Weekday revenue dominates  
- Weekend weakness across all modes  
- Revenue aligns with passenger flow  

### **System Reliance**
- Network heavily dependent on **work‑related travel**  
- Pricing appears consistent across time and duration  

---

##  **Recommendations**

### **1. Capacity & Scheduling Optimization**
- Increase capacity during peak weekday hours  
- Reduce services during low‑demand periods  
- Use off‑peak windows for maintenance  

### **2. Revenue Diversification**
- Introduce weekend promotions  
- Partner with tourism and entertainment sectors  

### **3. Mode‑Specific Strategies**
- **Bus & Train**: strengthen weekday operations  
- **Tram**: target evening/leisure riders  
- **Ferry**: market stability to commuters and tourists  

### **4. Pricing & Incentives**
- Implement dynamic/off‑peak pricing  
- Offer loyalty programs and bundled passes  

### **5. Operational Improvements**
- Align fleet allocation with demand patterns  
- Improve turnaround times and reduce delays  

---

## License

This project is licensed under the terms of the MIT License.  
See the [LICENSE](./LICENSE.md) file for full details.



## 📬 **Contact**

For collaboration, feedback, or inquiries, feel free to connect.


