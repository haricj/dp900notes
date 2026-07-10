# DP-900 Azure Data Fundamentals Notes (Part 2)

> Modules 7–10

---

# Table of Contents

- Module 7 – Identify Azure Data Services
- Module 8 – Azure SQL Services
- Module 9 – Azure Storage Services
- Module 10 – Azure Cosmos DB

---

# Module 7 — Identify Azure Data Services

Microsoft Azure provides managed data services for both transactional and analytical workloads.

---

## Azure SQL

A family of managed SQL Server services.

### Services

- Azure SQL Database
- Azure SQL Managed Instance
- SQL Server on Azure Virtual Machines

Use Cases

- Business applications
- Web applications
- ERP systems
- Reporting databases

---

## Azure Database for Open Source

Supports popular relational databases.

Available Services

- Azure Database for MySQL
- Azure Database for PostgreSQL
- Azure Database for MariaDB

Benefits

- Automatic backups
- Automatic patching
- High availability
- Built-in monitoring
- Easy scaling

---

## Azure Storage

Azure Storage provides massively scalable cloud storage.

Storage Types

| Service | Stores |
|----------|--------|
| Blob Storage | Images, videos, documents |
| Data Lake Storage Gen2 | Big Data |
| Azure Files | SMB File Shares |
| Azure Tables | NoSQL Key-Value |

---

## Azure Cosmos DB

Microsoft's globally distributed NoSQL database.

Supports

- JSON Documents
- Key-Value
- Graph
- Column Family

Features

- Automatic indexing
- Global replication
- Low latency
- Massive scalability

---

## Azure Data Factory

Purpose

- Data Integration
- ETL
- ELT

Components

- Linked Services
- Pipelines
- Activities
- Datasets
- Triggers

---

## Azure Synapse Analytics

Enterprise analytics platform.

Capabilities

- SQL Data Warehouse
- Apache Spark
- Pipelines
- Data Explorer

Best For

- Enterprise analytics
- Data Warehousing
- Big Data

---

## Azure Databricks

Apache Spark platform.

Supports

- Python
- Scala
- SQL
- R

Common Uses

- Machine Learning
- Data Engineering
- Streaming Analytics

---

## Azure HDInsight

Managed Hadoop ecosystem.

Supports

- Hadoop
- Spark
- Kafka
- Hive
- HBase

---

## Azure Stream Analytics

Processes streaming data in real time.

Common Sources

- Event Hub
- IoT Hub

Common Outputs

- Power BI
- SQL Database
- Blob Storage

---

## Microsoft Fabric

Unified SaaS analytics platform.

Capabilities

- Data Factory
- Lakehouse
- Warehouse
- Data Science
- Real-Time Analytics
- Power BI
- OneLake

---

# Azure Services Overview

```text
Applications
      │
      ▼
Azure SQL
Azure Storage
Cosmos DB
      │
      ▼
Azure Data Factory
      │
      ▼
Synapse / Fabric
      │
      ▼
Power BI
```

---

# Module 8 — Azure SQL Services

Azure SQL is Microsoft's cloud-based SQL Server platform.

---

## SQL Server on Azure Virtual Machine

Service Type

Infrastructure as a Service (IaaS)

Characteristics

- Full SQL Server
- Complete OS access
- Full administration

Advantages

- Lift-and-shift migration
- Full compatibility
- Maximum flexibility

Best For

- Existing SQL Server applications
- Legacy systems

---

## Azure SQL Managed Instance

Service Type

Platform as a Service (PaaS)

Characteristics

- Managed SQL Server
- Near 100% compatibility
- Supports multiple databases

Advantages

- Automatic patching
- Automatic backups
- Reduced administration

Best For

- Enterprise migrations
- Existing SQL Server workloads

---

## Azure SQL Database

Service Type

Platform as a Service (PaaS)

Characteristics

- Fully managed
- Automatic updates
- Automatic backups
- High availability

Deployment Options

### Single Database

Dedicated resources.

Best For

- Individual applications

---

### Elastic Pool

Multiple databases share resources.

Advantages

- Lower cost
- Better resource utilization

---

## SQL Comparison

| Service | Type | Best For |
|----------|------|----------|
| SQL VM | IaaS | Lift-and-shift |
| Managed Instance | PaaS | Existing SQL Server |
| SQL Database | PaaS | Cloud-native apps |

---

## High Availability

Azure SQL provides

- 99.99% uptime
- Automatic failover
- Automatic backups
- Disaster recovery

---

## Security Features

- Transparent Data Encryption (TDE)
- Always Encrypted
- Azure Active Directory Authentication
- Firewall Rules
- Threat Detection

---

# Module 9 — Azure Storage Services

Azure Storage stores structured, semi-structured, and unstructured data.

---

# Azure Blob Storage

Purpose

Store unstructured data.

Examples

- Images
- Videos
- PDFs
- Backup files
- Audio

---

## Blob Types

### Block Blob

Best For

- Images
- Documents
- Videos

Maximum Size

190.7 TB

---

### Page Blob

Best For

- Virtual Hard Disks

Characteristics

- Random Read/Write

---

### Append Blob

Best For

- Logs
- Audit Trails

Characteristics

- Append only

---

## Blob Access Tiers

| Tier | Usage |
|------|-------|
| Hot | Frequently accessed |
| Cool | Occasionally accessed |
| Archive | Rarely accessed |

---

## Blob Features

- Versioning
- Snapshots
- Soft Delete
- Lifecycle Management
- Change Feed

---

# Azure Data Lake Storage Gen2

Purpose

Store massive amounts of analytical data.

Characteristics

- Hierarchical namespace
- HDFS compatible
- Big Data optimized

Used By

- Synapse Analytics
- Databricks
- Fabric
- Spark

---

# Azure Files

Cloud SMB File Shares.

Protocols

- SMB
- NFS

Performance

- Standard
- Premium

Common Uses

- Lift-and-shift
- Shared folders
- File servers

---

# Azure Table Storage

NoSQL Key-Value database.

Characteristics

- Semi-structured
- Partition Key
- Row Key
- No joins
- No foreign keys

Advantages

- Extremely scalable
- Low cost
- Fast lookup

---

# Storage Comparison

| Service | Data Type | Best Use |
|----------|-----------|----------|
| Blob | Unstructured | Files |
| Data Lake | Big Data | Analytics |
| Files | Shared Files | SMB |
| Tables | Key-Value | NoSQL |

---

# Module 10 — Azure Cosmos DB

Azure Cosmos DB is Microsoft's globally distributed NoSQL database.

---

## Key Features

- Multi-model
- Global replication
- Automatic indexing
- Low latency
- Elastic scalability

---

## Supported APIs

| API | Database Type |
|------|---------------|
| SQL API | JSON Documents |
| MongoDB API | BSON Documents |
| Cassandra API | Column Family |
| Gremlin API | Graph |
| Table API | Key-Value |

---

## Consistency Levels

| Level | Description |
|---------|------------|
| Strong | Highest consistency |
| Bounded Staleness | Slight delay |
| Session | User session consistency |
| Consistent Prefix | Ordered updates |
| Eventual | Fastest, least consistent |

---

## Common Use Cases

### IoT

- Sensor data
- Device telemetry

---

### Gaming

- Player profiles
- Leaderboards
- Sessions

---

### Retail

- Product catalog
- Shopping cart

---

### Mobile Applications

- User profiles
- Social apps

---

## Cosmos DB Architecture

```text
Application
      │
      ▼
API Layer
(SQL / Mongo / Cassandra / Gremlin)
      │
      ▼
Cosmos DB
      │
      ▼
Automatic Partitioning
      │
      ▼
Global Replication
```

---

# SQL vs Cosmos DB

| Azure SQL | Cosmos DB |
|------------|-----------|
| Relational | NoSQL |
| Fixed Schema | Flexible Schema |
| ACID | Configurable Consistency |
| SQL Tables | JSON Documents |
| OLTP | Web-scale Applications |

---

# Exam Tips

✅ Know the differences between SQL Database, Managed Instance, and SQL VM.

✅ Memorize Blob Storage types.

✅ Understand Blob Storage access tiers.

✅ Know Azure Table Storage limitations.

✅ Remember Cosmos DB APIs.

✅ Learn Cosmos DB consistency levels.

✅ Understand which Azure Storage service fits each scenario.

---

# Quick Revision

| Service | Purpose |
|----------|----------|
| Azure SQL | Relational Database |
| Blob Storage | Files |
| Data Lake | Big Data |
| Azure Files | SMB Shares |
| Azure Tables | Key-Value |
| Cosmos DB | Multi-model NoSQL |
| Data Factory | ETL |
| Synapse | Analytics |
| Databricks | Apache Spark |
| Stream Analytics | Real-Time Data |
| Fabric | Unified Analytics Platform |