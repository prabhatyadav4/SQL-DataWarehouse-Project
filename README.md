# 🚀 SQL Data Warehouse Project

> A comprehensive data warehouse implementation using **Medallion Architecture** to transform raw ERP & CRM data into analytics-ready business intelligence.


---

## 📋 Table of Contents

- [Overview](#-overview)
- [Architecture](#️-architecture)
- [Features](#-features)
- [Project Structure](#-project-structure)
- [Getting Started](#-getting-started)
- [Data Pipeline](#-data-pipeline)
- [Tech Stack](#️-tech-stack)
- [Learning Outcomes](#-learning-outcomes)
- [Acknowledgments](#-acknowledgments)
- [Contact](#-contact)

---

## 🎯 Overview

This project demonstrates professional data engineering practices by building an end-to-end SQL-based data warehouse. It implements the **Medallion Architecture** (Bronze → Silver → Gold) to process and transform operational data into actionable business insights.

### Key Highlights

- **Medallion Architecture** with three-tier data pipeline
- **Star Schema modeling** for optimal analytical performance
- **Comprehensive ETL pipelines** with data quality checks
- **Real-world integration** of ERP and CRM systems
- **Production-ready SQL patterns** and best practices

---

## 🏗️ Architecture

<img width="1162" height="662" alt="data_architechture" src="https://github.com/user-attachments/assets/4bf523b9-2c8d-4b05-9d82-bbd822e6de57" />

The project follows the Medallion Architecture pattern, ensuring data quality, scalability, and maintainability across three distinct layers:

### 🥉 Bronze Layer — Raw Data Zone

**Purpose:** Immutable landing zone for source data

- Ingests raw data from ERP and CRM sources (CSV format)
- Preserves original data exactly as received
- Serves as the single source of truth for data lineage and auditing
- No transformations or cleansing applied

### 🥈 Silver Layer — Cleansed & Enriched Zone

**Purpose:** Standardized and validated data layer

- Data type corrections and normalization
- Handling of NULL values, duplicates, and data anomalies
- Relationship establishment between different source systems
- Business rule validation and data enrichment

### 🥇 Gold Layer — Analytics-Ready Zone

**Purpose:** Business-optimized data marts

- Fully dimensional Star Schema implementation
- Pre-aggregated fact tables with business metrics
- Conformed dimension tables for consistent reporting
- Optimized for BI tools and analytical queries

---

## ✨ Features

- ✅ **Complete ETL Pipeline** — End-to-end data transformation workflow
- ✅ **Data Quality Framework** — Automated validation and quality checks
- ✅ **Star Schema Design** — Optimized dimensional modeling
- ✅ **Stored Procedures** — Reusable and parameterized data loading
- ✅ **Data Lineage** — Track data flow from source to analytics
- ✅ **Integration Testing** — Comprehensive test suite for data validation

---

## 📂 Project Structure

```
sql-datawarehouse-project/
│
├── datasets/                      # Source data files
│   ├── source_crm/               # CRM system data
│   │   ├── cust_info.csv
│   │   ├── prd_info.csv
│   │   └── sales_details.csv
│   └── source_erp/               # ERP system data
│       ├── CUST_AZ12.csv
│       ├── LOC_A101.csv
│       └── PX_CAT_G1V2.csv
│
├── scripts/                       # SQL scripts
│   ├── init_database.sql         # Database initialization
│   ├── bronze/                   # Bronze layer scripts
│   │   ├── ddl_bronze.sql
│   │   └── proc_load_bronze.sql
│   ├── silver/                   # Silver layer scripts
│   │   ├── ddl_silver.sql
│   │   └── proc_load_silver.sql
│   └── gold/                     # Gold layer scripts
│       └── ddl_gold.sql
│
├── tests/                         # Quality assurance
│   ├── quality_checks_silver.sql
│   └── quality_checks_gold.sql
│
├── docs/                          # Documentation & diagrams
│   ├── data_catalog.md
│   ├── naming_conventions.md
│   └── [architecture diagrams]
│
└── README.md                      # This file
```

---

## 🚀 Getting Started

### Prerequisites

- **SQL Server Express** (2019 or later recommended)
- **SQL Server Management Studio (SSMS)**
- **Git** for version control
- Basic understanding of SQL and data warehousing concepts

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/prabhatyadav4/SQL-DataWarehouse-Project.git
   cd SQL-DataWarehouse-Project
   ```

2. **Initialize the database**
   ```sql
   -- Run in SSMS
   -- Open and execute: scripts/init_database.sql
   ```

3. **Load Bronze Layer**
   ```sql
   -- Execute Bronze DDL and load procedures
   -- scripts/bronze/ddl_bronze.sql
   -- scripts/bronze/proc_load_bronze.sql
   ```

4. **Process Silver Layer**
   ```sql
   -- Transform and cleanse data
   -- scripts/silver/ddl_silver.sql
   -- scripts/silver/proc_load_silver.sql
   ```

5. **Build Gold Layer**
   ```sql
   -- Create Star Schema
   -- scripts/gold/ddl_gold.sql
   ```

6. **Run Quality Checks**
   ```sql
   -- Validate data integrity
   -- tests/quality_checks_silver.sql
   -- tests/quality_checks_gold.sql
   ```

---

## 🔄 Data Pipeline

### Pipeline Flow

```
ERP/CRM Sources → Bronze (Raw) → Silver (Cleansed) → Gold (Analytics)
                     ↓               ↓                    ↓
                  Ingestion     Transformation        Star Schema
```

### ETL Process

1. **Extract**: Load raw data from CSV files into Bronze tables
2. **Transform**: Apply business rules and data quality checks in Silver
3. **Load**: Create dimensional model and populate Gold layer
4. **Validate**: Execute automated quality checks across all layers

---

## 🛠️ Tech Stack

| Category | Technology |
|----------|-----------|
| **Database** | SQL Server Express |
| **Development** | SQL Server Management Studio (SSMS) |
| **Version Control** | Git & GitHub |
| **Documentation** | Markdown, Notion |
| **Diagramming** | Eraser.io |

---

## 🧠 Learning Outcomes

Through this project, you'll gain hands-on experience with:

- ✅ End-to-end data warehouse implementation
- ✅ Medallion Architecture design pattern
- ✅ ETL pipeline development and orchestration
- ✅ Star Schema and dimensional modeling
- ✅ Data quality and validation frameworks
- ✅ SQL performance optimization techniques
- ✅ Business intelligence data preparation

---

## 🙏 Acknowledgments

This project was developed as part of learning from **[Data With Baraa](https://www.youtube.com/@DataWithBaraa)** — an excellent resource for practical data engineering education.

Special thanks to **Baraa Khatib Salkini** for providing clear, real-world guidance on data warehouse implementation.

---

## 👨‍💻 Contact

**Prabhat Kumar**  
Computer Science Engineering Student | Data Engineering Enthusiast

- 📧 Email: osrprabhatyadav4@gmail.com
- 💼 LinkedIn: [Prabhat Kumar](https://www.linkedin.com/in/prabhat-kumar-95059531a)
- 🐙 GitHub: [@prabhatyadav4](https://github.com/prabhatyadav4)

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## ⭐ Show Your Support

If you found this project helpful:

- Give it a ⭐ on GitHub
- Fork it and experiment with your own enhancements
- Share it with others learning data engineering

---

<div align="center">
  <sub>Built with 💙 by Prabhat Kumar</sub>
</div>
