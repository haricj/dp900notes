# DP-900 Azure Data Fundamentals Notes (Part 3)

> Modules 11–14

---

# Table of Contents

- Module 11 – Data Warehousing
- Module 12 – Data Ingestion Pipelines
- Module 13 – Analytical Platform Services
- Module 14 – Batch & Stream Processing
- Module 15 – Microsoft Fabric
- DP-900 Exam Summary

---

# Module 11 — Data Warehousing

## What is a Data Warehouse?

A **Data Warehouse** is a centralized repository designed for analytical reporting and business intelligence.

Characteristics

- Read-optimized
- Historical data
- Supports BI
- SQL queries
- Large datasets

---

## Traditional Data Warehouse Architecture

```text
Operational Databases
        │
        ▼
   ETL / ELT
        │
        ▼
 Data Warehouse
        │
        ▼
  OLAP Model
        │
        ▼
 Power BI Reports
```

---

## Star Schema

A fact table connected directly to multiple dimension tables.

```text
             Customer
                 │
                 │
Product ─── Fact Sales ─── Date
                 │
                 │
              Store
```

### Advantages

- Fast queries
- Simple design
- Excellent for Power BI

---

## Snowflake Schema

Dimension tables are normalized.

```text
Category
     │
Product
     │
Fact Sales
     │
Customer
     │
Country
```

### Advantages

- Less duplicated data

### Disadvantages

- More joins
- Slightly slower

---

## Fact Table

Stores measurable business events.

Examples

- Sales Amount
- Profit
- Quantity
- Cost

---

## Dimension Table

Stores descriptive information.

Examples

- Customer
- Product
- Date
- Employee
- Store

---

## Data Warehouse Benefits

- Historical analysis
- Faster reporting
- Better performance
- Business Intelligence
- KPI reporting

---

# Module 12 — Data Ingestion Pipelines

## What is Data Ingestion?

Moving data from one or more sources into an analytical platform.

---

## ETL

Extract

↓

Transform

↓

Load

Transformation occurs before loading.

---

## ELT

Extract

↓

Load

↓

Transform

Transformation occurs after loading.

---

## Azure Data Factory Components

### Linked Service

Connection to a data source.

Examples

- SQL Server
- Blob Storage
- Oracle
- SAP

---

### Dataset

Represents the input or output data.

---

### Activity

A single operation.

Examples

- Copy Data
- Execute SQL
- Stored Procedure
- Data Flow

---

### Pipeline

A collection of activities.

Example

```text
Copy Data

↓

Transform

↓

Load SQL Database

↓

Refresh Power BI
```

---

### Trigger

Starts a pipeline.

Types

- Manual
- Schedule
- Event

---

## Data Factory Workflow

```text
Source

↓

Linked Service

↓

Dataset

↓

Pipeline

↓

Activities

↓

Destination
```

---

## Azure Synapse Pipelines

Synapse pipelines are built on Azure Data Factory technology.

Provides

- Data movement
- ETL
- ELT
- Orchestration

---

# Module 13 — Analytical Platform Services

---

# Azure Synapse Analytics

Enterprise analytical platform.

Combines

- SQL Data Warehouse
- Apache Spark
- Data Explorer
- Pipelines

---

## Components

### Dedicated SQL Pool

Traditional Data Warehouse.

Best For

- Structured data
- SQL

---

### Serverless SQL Pool

Query files directly.

Examples

- CSV
- Parquet
- Delta

No infrastructure required.

---

### Apache Spark Pool

Used for

- Python
- Scala
- Machine Learning
- Big Data

---

## Synapse Studio

Unified development environment.

Capabilities

- SQL
- Spark
- Pipelines
- Monitoring
- Notebooks

---

# Azure Databricks

Built on Apache Spark.

Languages

- Python
- SQL
- Scala
- R

Best For

- Machine Learning
- Big Data
- Data Engineering

---

# Azure HDInsight

Managed Hadoop platform.

Supports

- Hadoop
- Spark
- Kafka
- Hive
- HBase

Best For

- Existing Hadoop workloads

---

## Comparison

| Service | Best For |
|----------|-----------|
| Synapse | Enterprise Analytics |
| Databricks | Data Engineering |
| HDInsight | Hadoop Migration |

---

# Module 14 — Batch & Stream Processing

## Batch Processing

Processes data in groups.

Examples

- Payroll
- Monthly Sales
- Billing

Advantages

- Handles huge datasets
- Cost effective

Disadvantages

- Delayed results

---

## Stream Processing

Processes events immediately.

Examples

- IoT
- Sensors
- Banking
- Stock Prices

Advantages

- Real-time

Disadvantages

- More complex

---

## Comparison

| Batch | Stream |
|---------|---------|
| Historical | Real-time |
| High Latency | Low Latency |
| Large Files | Individual Events |
| Scheduled | Continuous |

---

## Azure Stream Analytics

Processes streaming data using SQL-like queries.

Inputs

- Event Hub
- IoT Hub
- Blob Storage

Outputs

- SQL Database
- Blob Storage
- Synapse
- Power BI

---

## Stream Analytics Architecture

```text
IoT Device

↓

Event Hub

↓

Azure Stream Analytics

↓

Power BI Dashboard
```

---

# Apache Spark Streaming

Spark can process

- Batch Data
- Streaming Data

Uses

Structured Streaming

Advantages

- Scalable
- Distributed
- Fault tolerant

---

# Delta Lake

Storage layer for Apache Spark.

Features

- ACID Transactions
- Versioning
- Time Travel
- Schema Enforcement

Common in

- Microsoft Fabric
- Databricks
- Synapse

---

# Module 15 — Microsoft Fabric

Microsoft Fabric is Microsoft's unified analytics platform.

---

## OneLake

Single storage layer.

Benefits

- One copy of data
- Shared across workloads
- Delta format

---

## Fabric Experiences

| Experience | Purpose |
|------------|----------|
| Data Factory | ETL |
| Lakehouse | Big Data |
| Warehouse | SQL Analytics |
| Real-Time Intelligence | Streaming |
| Data Science | Machine Learning |
| Power BI | Reporting |

---

## Fabric Architecture

```text
Data Sources

↓

OneLake

↓

Lakehouse

↓

Warehouse

↓

Power BI
```

---

## Benefits

- SaaS
- Unified platform
- No infrastructure management
- Power BI integrated
- Shared storage
- Delta Lake

---

# DP-900 Power BI Overview

Workflow

```text
Import Data

↓

Transform

↓

Model

↓

Visualize

↓

Publish

↓

Share
```

---

## Power BI Components

### Power BI Desktop

Used for

- Import Data
- Modeling
- Reports

---

### Power BI Service

Used for

- Publish
- Dashboards
- Sharing

---

### Power BI Mobile

Used for

- View Reports
- Dashboards

---

## Power BI Visuals

- Table
- Matrix
- Card
- KPI
- Column Chart
- Bar Chart
- Line Chart
- Pie Chart
- Scatter Plot
- Tree Map
- Map

---

# DP-900 Exam Cheat Sheet

## OLTP

- Transactions
- ACID
- SQL
- Banking

---

## OLAP

- Analytics
- Reporting
- Data Warehouse

---

## Azure SQL

Relational Database

---

## Cosmos DB

NoSQL

---

## Blob Storage

Files

---

## Azure Files

SMB Shares

---

## Azure Tables

Key-Value

---

## Data Lake

Raw Data

---

## Synapse

Enterprise Analytics

---

## Databricks

Apache Spark

---

## Data Factory

ETL / ELT

---

## Stream Analytics

Real-Time Analytics

---

## Microsoft Fabric

Unified Analytics Platform

---

# DP-900 Memory Tips

| Remember | Meaning |
|-----------|---------|
| OLTP | Transactions |
| OLAP | Analytics |
| ETL | Transform before Load |
| ELT | Transform after Load |
| Blob | Files |
| Table Storage | Key-Value |
| Cosmos DB | Multi-model NoSQL |
| SQL Database | Relational |
| Synapse | Data Warehouse |
| Databricks | Spark |
| OneLake | Fabric Storage |
| Power BI | Visualization |

---

# Final Revision Checklist

- ✅ Data Roles
- ✅ Structured vs Unstructured Data
- ✅ Relational vs NoSQL
- ✅ Azure SQL Services
- ✅ Azure Storage Services
- ✅ Azure Cosmos DB
- ✅ ETL vs ELT
- ✅ Data Warehouse
- ✅ Data Lake
- ✅ Lakehouse
- ✅ Synapse Analytics
- ✅ Databricks
- ✅ Microsoft Fabric
- ✅ Power BI
- ✅ Batch vs Stream Processing