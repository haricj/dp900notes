# DP-900 Azure Data Fundamentals Notes

> Comprehensive study notes for Microsoft DP-900: Azure Data Fundamentals

---

# Table of Contents

- Module 1 - Explore Job Roles in the World of Data
- Module 2 - Identify Data Formats
- Module 3 - Explore File Storage
- Module 4 - Explore Databases
- Module 5 - Explore Transactional Data Processing
- Module 6 - Explore Analytical Data Processing

---

# Module 1 — Explore Job Roles in the World of Data

## Overview

Organizations require different data professionals to manage, transform, secure, and analyze data.

---

## Database Administrator (DBA)

### Responsibilities

- Design databases
- Configure database servers
- Maintain availability
- Monitor performance
- Backup and recovery
- Disaster recovery planning
- Security and permissions
- User management

### Primary Goal

Ensure databases remain secure, available, and performant.

---

## Data Engineer

### Responsibilities

- Design data pipelines
- Build ETL / ELT solutions
- Data cleansing
- Data transformation
- Manage analytical data stores
- Monitor pipeline execution
- Maintain data quality

### Common Azure Services

- Azure Data Factory
- Azure Synapse Analytics
- Azure Databricks
- Microsoft Fabric
- Azure Data Lake Storage

---

## Data Analyst

### Responsibilities

- Analyze business data
- Build reports
- Create dashboards
- Discover trends
- Design KPIs
- Produce business insights

### Common Tools

- Power BI
- Excel
- SQL

---

## Other Roles

- Data Scientist
- Data Architect
- Software Engineer
- BI Developer

---

# Module 2 — Identify Data Formats

Data can be classified into three categories.

---

## Structured Data

Characteristics

- Fixed schema
- Rows and columns
- Relational databases
- SQL support

Examples

- Customer table
- Employee table
- Product table

Example

| CustomerID | Name | City |
|------------|------|------|
| 1001 | John | London |

---

## Semi-Structured Data

Characteristics

- Flexible schema
- Self-describing
- Different records can contain different fields

Common Formats

- JSON
- XML

Example

```json
{
    "CustomerID":1001,
    "Name":"John",
    "Phone":"0123456789"
}
```

---

## Unstructured Data

Characteristics

- No schema
- Binary files

Examples

- Images
- Videos
- Audio
- PDFs
- Word Documents

---

# Module 3 — Explore File Storage

Cloud storage stores structured and unstructured data efficiently.

---

## Common File Formats

### CSV

- Comma-separated values
- Human readable
- Structured data

Example

```csv
ID,Name,Country
1,John,Malaysia
2,Ali,Singapore
```

---

### JSON

Hierarchical format

Example

```json
{
  "Employee":{
      "ID":1,
      "Name":"John"
  }
}
```

Advantages

- Flexible
- Easy for APIs
- Lightweight

---

### XML

Example

```xml
<Employee>
    <ID>1</ID>
    <Name>John</Name>
</Employee>
```

Mostly replaced by JSON.

---

### Binary Large Objects (BLOB)

Stores

- Images
- Videos
- Audio
- Documents

---

# Optimized Big Data File Formats

## Avro

Storage Type

Row-based

Advantages

- Schema evolution
- Compression
- Apache Kafka support

Best For

- Streaming data
- Data serialization

---

## ORC

Storage Type

Columnar

Advantages

- Fast queries
- Compression
- Predicate Pushdown

Best For

- Apache Hive

---

## Parquet

Storage Type

Columnar

Advantages

- Excellent compression
- Fast analytics
- Spark optimized

Best For

- Data Lake
- Microsoft Fabric
- Synapse Analytics

---

# Module 4 — Explore Databases

Database

A system used to store and retrieve data efficiently.

---

## Relational Database

Characteristics

- Tables
- Rows
- Columns
- SQL
- ACID
- Primary Keys
- Foreign Keys

Examples

- SQL Server
- Azure SQL
- MySQL
- PostgreSQL

---

## Primary Key

Uniquely identifies a row.

Example

```
CustomerID
```

---

## Foreign Key

Links one table to another.

Example

```
Orders.CustomerID
```

→

```
Customers.CustomerID
```

---

## Normalization

Purpose

Reduce duplicated data.

Benefits

- Data integrity
- Smaller storage
- Easier maintenance

---

## Non-Relational Database

Also known as

NoSQL

Advantages

- Flexible schema
- Massive scalability
- High performance

---

### Key-Value Database

Examples

- Azure Table Storage
- Redis

---

### Document Database

Stores

- JSON
- BSON

Example

Azure Cosmos DB

---

### Column Family

Example

Apache Cassandra

---

### Graph Database

Stores

- Nodes
- Edges

Example

Social Networks

---

# Module 5 — Transactional Data Processing

Also called

OLTP

Online Transaction Processing

Characteristics

- High transaction volume
- Fast inserts
- Fast updates
- ACID compliance

Examples

- Banking
- ATM
- Online Shopping
- Airline Booking

---

## CRUD Operations

| Operation | Description |
|-----------|-------------|
| Create | INSERT |
| Read | SELECT |
| Update | UPDATE |
| Delete | DELETE |

---

## ACID Properties

### Atomicity

Everything succeeds or everything fails.

---

### Consistency

Database always remains valid.

---

### Isolation

Transactions do not interfere.

---

### Durability

Committed transactions are permanent.

---

# Module 6 — Analytical Data Processing

Also called

OLAP

Online Analytical Processing

Purpose

Analyze historical business data.

---

## Typical Analytics Architecture

```text
Operational Database
        │
        ▼
   ETL / ELT
        │
        ▼
   Data Lake
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

## Data Lake

Characteristics

- Raw files
- Cheap storage
- Highly scalable

Examples

- Azure Data Lake Storage Gen2
- Microsoft OneLake

---

## Data Warehouse

Characteristics

- Structured
- SQL optimized
- Reporting

Examples

- Azure Synapse
- Microsoft Fabric Warehouse

---

## Data Lakehouse

Combines

- Data Lake
- Data Warehouse

Benefits

- SQL
- Spark
- Delta Lake

Examples

- Microsoft Fabric Lakehouse
- Delta Lake

---

## Users

### Data Scientist

Works directly with

- Python
- Spark
- Machine Learning

---

### Data Analyst

Works with

- SQL
- Power BI

---

### Business Users

Consume

- Dashboards
- Reports
- KPIs

---

# Summary

| Concept | Key Point |
|----------|-----------|
| Structured Data | Tables |
| Semi-Structured | JSON |
| Unstructured | Images, Videos |
| OLTP | Transactions |
| OLAP | Analytics |
| Data Lake | Raw Files |
| Data Warehouse | Structured Analytics |
| Lakehouse | Data Lake + Warehouse |
| DBA | Database Administration |
| Data Engineer | Pipelines & ETL |
| Data Analyst | Reporting & Insights |

---

**Next:** Module 7 – Identify Azure Data Services, Azure SQL, Azure Storage, Azure Cosmos DB, and Microsoft Fabric.