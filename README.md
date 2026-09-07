# Data Warehouse & Analytics Portfolio Project

An end-to-end Data Warehouse and Business Intelligence solution designed to consolidate disparate source systems (ERP & CRM), perform data transformations, and model analytical datasets into a Star Schema.

---

## 🏗️ Architecture Overview

This project implements the **Medallion Architecture** pattern using SQL Server:

* **Bronze Layer:** Ingests raw data directly from ERP and CRM CSV files into staging tables without modifications.
* **Silver Layer:** Cleanses data, standardizes data types, handles invalid entries, and normalizes key columns.
* **Gold Layer:** Models business-ready data into a **Star Schema** (Fact & Dimension tables) optimized for analytics.

**Pipeline Flow:**
`Raw CSV Files` ➔ `Bronze (Raw Staging)` ➔ `Silver (Cleansed)` ➔ `Gold (Star Schema)` ➔ `Power BI / SQL Analytics`

---

## 🛠️ Tech Stack & Skills

* **Database Engine:** Microsoft SQL Server
* **Development Environment:** SQL Server Management Studio (SSMS)
* **Modeling & Design:** Draw.io (ERD & Architecture Diagrams)
* **Version Control:** Git & GitHub
* **Core Skills:** ETL Pipelines, Data Modeling, Star Schema, SQL Transformations, Analytical Reporting

---

## 🚀 Project Specifications

### 1. Data Engineering
* **Source Systems:** Integration of ERP (orders and transactions) and CRM (customer profiles).
* **Data Cleansing:** Handling nulls, standardizing date formats, removing duplicates, and key mapping.
* **Data Integration:** Unified dimensions with surrogate keys to connect disparate datasets.

### 2. Analytics & Reporting
* **Customer Insights:** Top-tier customer identification, regional sales, and retention rates.
* **Product Performance:** Revenue drivers, volume by category, and margin analysis.
* **Sales Trends:** Monthly revenue trajectory and average order value (AOV).

---

## 📂 Repository Structure

```text
data-warehouse-project/
├── datasets/                           # Source ERP and CRM CSV files
├── docs/                               # Diagrams and data catalogs
│   ├── data_architecture.drawio
│   ├── data_models.drawio
│   └── data_catalog.md
├── scripts/                            # SQL pipeline scripts
│   ├── bronze/                         # Ingestion & staging scripts
│   ├── silver/                         # Cleaning & transformation procedures
│   └── gold/                           # Star Schema views and fact tables
├── tests/                              # Data quality assurance tests
├── .gitignore
├── LICENSE
└── README.md
```
## ⚙️ Setup & Execution Guide

### 1. Clone the Repository
```bash
git clone [https://github.com/your-username/data-warehouse-project.git](https://github.com/your-username/data-warehouse-project.git)
cd data-warehouse-project
```
2. Initialize Database
Open SSMS and run:

SQL
CREATE DATABASE DataWarehouse;
GO
USE DataWarehouse;
GO
3. Execute Pipeline Scripts
Run the scripts sequentially:

scripts/bronze/ to create staging tables and load raw files.

scripts/silver/ to execute transformation and validation procedures.

scripts/gold/ to build analytical views and star schemas.

4. Run Analytics
Execute analytical queries in scripts/gold/ to view business metrics.

👤 Author
Ahmed Badour

GitHub: https://github.com/Ahmedbadour14

LinkedIn: www.linkedin.com/in/ahmed-badour-

📄 License
This project is licensed under the MIT License - see the LICENSE file for details.
