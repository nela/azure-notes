# Azure Database and Analytics Services

[Introduction](https://docs.microsoft.com/en-us/learn/modules/azure-database-fundamentals/introduction) - (useless info)

## Azure Cosmos DB

[Module unit](https://docs.microsoft.com/en-us/learn/modules/azure-database-fundamentals/azure-cosmos-db)

Azure Cosmos DB is a globally distributed, multi-model database service.

Features:
- Elastically and independently scales throughput.
- Supports schema-less data (NoSQL?)
- Stores data in atom-record-sequence (ARS) format at the lowest level. The
data is then abstracted and projected as an API, that is specified upon
creating the database: SQL, MongoDB, Cassandra, Tables and Gremlin.
- The level of flexibility in the API allows for comfortable migration from
on-prem.

## Azure SQL Database

[Module unit](https://docs.microsoft.com/en-us/learn/modules/azure-database-fundamentals/azure-sql-database)

Relational database based on the latest stable version of the MSSQL Server
database engine. High-performance, reliable, fully managed and secure database.

Features:
- PaaS database engine. It handles most of the db management functions such as
upgrading, patching, backups and monitoring without user involvement.
- 99.99% availability. Built-in high-availability, backups and other common
maintenance operations.
- MS handles all updates to the SQL and OS code.
- Enables processing both relational data and non-relational, such as graphs,
  JSON, spatial and XML.
- Advanced processing features: high-performance, in-memory technologies and
intelligent query processing.

Migration can be done using the Azure Database Migration Service. MS Data
Migration Assistant can generate assessment reports that provide
recommendations to help guide through required changes.

### From the exercise
- Firewall can be enabled. In that case, the access IP address needs to be
enabled in a firewall rule.

## Azure Database for MySQL

[Module unit](https://docs.microsoft.com/en-us/learn/modules/azure-database-fundamentals/azure-mysql-database)

Relational database based on MySQL Community database engine, versions 5.6, 5.7
and 8.0.

Features:
- Built-in security, fault tolerance and data protection. Enterprise-grade
security and compliance.
- 99.99% availability SLA, powered by a global network of
Microsoft-managed datacenters.
- Point-in-time restore to recover a server to an earlier state, as far back as
35 days.
- Predictable performance and inclusive, pay-as-you-go pricing.
- Scale as needed, within seconds.
- Ability to protect sensitive data at-rest and in-motion.
- Automatic backups.

Azure Database Migration Service helps for migration to MySQL as well. MySQL
provides several service tiers with different performance and capabilities to
support lightweight to heavyweight workloads.

## Azure Database for PostreSQL

[Module unit](https://docs.microsoft.com/en-us/learn/modules/azure-database-fundamentals/azure-postgresql-database)

Relational database based on the community version of the open-source PostreSQL
engine.

Features:
- Built-in high-availability with no additional configuration, replication or
cost required.
- Predictable performance with simple and flexible pricing. Tier choices
include software patching, automatic backups, monitoring and securtity.
- Scale as needed.
- Adjustable automatic backups and point-in-time restore for up to 35 days.
- Enterprise-grade security and compliance to protect sensitive data at-rest
and in-motion: encryption on disk and SSL encryption between client and server.

Azure DB for PostreSQL is available in two options: **Single Server** and
**Hyperscale (Citus)**.

### Single Server

Deployment option delivers:
- Built-in high-availability, 99.99% SLA with no additional cost.
- Predictable performance and inclusive, pay-as-you-go pricing.
- Vertical scale as needed.
- Monitoring and alerting to assess your server.
- Enterprise-grade security and compliance.
- Ability to protect sensitive data at-rest and in-motion.
- Automatic backups and point-in-time restore up to 35 days.

Pricing tiers:
- Basic
- General Purpose
- Memory Optimized

### Hyperscale (Citus)

Horizontally scales queries across multiple machines by using sharding. Its
query engine parallelizes incoming SQL queries across servers for faster
responses on larger datasets. Serves applications that require greater scale
and performance, generally workloads approaching end exceeding 100GB of data.

This deployment options supports multi-tenant applications, real-time
operational analytics, and high throughput transactional workloads.

## Azure SQL Managed Instance

[Module unit](https://docs.microsoft.com/en-us/learn/modules/azure-database-fundamentals/azure-sql-managed-instance)

A PaaS db engine that provides the broadest SQL Server db engine compatibility
with all the benefits of a fully managed platform as a service. Offers many of
the same features as Azure SQL Ddatabase.

Features:
- Built-in high-availability and 99.99% uptime SLA
- Automated backups and a **configurable** backup retention period
- Supports Cyrillic characters for collation (Azure SQL Database uses only the
  default `SQL_Latin1_General_CP1_CI_AS` server collation)

[Detailed list](https://docs.microsoft.com/en-us/azure/azure-sql/database/features-comparison) of differences between Azure SQL Database and Azure SQL Managed
Instance.

Azure Database Migration Service can be utilized for migration, or using
a native backup and restore.

[Detailed description](https://docs.microsoft.com/en-us/azure/azure-sql/migration-guides/managed-instance/sql-server-to-managed-instance-guide) of the migration
process.

## Big Data and Analytics

[Module unit](https://docs.microsoft.com/en-us/learn/modules/azure-database-fundamentals/azure-big-data-analytics)

Microsoft Azure provides a broad range of technologies and services to provide
big data and analytic solutions, including Azure Synapse Analytics, Azure
HDInsight, Azure Databricks and Azure Data Lake Analytics.

### Azure Synapse Analytics

[Detailed? docs](https://docs.microsoft.com/en-us/azure/synapse-analytics/)


A limitless(?) analytics service that brings together enterprise data
warehousing and big data analytics. Data can be queried by either using
serverless or provisioned resources at scale. Unified experience to ingest,
prepare manage and serve data for immediate business intelligence and ML needs.

### Azure HDInsight

[Detailed docs](https://azure.microsoft.com/en-us/services/hdinsight/)

Fully managed, open-source analytics service for enterprises. Supports
open-source frameworks such as Apache Spark, Apache Hadoop, Apache Kafka,
Apache HBase, Apache Storm and ML Services. Supports a broad range of scenarios
such as extraction, transformation, and loading (ETL), data warehousing, ML and
IoT.

### Azure Databricks

[Detailed docs](https://azure.microsoft.com/en-us/services/databricks/)

Helps unlock insights from all your data and build AI solutions. Apache Spark
environment can be set up in minutes, and then autoscaled and collaborated on
shared projects in an interactive workspace. Supports Python, Scala, R, Java
and SQL as well as data science frameworks and libs including TensorFlow,
PyTorch and scikit-learn.

### Azure Data Lake Analytics

[Detailed docs](https://azure.microsoft.com/en-us/services/data-lake-analytics/)

On-demand analytics job service that simplifies big data. Instead of managing,
you write queries to transform your data and extract valuable insights.
Pay-as-you-go model.
