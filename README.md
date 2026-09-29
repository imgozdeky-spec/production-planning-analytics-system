# Production Planning Analytics System

## 📌 Project Overview

**Production Planning Analytics System** is a data analytics and decision-support project developed to analyze manufacturing operations using **SQL and Python**.

The system combines a relational database with Python-based analytics to examine:

* Customer orders
* Production quantities
* Machine performance
* Production efficiency
* Machine utilization
* Downtime
* Bottlenecks
* Order completion
* Production KPIs

The project demonstrates how **Industrial Engineering, SQL, Python and Data Analytics** can be combined to support production planning and operational decision-making.

---

## 🎯 Project Objectives

The main objectives of this project are:

* Design a relational production database
* Store production and order data using SQL
* Analyze manufacturing data with SQL queries
* Connect a SQL database with Python
* Perform data analysis using Pandas
* Calculate production efficiency
* Analyze machine utilization
* Identify potential production bottlenecks
* Track order completion
* Generate production KPIs
* Create analytical charts and reports

---

## 🏭 System Architecture

The project follows a simple data analytics architecture:

```text
Production Data
      ↓
Relational Database
      ↓
SQL Queries
      ↓
Python + Pandas
      ↓
Production Analysis
      ↓
KPI & Bottleneck Analysis
      ↓
Charts & Reports
```

---

## 🗄️ Database Structure

The project uses a relational database consisting of four main tables.

### Customers

Stores customer information.

Main fields:

* `customer_id`
* `customer_name`
* `industry`

### Machines

Stores production machine information.

Main fields:

* `machine_id`
* `machine_name`
* `machine_type`
* `capacity_per_hour`
* `status`

### Orders

Stores customer orders.

Main fields:

* `order_id`
* `customer_id`
* `product`
* `quantity`
* `order_date`
* `due_date`
* `priority`

### Production Records

Stores production activities.

Main fields:

* `record_id`
* `order_id`
* `machine_id`
* `production_date`
* `planned_quantity`
* `produced_quantity`
* `production_time_hours`
* `downtime_hours`

---

## 🔎 SQL Analysis

The project includes SQL queries for:

### Order and Customer Analysis

Customer orders are analyzed using relational joins between the `orders` and `customers` tables.

### Machine Performance

Production quantities and downtime are grouped by machine.

### Production Efficiency

Production efficiency is calculated as:

```text
Production Efficiency =
Produced Quantity / Planned Quantity × 100
```

### Machine Downtime

Total downtime is calculated for each machine to identify machines requiring further investigation.

### Order Completion

The system calculates:

```text
Remaining Quantity =
Ordered Quantity - Produced Quantity
```

This allows production progress to be monitored for each order.

---

## 🐍 Python Analysis

Python is used to retrieve data from the database and perform additional analytics.

Main Python technologies:

* Pandas
* Matplotlib
* SQLite

Python modules include:

* `database_connection.py`
* `data_analysis.py`
* `order_analysis.py`
* `bottleneck_analysis.py`
* `visualization.py`
* `kpi_report.py`
* `production_dashboard.py`

---

## 📊 KPI Analysis

The system calculates several production KPIs.

### Overall Completion Rate

```text
Overall Completion Rate =
Total Produced Quantity /
Total Ordered Quantity × 100
```

### Machine Utilization

```text
Machine Utilization =
Production Hours /
(Production Hours + Downtime Hours) × 100
```

### Production Efficiency

```text
Production Efficiency =
Produced Quantity /
Planned Quantity × 100
```

These indicators provide a basic overview of production performance.

---

## 🚧 Bottleneck Analysis

A simple analytical bottleneck score is calculated using production efficiency and machine utilization.

```text
Bottleneck Score =
(100 - Efficiency) × 0.5
+
(100 - Utilization) × 0.5
```

Machines with higher scores can be considered potential bottlenecks for further investigation.

> **Note:** The bottleneck score is an analytical indicator created for this portfolio project. It is not intended to represent a validated industrial optimization model.

---

## 📈 Visualization

The project generates production analysis charts including:

* Machine Production Efficiency
* Machine Downtime Analysis

Generated outputs are stored under:

```text
outputs/
└── charts/
```

Reports are stored under:

```text
outputs/
└── reports/
```

---

## 📁 Project Structure

```text
production-planning-analytics-system
│
├── database
│   ├── schema.sql
│   ├── seed_data.sql
│   └── analysis_queries.sql
│
├── data
│
├── notebooks
│
├── outputs
│   ├── charts
│   └── reports
│
├── src
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

## 🛠️ Technologies

* **Python**
* **SQL**
* **SQLite**
* **Pandas**
* **Matplotlib**
* **Relational Database**
* **Data Analytics**

---

## 🏭 Industrial Engineering Perspective

This project focuses on several important Industrial Engineering concepts:

* Production planning
* Capacity analysis
* Machine utilization
* Bottleneck identification
* Production efficiency
* Order tracking
* KPI monitoring
* Data-driven decision support

The project demonstrates how production data can be transformed into analytical information that supports operational decision-making.

---

## 🚀 Future Improvements

Possible future improvements include:

* Automatic production scheduling
* Linear Programming / Mixed Integer Programming
* Job Shop Scheduling
* Due-date optimization
* Genetic Algorithm based scheduling
* Demand forecasting
* Machine learning based delay prediction
* Interactive Streamlit dashboard
* Real-time production monitoring
* ERP system integration
* Multi-objective production optimization
* Integration with predictive maintenance systems

---

## 🎓 Portfolio Purpose

This project was developed as a portfolio project to demonstrate the combination of:

**Industrial Engineering + SQL + Python + Data Analytics + Production Planning**

It is designed to demonstrate practical skills in database design, production analytics, KPI development and data-driven decision support.
