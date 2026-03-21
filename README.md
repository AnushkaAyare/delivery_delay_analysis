# Delivery Delay Analysis & Optimization using SQL

## Project Overview
This project explores a food delivery dataset to understand what actually drives delivery delays in real-world conditions.
The goal was not just analysis, but identifying patterns that can help improve delivery efficiency using data.

---

## Objective
The objective of this analysis was to identify the main reasons behind delivery delays and understand how different operational and environmental factors impact delivery time.
---

## Data Cleaning
- Removed duplicate records using `GROUP BY` validation
- Standardized categorical values using `TRIM()`
- Handled missing values by replacing NULLs with `'Unknown'`
- Converted courier experience into numeric format for analysis
---

## Exploratory Data Analysis (EDA)

### Key Factors Analyzed:
- Distance
- Preparation Time
- Traffic Level
- Weather Conditions
- Courier Experience
- Vehicle Type
- Time of Day
---

## Key Insights

- Distance turned out to be the most consistent and strongest driver of delivery time, showing a clear and expected relationship.
- Traffic has a strong and consistent impact on delivery time across all distance ranges, often causing major delays even for short trips.
- Weather and Preparation Time have moderate impact  
- Courier Experience , Vehicle Type , and Time of Day have minimal influence  

---

## Advanced Analysis

What stood out during deeper analysis:
- Traffic impact becomes much more severe when combined with longer distances  
- The worst delays happen when high traffic overlaps with poor weather conditions  
- Even short trips are heavily delayed during peak traffic situations

### Performance Metrics
- Late delivery percentage calculated using threshold-based classification  
- Delivery categorized into:
  - On Time
  - Slight Delay
  - High Delay  
- Efficiency evaluated using time per kilometer

One interesting observation was that external factors like traffic had a much stronger impact on delivery time than courier experience, which was less significant than expected.
---

## Key Findings

- Delivery performance is primarily driven by **external factors** (traffic, distance, weather)
- Internal factors like courier experience have limited impact
- Worst-case scenarios occur when:
  - Distance is high  
  - Traffic is heavy  
  - Weather conditions are poor  

---

## Proposed Solutions

### 1. Dynamic Order Batching
Group nearby orders during high-traffic periods to reduce trips and improve efficiency.

### 2. Traffic-Aware ETA & Pricing
Adjust delivery time estimates dynamically based on traffic conditions to improve customer experience.

### 3. Smart Courier Allocation
Assign deliveries based on route complexity (distance + traffic) rather than random assignment.

### 4. Micro-Zone Optimization
Divide delivery areas into smaller zones based on delay patterns to reduce variability.

---

## Tools & Technologies
- SQL (SQLite)

---

## Conclusion
Overall, the results clearly show that delivery delays are driven more by external conditions like traffic and distance rather than individual courier performance.
This highlights the importance of smarter logistics planning over focusing only on courier efficiency.
