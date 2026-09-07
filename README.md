# Data Warehouse & Analytics Portfolio Project

An end-to-end modern Data Warehouse and Business Intelligence solution designed to consolidate disparate source systems (ERP & CRM), perform robust data cleaning and transformations, and model analytical datasets into a Star Schema to deliver actionable business insights.

---

## 🏗️ Architecture Overview

This project implements the **Medallion Architecture** pattern using Microsoft SQL Server across three distinct layers:

* **Bronze Layer:** Stores raw data as-is from source systems. Ingests raw CSV files (ERP & CRM) directly into staging database tables.
* **Silver Layer:** Cleanses, standardizes, and normalizes the data. Resolves data quality issues, handles missing values, and prepares structured tables.
* **Gold Layer:** Business-ready data modeled into an optimized **Star Schema** (Fact and Dimension tables) ready for reporting, analytical queries, and BI tools.

**Pipeline Flow:**  
`Source CSVs (ERP & CRM)` ➔ `Bronze Layer (Raw)` ➔ `Silver Layer (Cleansed)` ➔ `Gold Layer (Star Schema)` ➔ `BI & SQL Analytics`

---

## 🛠️ Tech Stack & Skills

* **Database Engine:** Microsoft SQL Server
* **Development GUI:** SQL Server Management Studio (SSMS)
* **Architecture & ERD Design:** Draw.io
* **Version Control:** Git & GitHub
* **Core Competencies:**
  * ETL / ELT Pipeline Architecture
  * Data Cleansing, Normalization & Transformation
  * Dimensional Modeling (Star Schema: Fact & Dimension tables)
  * Advanced SQL (Stored Procedures, CTEs, Window Functions, Views)
  * Exploratory Data Analysis & Business Performance Reporting

---

## 🚀 Project Requirements & Specifications

### 1. Building the Data Warehouse (Data Engineering)
* **Data Sources:** Consolidate data from two independent internal systems (ERP for transactions, CRM for customer profiles).
* **Data Quality:** Cleanse, standardize inconsistent data types, and eliminate invalid records prior to modeling.
* **Data Integration:** Unify datasets into a single cohesive data model using surrogate keys.
* **Scope:** Optimized for current analytical datasets.

### 2. Analytics & Reporting (Data Analysis)
Develop SQL-based analytical queries to deliver actionable insights into:
* **Customer Behavior:** Lifetime value, retention metrics, and geographical purchasing patterns.
* **Product Performance:** Top-performing products, sales velocity, and category revenue drivers.
* **Sales Trends:** Growth rates, seasonality analysis, and average order value (AOV).

---

## 📂 Repository Structure

```text
data-warehouse-project/
│
├── datasets/                           # Raw datasets (ERP and CRM data)
│
├── docs/                               # Project documentation & architecture
│   ├── etl.drawio                      # ETL processes and methods diagram
│   ├── data_architecture.drawio        # High-level architecture design
│   ├── data_catalog.md                 # Metadata and column descriptions
│   ├── data_flow.drawio                # End-to-end data flow pipeline
│   ├── data_models.drawio              # Dimensional model (Star Schema)
│   └── naming-conventions.md           # Guidelines for tables and scripts
│
├── scripts/                            # Pipeline transformation scripts
│   ├── bronze/                         # DDL & procedures for raw data ingestion
│   ├── silver/                         # Cleaning and transformation logic
│   └── gold/                           # Dimensional modeling views & fact tables
│
├── tests/                              # Data validation & quality checks
│
├── README.md                           # Project documentation
├── LICENSE                             # Project license
├── .gitignore                          # Files ignored by Git
└── requirements.txt                    # Project dependencies
```

---

## ⚙️ Setup & Execution Guide

### 1. Clone the Repository

```bash
git clone https://github.com/Ahmedbadour14/data-warehouse-project.git
cd data-warehouse-project
```

### 2. Initialize Database

Open SSMS and run:

```sql
CREATE DATABASE DataWarehouse;
GO
USE DataWarehouse;
GO
```

### 3. Execute Pipeline Scripts

Run the SQL scripts sequentially:
* `scripts/bronze/` to create staging tables and bulk-load the raw CSV data.
* `scripts/silver/` to execute cleansing, standardization, and loading procedures.
* `scripts/gold/` to create the dimension tables, fact tables, and analytical views.

### 4. Run Analytics & Validation

* Execute scripts in `tests/` to ensure data integrity and validation checks pass.
* Run queries in `scripts/gold/` to produce core business performance insights.

---

## 👤 Author

**Ahmed Badour**
* **GitHub:** [Ahmedbadour14](https://github.com/Ahmedbadour14)
* **LinkedIn:** [Ahmed Badour](https://www.linkedin.com/in/ahmed-badour-)

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
