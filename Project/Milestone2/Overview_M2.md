# Milestone 2 – Data Modeling & DAX

## Overview

**Milestone 2** focuses on structuring the **Urban Pulse – Smart Mobility** datasets in Power BI and preparing them for scalable mobility analysis.

The milestone involves transforming raw data, designing **Fact and Dimension tables**, creating a dedicated **Date dimension**, establishing relationships using a **Star Schema**, and implementing **DAX measures and calculated columns** for analysis.

## Data Modeling

The Urban Pulse data ecosystem is organized according to analytical roles rather than merging all datasets into a single flat table.

### Fact Tables

* **Fact_Mobility** – Contains event-level mobility metrics such as vehicle count, traffic speed, road occupancy, ride-sharing demand, emissions, energy, parking, and accidents.
* **Fact_Trips** – Contains trip-level information such as start/end dates, category, purpose, and miles.

### Dimension Tables

* **Dim_Date** – Date, Year, Month, Quarter, and Day
* **Dim_City** – City, Country, Region, and geographic details
* **Dim_WeatherStation** – Weather station and location information
* **Dim_Happiness** – Happiness and socio-economic indicators

## Star Schema

The datasets are organized into a **Star Schema**, where fact tables store measurable event-level data and dimension tables provide additional context.

Key relationships include:

* `Dim_Date (1) → Fact_Mobility (N)`
* `Dim_Date (1) → Fact_Trips (N)`

The model uses **one-to-many cardinality** with **single cross-filter direction**.

## Date Dimension

A dedicated **Dim_Date** table was created with:

* Date
* Year
* Month
* Quarter
* Day

It enables time-based filtering and trend analysis across the mobility datasets.

## DAX Implementation

DAX was used to create important measures and calculated columns.

### Key Measures

**Total Vehicles**

```DAX
Total Vehicles =
SUM(Fact_Mobility[Vehicle_Count])
```

**Average Traffic Speed**

```DAX
Average Traffic Speed =
AVERAGE(Fact_Mobility[Traffic_Speed_kmh])
```

**Total Trips**

```DAX
Total Trips =
COUNTROWS(Fact_Trips)
```

### Calculated Column

A **Traffic Speed Category** was created using `SWITCH(TRUE())` to classify traffic speed as:

* Low – below 20 km/h
* Moderate – below 40 km/h
* High – 40 km/h and above

Measures respond to filter context, while calculated columns provide row-level categorization.

## Mobility Dashboard

The structured model and DAX calculations were used to create an interactive Power BI dashboard containing:

### KPI Cards

* Total Vehicles
* Average Speed
* Road Occupancy
* Ride-Sharing Demand

### Charts

* Volume Over Time
* Volume by Speed
* Trips by Purpose

### Filters

* Year
* Weather
* Traffic Condition

## Milestone 2 Outcome

By completing Milestone 2, the Urban Pulse project has:

* Built a structured **Fact/Dimension data model**
* Created a dedicated **Date dimension**
* Established valid table relationships
* Implemented DAX-driven KPIs
* Developed an interactive mobility dashboard
* Prepared the model for further mobility analysis

### Future Scope

The next stages include:

* Time-intelligence analysis
* Map-based traffic visualization
* Traffic-flow prediction
* Accident-risk analysis
