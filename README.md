# Data Warehouse & Analytics Project 🏗️

> A comprehensive data warehousing and analytics solution — from raw ingestion to actionable insights — built with Medallion Architecture on SQL Server.

![SQL Server](https://img.shields.io/badge/SQL%20Server-CC2927?style=flat&logo=microsoft-sql-server&logoColor=white)
![ETL](https://img.shields.io/badge/ETL%20Pipelines-0078D4?style=flat)
![Architecture](https://img.shields.io/badge/Medallion%20Architecture-F0A500?style=flat)
![Status](https://img.shields.io/badge/Status-Portfolio%20Project-brightgreen?style=flat)

---

## Overview

This project demonstrates an end-to-end data warehousing pipeline integrating sales data from two source systems (ERP and CRM). It covers data architecture design, ETL development, dimensional modeling, and SQL-based analytics reporting — all built to reflect industry best practices.

This repository is a practical reference for professionals and students looking to demonstrate expertise in:

`SQL Development` · `Data Architecture` · `Data Engineering` · `ETL Pipelines` · `Data Modeling` · `Analytics`

---

## Architecture — Medallion Layers
```
┌─────────────┐     ┌─────────────┐     ┌─────────────┐
│   🥉 Bronze  │ ──► │   🥈 Silver  │ ──► │   🥇 Gold    │
│   Raw Zone  │     │ Cleansed    │     │  Curated    │
└─────────────┘     └─────────────┘     └─────────────┘
  ERP + CRM CSVs    Quality-resolved    Star schema for
  ingested as-is    unified schema      analytical queries
```

| Layer | Purpose |
|-------|---------|
| **Bronze** | Raw ingestion from ERP and CRM CSV files — no transformations applied |
| **Silver** | Data cleansing, deduplication, schema standardization, and source integration |
| **Gold** | Fact and dimension tables optimized for OLAP queries and reporting |

---

## Project Scope

### Objective
Build a modern data warehouse on **SQL Server** that consolidates sales data from heterogeneous sources, enabling reliable analytical reporting and informed decision-making.

### Specifications

| Requirement | Detail |
|---|---|
| **Data sources** | Two systems — ERP and CRM — provided as CSV files |
| **Data quality** | Cleansing and issue resolution in the Silver layer before analysis |
| **Integration** | Both sources merged into a single user-friendly analytical model |
| **Historization** | Latest snapshot only — no SCD or temporal tracking required |
| **Documentation** | Full data model docs for business stakeholders and analytics teams |

---

## What's Included

### 🔷 Data Architecture
Modern warehouse design applying Medallion Architecture (Bronze → Silver → Gold) to structure data flow from raw ingestion to curated analytics.

### 🔄 ETL Pipelines
Extraction, transformation, and load workflows connecting ERP and CRM source systems to the warehouse layers, with data quality checks at each stage.

### 📐 Data Modeling
Star-schema dimensional model with fact and dimension tables designed for performant analytical queries across the integrated dataset.

### 📊 Analytics & Reporting
SQL-based reports and dashboard-ready views delivering business insights from the Gold layer.

---

## Repository Structure
```
📦 data-warehouse-project
├── 📁 datasets/          # Source CSV files (ERP & CRM)
├── 📁 docs/              # Data model documentation & diagrams
├── 📁 scripts/
│   ├── bronze/           # Raw ingestion scripts
│   ├── silver/           # Cleansing & transformation scripts
│   └── gold/             # Dimensional model scripts
├── 📁 reports/           # SQL analytics queries & views
└── README.md
```

---

## Getting Started

1. **Clone the repository**
```bash
   git clone https://github.com/your-username/data-warehouse-project.git
```
2. **Set up SQL Server** and create a new database instance.
3. **Run scripts in order**: `bronze/` → `silver/` → `gold/`
4. **Explore reports** in the `/reports` folder for ready-made analytical queries.

---

## License
This project is open-source and available under the [MIT License](LICENSE).
