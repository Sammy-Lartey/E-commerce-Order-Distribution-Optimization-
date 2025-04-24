# Affinity Labs E-commerce Order Distribution Optimization

## Overview

This project analyzes and optimizes the order distribution strategy for Affinity Labs, an e-commerce company operating out of Lomé, Togo and serving customers in Ghana. The goal is to diagnose current operational inefficiencies, simulate truck allocation strategies, and recommend scalable improvements to improve delivery performance.

The analysis covers an 8-month period from July 2024 to March 2025 and includes raw operational data from orders, delivery centers, and truck fleets.

---

## Key Findings

### Order Fulfillment Breakdown
- 59% of all orders (310,775 out of 526,945) remained pending.  
- Only 35.5% were completed, and 5.5% were in transit.  
- The bottleneck suggests inefficiencies in dispatch, truck availability, or routing workflows.

### March 2025 Anomaly
- Over 341,000 orders were logged in March—14x higher than the monthly average.  
- Revenue spiked to GHS 1.54 billion, up from GHS 134 million/month average.  
- This raises concerns of either a legitimate operational spike or data inflation.

### Client Distribution & Data Gaps
- A handful of clients dominated order volume.  
- The top "client" had no identifiable ID—flagging poor data integrity.  
- Clean client data is essential for forecasting and performance monitoring.

---

## Optimization Strategy

An algorithm was developed to simulate truck assignments and assess whether the existing fleet could realistically fulfill the outstanding backlog. This involved:

- Calculating volume compatibility between pending orders and available trucks.  
- Prioritizing assignments by delivery center and order volume.  
- Enforcing truck capacity limits during allocation.

The results are saved in the [`outputs/`](outputs/) folder as:
- `optimized_assignments.csv`  
- `remaining_backlog.csv`

---

## Actionable Long-Term Solutions

These strategies aim to sustainably expand capacity, improve operational efficiency, and prevent future backlog issues:

### 1. Expand Fleet Capacity Strategically
- Add more box trucks, which match the average order volume.  
- Use short-term leasing during high-demand months (e.g. March) to avoid permanent overhead.

### 2. Align Fleet Deployment with Regional Demand
- Allocate trucks based on real-time demand in high-volume hubs like Accra and Tema.  
- Monitor backlog and fulfillment KPIs per region to support dynamic reallocation.  
- Avoid inter-regional shifting of orders unless capacity or service-level metrics support it.

### 3. Strengthen Data Integrity and Planning Accuracy
- Apply validation checks (e.g. capacity thresholds) during truck assignment to prevent overloading.  
- Standardize truck capacity definitions across platforms for consistent planning and analytics.

---

## Tools Used

- **Python** with **Jupyter Notebook** for data processing and simulation.  
- **SQL** with **Metabase** for Part 1 dashboarding and business analysis.

---

## Author

Samuel Lartey  
Data Analyst
April 2025
