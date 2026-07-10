# Microsoft Azure Data Fundamentals (DP-900) Notes

> Clean Markdown notes based on the DP-900 Master Cheat Sheet.

---

# Table of Contents

1. Core Data Concepts
2. Data Processing
3. Data Roles
4. Relational Data
5. Non-Relational Data
6. Azure Data Services
7. Modern Data Warehouse
8. Power BI
9. Exam Tips

---

# Module 1 – Explore Core Data Concepts

## Types of Data

| Type | Description | Examples |
|-------|-------------|----------|
| Structured | Fixed schema (rows & columns) | SQL Server, Azure SQL Database |
| Semi-Structured | Flexible schema | JSON, XML |
| Unstructured | No predefined schema | Images, Audio, Video, PDF |

---

## Data Processing

### Batch Processing

- Processes large volumes of data together
- Higher latency
- Scheduled execution

Examples

- CSV files
- Monthly sales
- Payroll

### Stream Processing

- Processes data continuously
- Near real-time
- Low latency

Examples

- IoT Sensors
- Online Gaming
- Stock Market
- Live Transactions

---

## Transactional vs Analytical Systems

| OLTP | OLAP |
|------|------|
| Online Transaction Processing | Online Analytical Processing |
| Many small transactions | Large analytical queries |
| Fast inserts/updates | Fast aggregations |
| Normalized | Usually denormalized |
| Banking | Business Intelligence |

---

## Data Analytics Lifecycle

```
Raw Data
    │
    ▼
Data Ingestion
    │
    ▼
Transformation
    │
    ▼
Storage
    │
    ▼
Query
    │
    ▼
Visualization
```

---

# Module 2 – Data Roles

## Database Administrator (DBA)

Responsibilities

- Install databases
- Configure servers
- Backup & Recovery
- Security
- Performance tuning

Tools

- SQL Server Management Studio
- Azure Data Studio
- pgAdmin
- MySQL Workbench

---

## Data Engineer

Responsibilities

- ETL / ELT
- Data Pipelines
- Data Cleansing
- Data Integration
- Big Data Processing

Tools

- Azure Data Factory
- Azure Databricks
- Azure Synapse
- Azure SQL
- Cosmos DB

---

## Data Analyst

Responsibilities

- Analyze data
- Create dashboards
- Build KPIs
- Reports
- Visualizations

Tools

- Excel
- Power BI

---

# Module 3 – Relational Data

## Characteristics

- Tables
- Rows
- Columns
- Fixed schema
- SQL
- ACID

---

## Primary Key

- Unique identifier
- Cannot contain duplicates

Example

CustomerID

---

## Foreign Key

Links two tables together.

Example

Orders.CustomerID → Customers.CustomerID

---

## Index

Improves query performance.

Advantages

- Faster SELECT

Disadvantages

- Uses storage
- Slower INSERT/UPDATE

---

## ACID Properties

| Property | Description |
|----------|-------------|
| Atomicity | All or Nothing |
| Consistency | Valid data only |
| Isolation | Transactions don't interfere |
| Durability | Changes remain after commit |

---

# Module 4 – Non-Relational Data

Characteristics

- Flexible schema
- High scalability
- No joins
- High performance

---

## Types

### Key-Value

Examples

- Azure Table Storage
- Redis

---

### Document Database

Stores

- JSON
- BSON
- XML

Example

Azure Cosmos DB

---

### Column Family

Examples

- Cassandra
- Cosmos DB Cassandra API

---

### Graph Database

Stores

- Nodes
- Edges

Example

Cosmos DB Gremlin API

---

# Azure Storage Services

## Azure Table Storage

Data Type

Semi-structured

Model

Key-Value

Advantages

- Fast
- Cheap
- Highly scalable

Limitations

- No joins
- No foreign keys
- No stored procedures

---

## Azure Blob Storage

Stores

- Images
- Audio
- Video
- Backup

Blob Types

| Type | Use |
|------|-----|
| Block Blob | Images, Files |
| Page Blob | Virtual Disks |
| Append Blob | Logs |

Access Tiers

- Hot
- Cool
- Archive

Features

- Versioning
- Snapshots
- Soft Delete
- Change Feed

---

## Azure File Storage

Supports

- SMB
- File Shares
- Hybrid Storage

Performance

- Standard
- Premium

---

## Azure Cosmos DB

Multi-model NoSQL Database

Supports

- SQL API
- MongoDB API
- Cassandra API
- Gremlin API
- Table API

Advantages

- Global Distribution
- High Availability
- Automatic Indexing
- Low Latency

Consistency Levels

- Strong
- Bounded Staleness
- Session
- Consistent Prefix
- Eventual

---

# Module 5 – Data Analytics

Pipeline

```
Extract
    │
Transform
    │
Load
```

or

```
Extract
    │
Load
    │
Transform
```

---

## ETL

Extract

↓

Transform

↓

Load

---

## ELT

Extract

↓

Load

↓

Transform

---

## Analytics Types

| Type | Question |
|------|----------|
| Descriptive | What happened? |
| Diagnostic | Why happened? |
| Predictive | What will happen? |
| Prescriptive | What should we do? |
| Cognitive | What can AI learn? |

---

# Azure Data Services

## Azure SQL Database

Deployment Models

- Single Database
- Elastic Pool
- Managed Instance

---

## Azure Data Factory

Purpose

- Data Integration
- ETL
- ELT

Concepts

- Linked Service
- Dataset
- Pipeline
- Trigger

---

## Azure Data Lake Storage

Stores

- Raw Data

Supports

- HDFS
- POSIX

---

## Azure Databricks

Apache Spark Platform

Languages

- Python
- Scala
- SQL
- R

---

## Azure Synapse Analytics

Supports

- SQL Pool
- Spark Pool

Capabilities

- Data Warehouse
- Big Data
- PolyBase

---

## Azure Analysis Services

Best For

- Semantic Models
- OLAP
- Power BI

---

# Modern Data Warehouse

Architecture

```
Data Sources
      │
      ▼
Azure Data Factory
      │
      ▼
Azure Data Lake
      │
      ▼
Databricks
      │
      ▼
Synapse Analytics
      │
      ▼
Analysis Services
      │
      ▼
Power BI
```

---

# Power BI

Workflow

```
Connect Data

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

Building Blocks

- Dataset
- Report
- Dashboard
- Tile
- Visualization

---

# Important Ports

| Service | Port |
|----------|------|
| Azure SQL | 1433 |
| PostgreSQL | 5432 |
| MySQL | 3306 |

---

# Exam Tips

✅ Know the difference between OLTP and OLAP.

✅ Memorize Azure Storage services.

✅ Understand ETL vs ELT.

✅ Learn Cosmos DB consistency levels.

✅ Know Blob Storage access tiers.

✅ Remember Azure Data Factory components.

✅ Understand SQL Database deployment models.

✅ Know when to use Synapse vs Analysis Services.

---

# Quick Revision

## Relational

- SQL
- Tables
- ACID
- Foreign Keys

## Non-Relational

- JSON
- Flexible Schema
- High Scalability

## Storage

- Blob → Files
- Table → Key-Value
- File → SMB
- Cosmos → Multi-model

## Analytics

- Data Factory
- Data Lake
- Databricks
- Synapse
- Power BI