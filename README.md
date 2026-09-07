Data Warehouse & Analytics Portfolio Project
An end-to-end modern Data Warehouse and Business Intelligence solution designed to consolidate disparate source systems (ERP & CRM), perform robust data cleaning and transformations, and model analytical datasets into a Star Schema to deliver actionable business insights.

🏗️ Architecture Overview
This project implements the Medallion Architecture pattern using SQL Server to structure data processing across three distinct stages:

[ ERP / CRM CSV Sources ]
           │
           ▼
┌───────────────────────┐
│     Bronze Layer      │  --> Raw data ingestion (as-is staging tables)
└───────────────────────┘
           │
           ▼
┌───────────────────────┐
│     Silver Layer      │  --> Cleansing, standardization, missing value handling & deduplication
└───────────────────────┘
           │
           ▼
┌───────────────────────┐
│      Gold Layer       │  --> Star Schema data modeling (Fact & Dimension views for analytics)
└───────────────────────┘
           │
           ▼
[ BI & SQL Analytics Reports ]
Bronze Layer: Ingests raw data directly from ERP and CRM CSV files into SQL Server without structural modifications.

Silver Layer: Cleanses, standardizes data types, handles invalid entries, and normalizes key columns to prepare clean tables.

Gold Layer: Models data into a consumption-ready Star Schema with dimension and fact structures optimized for analytical queries.

🛠️ Tech Stack & Skills
Database Engine: Microsoft SQL Server

Development Environment: SQL Server Management Studio (SSMS)

Design & Diagramming: Draw.io (Data Flow, Architecture, and Star Schema ERD)

Version Control: Git & GitHub

Core Competencies:

ETL / ELT Pipeline Design

Data Cleansing & Transformation

Dimensional Modeling (Star Schema: Fact & Dimension tables)

Advanced SQL (Window Functions, CTEs, Aggregations, Stored Procedures, Views)

Business Performance & Exploratory Data Analysis (EDA)

🚀 Project Specifications
1. Data Engineering (Warehouse Implementation)
Source Systems: Two internal systems representing ERP (sales transactions, order details) and CRM (customer profiles, regional data).

Data Cleansing: Handling null values, correcting inconsistent categorical naming, standardizing date formats, and filtering invalid customer records.

Data Integration: Unifying customer and product data across systems with surrogate keys and unified dimension structures.

Scope: Current-state analytical snapshot optimization.

2. Business Intelligence & Analytics
Analytical queries in the Gold Layer address key commercial questions:

Customer Analysis: Identifying high-value customer segments, repeat purchase rates, and geographical distribution.

Product Performance: Tracking top-selling products, category contribution margins, and low-velocity inventory.

Sales Trends: Calculating monthly revenue growth, seasonality patterns, and average order values (AOV).

📂 Repository Structure
Plaintext
data-warehouse-project/
│
├── datasets/                           # Source datasets (ERP and CRM CSV files)
│   ├── erp/
│   └── crm/
│
├── docs/                               # Architecture diagrams and specifications
│   ├── data_architecture.drawio        # End-to-end data pipeline diagram
│   ├── data_models.drawio              # Star Schema entity relationship diagram (ERD)
│   ├── data_flow.drawio                # ETL data flow breakdown
│   ├── data_catalog.md                 # Column descriptions, schemas, and metadata
│   └── naming-conventions.md           # Database and script naming standards
│
├── scripts/                            # SQL pipeline scripts
│   ├── bronze/                         # DDL & Bulk Ingestion scripts
│   │   ├── ddl_bronze.sql
│   │   └── proc_load_bronze.sql
│   ├── silver/                         # Cleaning & Transformation procedures
│   │   ├── ddl_silver.sql
│   │   └── proc_load_silver.sql
│   └── gold/                           # Dimensional Modeling (Views & Facts)
│       ├── ddl_gold.sql
│       └── analytical_queries.sql
│
├── tests/                              # Data quality and validation tests
│   └── data_quality_checks.sql
│
├── .gitignore
├── LICENSE
└── README.md
⚙️ Setup & Execution Guide
Prerequisites
Microsoft SQL Server (Developer or Express Edition)

SQL Server Management Studio (SSMS)

Git installed locally

Step-by-Step Installation
Clone the Repository

Bash
git clone https://github.com/your-username/data-warehouse-project.git
cd data-warehouse-project
Initialize Database

Open SSMS and create a new database:

SQL
CREATE DATABASE DataWarehouse;
GO
USE DataWarehouse;
GO
Deploy Schemas & Pipelines

Execute scripts sequentially:

scripts/bronze/ddl_bronze.sql then scripts/bronze/proc_load_bronze.sql

scripts/silver/ddl_silver.sql then scripts/silver/proc_load_silver.sql

scripts/gold/ddl_gold.sql

Verify Pipeline & Run Analytics

Run validation tests in tests/data_quality_checks.sql.

Execute analytical queries located in scripts/gold/analytical_queries.sql to generate business insights.

👤 Author
Ahmed Badour

GitHub: https://github.com/Ahmedbadour14

LinkedIn: www.linkedin.com/in/ahmed-badour-

Portfolio / Contact: ahmed.badour2005@gmail.com

📄 License
This project is licensed under the MIT License - see the LICENSE file for details.
