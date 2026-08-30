# Milestone 3: Urban Pulse – Transportation & Mobility Intelligence Dashboard

## Overview

The Transportation & Mobility Intelligence Dashboard is an interactive Power BI dashboard developed as part of the Urban Pulse Smart City Analytics Platform. The dashboard provides a consolidated view of urban transportation activities by integrating traffic, mobility, weather, and incident data into a single analytical interface.

The primary objective of this dashboard is to monitor transportation performance, analyze traffic behavior, evaluate road utilization, understand ride-sharing demand, and assess the impact of weather conditions on urban mobility. The dashboard enables users to explore transportation trends through dynamic visualizations and interactive filters, supporting data-driven decision-making for smart city transportation management.

---

## Dashboard Objectives

- Monitor overall transportation activity across the city.
- Analyze traffic speed and road occupancy levels.
- Track ride-sharing demand patterns over time.
- Evaluate the impact of weather conditions on vehicle movement.
- Monitor accident occurrences and traffic conditions.
- Provide an interactive platform for transportation analytics.

---

## Key Performance Indicators (KPIs)

The dashboard includes the following KPI cards:

| KPI | Value |
|------|------|
| Total Vehicles | 266K |
| Average Traffic Speed | 37.42 km/h |
| Average Road Occupancy | 61.37% |
| Ride-Sharing Demand | 73K |
| Accident Reports | 196 |

These KPIs provide a quick overview of transportation performance and mobility conditions.

---

## Dashboard Components

### Vehicle Volume Over Time
Displays monthly vehicle volume trends to identify traffic fluctuations and transportation demand patterns.

### Traffic Condition Distribution
Shows the distribution of traffic conditions, helping users understand congestion levels within the transportation network.

### Traffic Speed vs Road Occupancy
Analyzes the relationship between road occupancy and vehicle speed to identify traffic bottlenecks and congestion patterns.

### Vehicle Volume by Weather
Compares vehicle traffic under different weather conditions such as Clear, Rain, Fog, and Snow to evaluate environmental impacts on mobility.

### Ride-Sharing Demand by Month
Tracks ride-sharing demand trends over time and helps identify seasonal changes in transportation usage.

### Interactive Filters
The dashboard provides dynamic slicers for:

- Weather Condition
- Traffic Condition
- Date Range

allowing users to perform customized transportation analysis.

---

## Data Model

The dashboard is built using a Star Schema consisting of:

### Fact Table
- Transportation_Data

### Dimension Tables
- Dim_Date
- Dim_Weather
- Dim_Location
- Dim_Incident
- Dim_Mobility

This model enables efficient reporting and analytical calculations.

---

## Technologies Used

- Microsoft Power BI
- Power Query
- DAX (Data Analysis Expressions)
- Star Schema Data Modeling
- Interactive Dashboard Design

---

## Key Insights

- Traffic volume varies across different months, indicating changing transportation demand.
- Road occupancy directly influences traffic speed and congestion levels.
- Weather conditions impact vehicle movement and traffic volume.
- Ride-sharing demand exhibits noticeable monthly trends.
- Traffic conditions and accident occurrences affect transportation efficiency.
- Interactive filtering enables detailed exploration of transportation behavior and mobility performance.

---

## Outcome

The Transportation & Mobility Intelligence Dashboard successfully transforms raw transportation and mobility data into actionable insights. By combining traffic, weather, and ride-sharing information, the dashboard supports smarter transportation planning, improved traffic management, and data-driven urban mobility decision-making.

---
