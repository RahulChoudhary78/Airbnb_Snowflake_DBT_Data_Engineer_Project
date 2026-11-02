# Airbnb Data Engineering Project | Snowflake & dbt

## Overview
An end-to-end data engineering project that transforms Airbnb datasets using Snowflake and dbt. The project implements a Medallion Architecture to organize data into Bronze, Silver, and Gold layers for analytics and reporting.

## Architecture

**Source Data → Snowflake → dbt Transformations → Analytics-Ready Models**

- **Bronze Layer:** Raw source data ingestion
- **Silver Layer:** Data cleaning, transformation, and standardization
- **Gold Layer:** Business-ready fact tables and analytical models

## Tech Stack

- **Cloud Data Warehouse:** Snowflake
- **Transformation:** dbt Core, SQL
- **Language:** SQL
- **Data Modeling:** Medallion Architecture
- **Version Control:** Git & GitHub

## Key Features

- Modular SQL-based data transformations using dbt
- Bronze, Silver, and Gold data layers
- Incremental data loading
- Slowly Changing Dimension (SCD) Type 2 snapshots
- Reusable dbt macros
- Data quality testing
- Fact and analytical model creation
- Source definitions and model documentation

## Project Structure

```text
AWS_DBT_Snowflake/
├── DDL/
│   └── SQL scripts
├── SourceData/
│   ├── bookings.csv
│   ├── hosts.csv
│   └── listings.csv
├── aws_snowflake_dbt_project/
│   ├── analyses/
│   ├── macros/
│   ├── models/
│   │   ├── bronze/
│   │   ├── silver/
│   │   └── gold/
│   ├── snapshots/
│   ├── tests/
│   ├── dbt_project.yml
│   └── README.md
├── pyproject.toml
└── README.md
```

## Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/RahulChoudhary78/Airbnb_Snowflake_DBT_Data_Engineer_Project.git
cd Airbnb_Snowflake_DBT_Data_Engineer_Project
```

### 2. Set up the Python environment

Install Python and uv, then run:

```bash
uv sync
```

### 3. Configure Snowflake

Configure your Snowflake connection locally using your dbt profile.

**Important:** Never commit credentials, passwords, access tokens, or personal connection details.

### 4. Run dbt

Navigate to the dbt project directory:

```bash
cd aws_snowflake_dbt_project
```

Run the following commands:

```bash
dbt debug
dbt deps
dbt seed
dbt run
dbt test
dbt snapshot
```

Note: Execution order may depend on your Snowflake configuration and project setup.

## Learning Objectives

This project demonstrates practical experience with:

- Cloud data warehousing
- ELT pipeline development
- SQL transformations
- dbt development workflows
- Data modeling and dimensional design
- Incremental pipelines and snapshots
- Data quality and testing
- Git-based version control

## License

This project is licensed under the MIT License. See [LICENSE](LICENSE) for details.

## Author

**Rahul Choudhary**

GitHub: [RahulChoudhary78](https://github.com/RahulChoudhary78)

If you found this project useful, feel free to ⭐ the repository!
