# Production Planning Analytics System

A SQL and Python-based production analytics and decision-support system designed to analyze manufacturing performance, order completion, machine utilization, downtime, and potential production bottlenecks.

The project demonstrates how **SQL databases and Python analytics** can be integrated into an industrial engineering-oriented production planning workflow.

---

## Project Overview

Production environments generate large amounts of operational data related to:

* Customer orders
* Production quantities
* Machine capacity
* Production time
* Machine downtime
* Order priorities

This project stores these data in a relational SQL database and uses Python to transform them into operational KPIs and analytical insights.

The main objective is to create a simple data-driven production planning support system.

---

## Project Architecture

```text
                 SQL DATABASE
                      │
       ┌──────────────┼──────────────┐
       │              │              │
   Customers       Orders        Machines
                      │              │
                      └──────┬───────┘
                             │
                    Production Records
                             │
                             ▼
                         Python
                             │
             ┌───────────────┼───────────────┐
             │               │               │
       Order Analysis   Machine Analysis   KPI Analysis
             │               │               │
             └───────────────┼───────────────┘
                             ▼
                  Visualization & Reports
```

---

## Main Objectives

* Build a relational production database
* Store manufacturing data using SQL
* Query operational data using SQL
* Connect Python to the SQL database
* Analyze production performance with Pandas
* Calculate production efficiency
* Analyze machine utilization
* Identify potential bottlenecks
* Monitor order completion
* Generate production KPIs
* Create analytical charts and reports

---

## Database Structure

The database contains four main tables.

### Customers

Stores customer information.

| Column        | Description                |
| ------------- | -------------------------- |
| customer_id   | Unique customer identifier |
| customer_name | Customer name              |
| industry      | Customer industry          |

### Machines

Stores production machine information.

| Column            | Description               |
| ----------------- | ------------------------- |
| machine_id        | Unique machine identifier |
| machine_name      | Machine name              |
| machine_type      | Machine category          |
| capacity_per_hour | Production capacity       |
| status            | Current machine status    |

### Orders

Stores customer orders.

| Column      | Description             |
| ----------- | ----------------------- |
| order_id    | Unique order identifier |
| customer_id | Related customer        |
| product     | Product name            |
| quantity    | Ordered quantity        |
| order_date  | Order date              |
| due_date    | Required delivery date  |
| priority    | Order priority          |

### Production Records

Stores production activity.

| Column                | Description                  |
| --------------------- | ---------------------------- |
| record_id             | Production record identifier |
| order_id              | Related order                |
| machine_id            | Machine used                 |
| production_date       | Production date              |
| planned_quantity      | Planned production           |
| produced_quantity     | Actual production            |
| production_time_hours | Production duration          |
| downtime_hours        | Machine downtime             |

---

## SQL Analysis

The project uses SQL queries to perform operational analysis.

Examples include:

### Production Performance

```text
Planned Quantity
        ↓
Produced Quantity
        ↓
Production Efficiency
```

### Machine Downtime

```text
Machine
   ↓
Total Downtime
   ↓
Potential Operational Problem
```

### Order Status

```text
Ordered Quantity
       ↓
Produced Quantity
       ↓
Remaining Quantity
       ↓
Completion Rate
```

---

## Python Analysis

Python is used to retrieve data from the SQL database and perform analytical calculations.

Main Python libraries:

* Pandas
* Matplotlib
* SQLite

The Python layer performs:

* Data extraction
* Data transformation
* KPI calculation
* Machine performance analysis
* Order analysis
* Bottleneck analysis
* Visualization
* Report generation

---

## Key Performance Indicators

The system calculates several production KPIs.

### Production Efficiency

```text
Production Efficiency =
Produced Quantity / Planned Quantity × 100
```

### Machine Utilization

```text
Machine Utilization =
Production Time /
(Production Time + Downtime) × 100
```

### Order Completion Rate

```text
Completion Rate =
Produced Quantity / Ordered Quantity × 100
```

### Bottleneck Score

The project combines production efficiency and machine utilization to create an analytical bottleneck score.

A higher score indicates a machine that may require further investigation.

---

## Bottleneck Analysis

The system analyzes machine-level performance using:

* Production efficiency
* Machine utilization
* Downtime

This can help identify machines that may become constraints in the production process.

Example analytical flow:

```text
Low Efficiency
      +
Low Utilization
      +
High Downtime
      ↓
Higher Bottleneck Score
      ↓
Further Investigation
```

The bottleneck score is an analytical indicator and does not represent a validated industrial optimization model.

---

## Visualization

Python generates production analysis charts.

The current visualization module produces:

```text
outputs/
└── charts/
    ├── machine_efficiency.png
    └── machine_downtime.png
```

These visualizations provide a quick overview of machine-level performance.

---

## KPI Report

The KPI module generates a CSV report containing:

* Total orders
* Total ordered quantity
* Total produced quantity
* Total downtime
* Total production time
* Overall completion rate
* Machine utilization

Generated report:

```text
outputs/
└── reports/
    └── production_kpi_report.csv
```

---

## Project Structure

```text
production-planning-analytics-system/
│
├── database/
│   ├── schema.sql
│   ├── seed_data.sql
│   └── analysis_queries.sql
│
├── data/
│
├── notebooks/
│
├── outputs/
│   ├── charts/
│   └── reports/
│
├── src/
│   ├── database_connection.py
│   ├── data_analysis.py
│   ├── order_analysis.py
│   ├── bottleneck_analysis.py
│   ├── visualization.py
│   ├── kpi_report.py
│   └── production_dashboard.py
│
├── requirements.txt
└── README.md
```

---

## Technologies

* Python
* SQL
* SQLite
* Pandas
* Matplotlib
* Relational Database Design
* Data Analysis
* Production Planning
* KPI Analysis

---

## Industrial Engineering Perspective

This project combines several industrial engineering concepts:

* Production planning
* Manufacturing performance analysis
* Capacity utilization
* Bottleneck analysis
* Production efficiency
* Order management
* Downtime analysis
* KPI-based decision support

The project demonstrates how operational data can be transformed into information that can support production planning decisions.

---

## Example Decision Flow

```text
Customer Orders
      ↓
Production Planning
      ↓
Machine Assignment
      ↓
Production Records
      ↓
SQL Analysis
      ↓
Python Analytics
      ↓
KPI Calculation
      ↓
Bottleneck Identification
      ↓
Production Planning Insight
```

---

## Future Improvements

Possible future developments include:

* Automatic production scheduling
* Optimization algorithms
* Linear programming
* Mixed-integer programming
* Machine capacity constraints
* Due-date optimization
* Job-shop scheduling
* Genetic algorithms
* Demand forecasting
* Machine learning-based delay prediction
* Interactive Streamlit dashboard
* Real-time production monitoring
* ERP system integration
* Multi-objective production optimization

---

## Purpose

This project was developed as a portfolio project to demonstrate the integration of:

**Industrial Engineering + SQL + Python + Data Analytics + Production Planning**

The project focuses on transforming structured production data into analytical insights and decision-support outputs.
