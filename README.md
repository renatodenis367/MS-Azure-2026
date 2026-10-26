# Azure Data Fundamentals (DP-900) Project

## Project Overview
This repository contains the practical labs, research, and architectural project completed during the **Azure Data Fundamentals (DP-900)** training course. The project covers the core concepts of cloud computing and demonstrates hands-on experience across relational, non-relational, and analytical data workloads on Microsoft Azure. 

Using a real-world retail scenario ("Paws & Whiskers" pet shop) and guided Skillable labs, this project demonstrates how to design, ingest, and analyze data using various Azure data services.

## Tools & Technologies
- **Microsoft Azure** (Portal, Pricing Calculator)
- **Azure SQL Database** (Relational data)
- **Azure Storage Account & Azure Cosmos DB** (Non-relational data)
- **Microsoft Fabric** (Lakehouse, Eventstreams, Power BI)
- **Azure Data Factory** (Data ingestion/integration)
- **SQL** (Querying and analysis)
- **DP-900 Exam Preparation**

---

## Core Competencies

### 1. Cloud Computing Fundamentals
- **Service Models:** Understanding **IaaS** (Infrastructure as a Service - ideal for enterprises requiring full OS and storage control, like the "DataCore Enterprises" scenario), **PaaS** (Platform as a Service), and **SaaS**.
- **Deployment Models:** Differentiating between Public, Private, Hybrid, and Community clouds based on security and accessibility needs.
- **Cost Management:** Using the Azure Pricing Calculator to estimate enterprise BI solution costs and understanding how compute SKUs, reservations, and support plans impact monthly billing.

### 2. Relational Data & SQL Skills
Completed the "Explore Azure SQL Database" lab. Applied practical SQL skills to analyze structured retail and sales data (e.g., tracking customer demographics, transaction history, and pet inventory). 
- **Querying:** Using `SELECT` and `WHERE` to filter customer records and sales transactions.
- **Sorting & Aggregating:** Using `ORDER BY`, `GROUP BY`, and aggregate functions to summarize sales trends.
- **Joining Tables:** Using `JOINs` to combine customer data with purchase history to extract meaningful business insights.

**Example Query (Retail Analysis):**
```sql
SELECT c.CustomerName, 
       SUM(s.TransactionAmount) AS TotalSpent
FROM Customers c
JOIN Sales s ON c.CustomerID = s.CustomerID
WHERE s.TransactionDate >= '2026-01-01'
GROUP BY c.CustomerName
ORDER BY TotalSpent DESC;
```

### 3. Non-Relational Data Workloads
Completed the "Explore Azure Storage for non-relational data" lab.
- Provisioned and configured **Azure Storage Accounts** (General Purpose V2) and **Azure File Shares**.
- Explored **Azure Cosmos DB** to understand how highly scalable, non-relational databases handle unstructured and semi-structured data.
- Differentiated when to use relational vs. non-relational storage based on data flexibility and structure.

### 4. Analytical Workloads & Data Ingestion
Completed the "Explore fundamentals of large-scale data analytics" lab.
- Explored **Microsoft Fabric Lakehouse** architecture for scalable, cloud-based analytics.
- Understood the role of **Eventstreams** and real-time analytics within Fabric.
- Learned how **Azure Data Factory** and other ingestion methods can automate data movement from on-premises sources (like spreadsheets) into cloud environments.

### 5. Data Security, Governance & Compliance
Contextualized Azure data services within UK and EU laws:
- **Data Protection Act (DPA) 2018 & GDPR:** Highlighted the importance of compliance when storing customer information.
- **Security:** Recommended Azure built-in encryption and access controls to secure data.
- **Computer Misuse Act:** Studied legal frameworks surrounding unauthorized access, modification of computer material, and the distribution of hacking tools.

---

## Business Scenario: "Paws & Whiskers" Retail Architecture
As part of the course project, I proposed a modern data architecture for a growing pet shop transitioning from manual spreadsheets to Azure:
- **Data Modelling:** Designed a relational model for core transactional data (Customers, Inventory, Sales) and a Data Warehouse approach for analytical reporting.
- **Data Formats:** Recommended **CSV** for raw data imports, **JSON** for structured application data, and **Parquet** for optimized analytics.
- **Visualization & Scalability:** Proposed using **Power BI** for real-time management dashboards and leveraging Azure's elastic scalability to accommodate growing datasets.

## Learning Outcomes
- Gained foundational knowledge of core data concepts and Microsoft Azure data services.
- Successfully passed the Skillable labs for Azure SQL Database, Azure Storage, and Microsoft Fabric.
- Developed the ability to recommend appropriate Azure services based on business requirements, data types, and legal constraints.
- Demonstrated proficiency in using SQL to extract insights from structured datasets.
