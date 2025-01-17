# AWS Storage Services Guide

Created by: Beatriz Almeida
Created time: January 16, 2025 8:07 PM

# TOPICS

- Object storage services
    - S3
    - S3 Glacier
- File storage services
    - EFS (Elastic File System)
    - FSx
- Block Storage services
    - EBS (Elastic Block Store)
- Relational Database services
    - RDS (Relational Database System)
    - Amazon Aurora
- NoSQL Databases
    - DynamoDB
    - ElastiCache
    - Neptune
- Data Warehousing
    - Redshift
- Data Lakes
    - LakeFormation
- Backup and Archival
    - AWS Backup
- Hybrid and Edge Storage
    - Storage Gateway
    - SnowBall Family
- Specialized Databases
    - QLDB (Quantum Ledger Database)
    - Timestream
    - OpenSearch Service

---

## **1. Object Storage**

- **Amazon S3 (Simple Storage Service):** Scalable object storage for general-purpose use, including backups, archives, and big data analytics.
- **Amazon S3 Glacier:** Low-cost archival storage with retrieval options ranging from milliseconds to hours.

## **2. File Storage**

- **Amazon EFS (Elastic File System):** Managed file storage for Linux-based workloads with shared access.
- **Amazon FSx:** Fully managed file systems for specialized workloads, including:
    - **FSx for Windows File Server:** File storage for Windows-based applications.
    - **FSx for Lustre:** High-performance file storage for compute-intensive workloads.
    

## **3. Block Storage**

- **Amazon EBS (Elastic Block Store):** Persistent block storage for EC2 instances, optimized for low-latency and high-throughput workloads.

## **4. Relational Databases**

- **Amazon RDS (Relational Database Service):** Managed relational databases with support for:
    - MySQL
    - PostgreSQL
    - MariaDB
    - Oracle
    - Microsoft SQL Server
- **Amazon Aurora:** High-performance relational database compatible with MySQL and PostgreSQL.

**Differences between RDS and Aurora:**

- **Amazon RDS**: For general-purpose workloads, smaller applications, or when you need database engines not supported by Aurora (e.g., Oracle or SQL Server).
- **Amazon Aurora**: For performance-critical, highly available, and large-scale workloads where you need MySQL or PostgreSQL compatibility.

## **5. NoSQL Databases**

- **Amazon DynamoDB:** Fully managed key-value and document database with low-latency performance.
- **Amazon ElastiCache:** In-memory caching for real-time applications, with support for:
    - Redis
    - Memcached
- **Amazon Neptune:** Managed graph database for use cases like social networks and recommendation engines.

## **6. Data Warehousing**

- **Amazon Redshift:** Fully managed data warehouse optimized for large-scale analytics and reporting.

## **7. Data Lakes**

- **AWS Lake Formation:** Service to build and manage secure data lakes for analytics.

Data Lakes:
A data lake is a centralized repository that stores large amounts of structured, semi-structured, and unstructured data in its raw format. It allows businesses to store data at scale and process it later for analytics, machine learning, or other purposes. 

## **8. Backup and Archival**

- **AWS Backup:** Centralized service to automate backups for AWS services like S3, EBS, DynamoDB, RDS, and more.

## **9. Hybrid and Edge Storage**

- **AWS Storage Gateway:** Bridge between on-premises environments and AWS for hybrid storage use cases.
- **AWS Snow Family:** Physical devices for data migration and edge computing, including Snowcone, Snowball, and Snowmobile.

## **10. Specialized Databases**

- **Amazon QLDB (Quantum Ledger Database):** Managed ledger database with immutable and cryptographically verifiable transaction history.
- **Amazon Timestream:** Time-series database for IoT and operational applications.
- **Amazon OpenSearch Service (formerly ElasticSearch Service):** Managed search and analytics engine for log analytics, search, and more.