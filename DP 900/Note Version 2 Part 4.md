# DP-900 Azure Data Fundamentals - Final Revision & Exam Cheat Sheet

> Last-minute revision notes for Microsoft DP-900

---

# DP-900 Exam Skills Measured

| Domain | Weight |
|---------|---------|
| Describe core data concepts | 15–20% |
| Work with relational data on Azure | 25–30% |
| Work with non-relational data on Azure | 25–30% |
| Describe analytics workloads on Azure | 25–30% |

---

# Core Data Concepts

## Data Types

| Type | Examples | Storage |
|------|----------|---------|
| Structured | SQL Tables | Azure SQL |
| Semi-Structured | JSON, XML | Cosmos DB |
| Unstructured | Images, Video, PDFs | Blob Storage |

---

## OLTP vs OLAP

| OLTP | OLAP |
|------|------|
| Online Transaction Processing | Online Analytical Processing |
| Day-to-day operations | Reporting & Analytics |
| INSERT, UPDATE, DELETE | SELECT |
| Highly normalized | Usually denormalized |
| Small transactions | Large aggregations |
| Banking | Power BI |

---

## Batch vs Stream Processing

| Batch | Stream |
|--------|---------|
| Historical data | Real-time data |
| Scheduled | Continuous |
| High latency | Low latency |
| Payroll | IoT |

---

# Azure SQL Services

| Service | Type | Best Use |
|----------|------|----------|
| SQL VM | IaaS | Lift-and-shift |
| SQL Managed Instance | PaaS | Existing SQL Server |
| Azure SQL Database | PaaS | Cloud-native apps |

---

# Azure Storage Services

| Service | Stores | Best For |
|----------|---------|----------|
| Blob Storage | Files | Images, Video |
| Azure Files | SMB Shares | Shared folders |
| Azure Tables | Key-Value | NoSQL |
| Data Lake Storage Gen2 | Raw Data | Big Data |

---

# Blob Types

| Blob | Use |
|------|-----|
| Block Blob | Images, Documents |
| Page Blob | Virtual Disks |
| Append Blob | Logs |

---

# Blob Access Tiers

| Tier | Usage |
|------|--------|
| Hot | Frequently used |
| Cool | Occasionally used |
| Archive | Rarely accessed |

---

# Azure Cosmos DB

## APIs

| API | Database Model |
|------|----------------|
| SQL API | JSON Documents |
| MongoDB API | BSON Documents |
| Cassandra API | Column Family |
| Gremlin API | Graph |
| Table API | Key-Value |

---

## Consistency Levels

1. Strong
2. Bounded Staleness
3. Session
4. Consistent Prefix
5. Eventual

Memory Tip:

**Strong → Eventual = Highest consistency → Lowest latency**

---

# Data Processing

## ETL

```text
Extract
   ↓
Transform
   ↓
Load
```

Transformation occurs **before** loading.

---

## ELT

```text
Extract
   ↓
Load
   ↓
Transform
```

Transformation occurs **after** loading.

---

# Azure Data Factory

Core Components

- Linked Service
- Dataset
- Activity
- Pipeline
- Trigger

Workflow

```text
Source
   ↓
Linked Service
   ↓
Dataset
   ↓
Pipeline
   ↓
Destination
```

---

# Data Warehouse

Optimized for:

- SQL
- Reporting
- Business Intelligence

Schema

- Star Schema
- Snowflake Schema

---

# Data Lake

Stores

- Structured
- Semi-Structured
- Unstructured

Advantages

- Cheap
- Massive scale
- Raw data

---

# Lakehouse

Combines

- Data Lake
- Data Warehouse

Examples

- Microsoft Fabric Lakehouse
- Delta Lake

---

# Azure Synapse Analytics

Features

- Dedicated SQL Pool
- Serverless SQL Pool
- Spark Pool
- Pipelines

---

# Azure Databricks

Built on

Apache Spark

Languages

- Python
- SQL
- Scala
- R

---

# Microsoft Fabric

Experiences

- Data Factory
- Data Engineering
- Data Warehouse
- Data Science
- Real-Time Intelligence
- Power BI

Storage

OneLake

---

# Power BI Workflow

```text
Connect

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

# Power BI Components

| Component | Purpose |
|------------|----------|
| Desktop | Build Reports |
| Service | Publish & Share |
| Mobile | Consume Reports |

---

# Common Visuals

- Table
- Matrix
- Card
- KPI
- Bar Chart
- Column Chart
- Line Chart
- Pie Chart
- Scatter Plot
- Map
- Treemap

---

# Azure Service Selection Guide

| Scenario | Azure Service |
|------------|---------------|
| Relational Database | Azure SQL Database |
| Existing SQL Server | SQL Managed Instance |
| Lift-and-Shift | SQL VM |
| Images & Videos | Blob Storage |
| Shared Folder | Azure Files |
| NoSQL Key-Value | Azure Tables |
| Global NoSQL | Cosmos DB |
| ETL | Azure Data Factory |
| Big Data | Data Lake Storage |
| Enterprise Analytics | Synapse Analytics |
| Apache Spark | Databricks |
| Streaming Analytics | Azure Stream Analytics |
| Unified Analytics | Microsoft Fabric |

---

# Frequently Tested DP-900 Topics

- ACID properties
- Primary Key vs Foreign Key
- Normalization
- OLTP vs OLAP
- ETL vs ELT
- Blob types
- Blob access tiers
- Azure SQL deployment models
- Azure Cosmos DB APIs
- Cosmos DB consistency levels
- Azure Storage services
- Data Warehouse vs Data Lake
- Star vs Snowflake schema
- Batch vs Stream processing
- Microsoft Fabric architecture
- Power BI workflow

---

# DP-900 Memory Map

```text
                DP-900

                    │
 ┌──────────────────┼──────────────────┐
 │                  │                  │
Core Data      Relational         Non-Relational
 │                  │                  │
OLTP          Azure SQL        Blob Storage
OLAP          SQL Database     Azure Files
ETL           SQL VM           Azure Tables
ELT           Managed Instance Cosmos DB
 │
Analytics
 │
Data Factory
 │
Data Lake
 │
Synapse
 │
Fabric
 │
Power BI
```

---

# Last-Minute Exam Checklist

- [ ] Understand structured vs semi-structured vs unstructured data
- [ ] Compare OLTP and OLAP
- [ ] Explain ETL and ELT
- [ ] Identify Azure SQL deployment options
- [ ] Know Blob Storage types and access tiers
- [ ] Understand Azure Files, Tables, and Data Lake Storage
- [ ] Memorize Cosmos DB APIs and consistency levels
- [ ] Compare Data Warehouse, Data Lake, and Lakehouse
- [ ] Explain Azure Data Factory components
- [ ] Describe Synapse Analytics and Databricks
- [ ] Understand Microsoft Fabric and OneLake
- [ ] Review Power BI workflow and core components

---

# Quick Memory Aids

- **Blob = Binary Files**
- **Azure Files = SMB Shares**
- **Azure Tables = Key-Value**
- **Cosmos DB = Global NoSQL**
- **Data Factory = ETL / ELT**
- **Synapse = Enterprise Analytics**
- **Databricks = Spark**
- **OneLake = Fabric Storage**
- **Power BI = Visualization**