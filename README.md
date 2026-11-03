# Hi, I'm Isaac Tonyloi 👋

### Data Engineer · Cloud Engineer · Technical Writer

**I build reliable data platforms and self-healing cloud infrastructure, then explain them clearly.**

![Open to work](https://img.shields.io/badge/Open%20to-Data%20%26%20Cloud%20Engineering%20Roles-2ea44f?style=for-the-badge) ![Remote](https://img.shields.io/badge/Remote-Available-0A66C2?style=for-the-badge) ![Upwork](https://img.shields.io/badge/Upwork-Freelancer-14a800?style=for-the-badge&logo=upwork&logoColor=white) [![X](https://img.shields.io/badge/X-@IsaacTonyloi-000000?style=for-the-badge&logo=x&logoColor=white)](https://x.com/IsaacTonyloi) ![Profile views](https://komarev.com/ghpvc/?username=isaactony&style=for-the-badge&color=blueviolet)

---

## 💡 What I Do

| Focus | What I deliver | Tools |
| --- | --- | --- |
| 🗄️ **Data Engineering** | Streaming and batch pipelines, medallion (bronze/silver/gold) lakehouse layers, data lineage and audit trails, data contracts, analytics modeling | Kafka, Spark, Airflow, dbt, PostgreSQL, MinIO, Parquet, OpenLineage |
| ☁️ **Cloud & Infrastructure** | Infrastructure as Code on AWS, auto-scaling and self-healing systems, serverless event-driven apps, chaos engineering, monitoring and alerting | Terraform, AWS (EC2, ALB, ASG, Lambda, S3, CloudWatch, SNS, FIS, IAM, VPC), Docker |
| ⚙️ **Platform & Backend** | Microservices with secure auth, message queues, caching, and CI/CD gates | Spring Boot, Kafka, Redis, Jenkins, Docker |
| ✍️ **Technical Writing** | Docs, tutorials, and articles that make data and cloud concepts easy to follow | Markdown, diagrams, runnable demos |

## 🧰 Toolbox

**Languages**

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white) ![SQL](https://img.shields.io/badge/SQL-4479A1?style=flat-square&logo=postgresql&logoColor=white) ![Java](https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white) ![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white) ![Bash](https://img.shields.io/badge/Bash-4EAA25?style=flat-square&logo=gnubash&logoColor=white) ![HCL](https://img.shields.io/badge/HCL-7B42BC?style=flat-square&logo=hashicorp&logoColor=white)

**Data Engineering**

![Apache Kafka](https://img.shields.io/badge/Apache%20Kafka-231F20?style=flat-square&logo=apachekafka&logoColor=white) ![Apache Spark](https://img.shields.io/badge/Apache%20Spark-E25A1C?style=flat-square&logo=apachespark&logoColor=white) ![Apache Airflow](https://img.shields.io/badge/Apache%20Airflow-017CEE?style=flat-square&logo=apacheairflow&logoColor=white) ![dbt](https://img.shields.io/badge/dbt-FF694B?style=flat-square&logo=dbt&logoColor=white) ![Parquet](https://img.shields.io/badge/Parquet-50ABF1?style=flat-square&logo=apache&logoColor=white) ![OpenLineage](https://img.shields.io/badge/OpenLineage-4B5563?style=flat-square) ![Marquez](https://img.shields.io/badge/Marquez-1F2937?style=flat-square)

**Cloud & Infrastructure as Code**

![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat-square&logo=amazonwebservices&logoColor=white) ![EC2](https://img.shields.io/badge/EC2-FF9900?style=flat-square&logo=amazonec2&logoColor=white) ![S3](https://img.shields.io/badge/S3-569A31?style=flat-square&logo=amazons3&logoColor=white) ![Lambda](https://img.shields.io/badge/Lambda-FF9900?style=flat-square&logo=awslambda&logoColor=white) ![CloudWatch](https://img.shields.io/badge/CloudWatch-FF4F8B?style=flat-square&logo=amazoncloudwatch&logoColor=white) ![Terraform](https://img.shields.io/badge/Terraform-7B42BC?style=flat-square&logo=terraform&logoColor=white) ![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)

**Databases, Storage & Analytics**

![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white) ![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white) ![MinIO](https://img.shields.io/badge/MinIO-C72E49?style=flat-square&logo=minio&logoColor=white) ![Metabase](https://img.shields.io/badge/Metabase-509EE3?style=flat-square&logo=metabase&logoColor=white) ![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=flat-square&logo=streamlit&logoColor=white)

**DevOps & Backend**

![Jenkins](https://img.shields.io/badge/Jenkins-D24939?style=flat-square&logo=jenkins&logoColor=white) ![Spring Boot](https://img.shields.io/badge/Spring%20Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white) ![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white) ![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=github&logoColor=white) ![Make](https://img.shields.io/badge/Make-6D00CC?style=flat-square&logo=gnu&logoColor=white)

## 🏗️ Featured Projects

### 📡 [Call Tower Data Platform](https://github.com/isaactony/cell-tower-monitoring-solution)

An end-to-end data platform for cell tower (RAN) and weather data, running entirely on Docker Compose. Kafka feeds both Spark Structured Streaming for near real-time tables and an hourly Airflow-orchestrated medallion pipeline that lands bronze, silver, and gold layers in a MinIO data lake. Gold KPIs land in PostgreSQL and power a live Streamlit operations dashboard.

**Stack:** Kafka · Spark · Airflow · MinIO · PostgreSQL · Streamlit · Docker

```mermaid
flowchart LR
A[RAN and weather producers] --> B[Kafka]
B --> C[Spark Structured Streaming]
C --> D[Postgres live tables]
B --> E[Bronze: raw Parquet in MinIO]
E --> F[Silver: dedup and typed]
F --> G[Gold: hourly KPIs]
G --> H[Postgres gold tables]
D --> I[Streamlit dashboard]
H --> I
J[Airflow] -.orchestrates.-> E
```

### 🛡️ [Self-Healing AWS Infrastructure](https://github.com/isaactony/self-healing-infra)

Terraform-managed AWS infrastructure that detects and recovers from failure on its own: Auto Scaling Groups behind an Application Load Balancer with health checks across availability zones, CloudWatch dashboards and alarms, SNS alerts, and controlled chaos experiments (CPU stress and instance termination) using AWS Fault Injection Simulator. Built with least-privilege IAM and no hardcoded secrets.

**Stack:** Terraform · AWS (VPC, EC2, ALB, ASG, CloudWatch, SNS, FIS, SSM, IAM) · Spring Boot

### 📬 [Serverless Sentiment Inbox](https://github.com/isaactony/Serverless-Sentiment-Inbox)

A serverless, event-driven pipeline: drop an email into S3 and Lambda parses it, Amazon Comprehend scores the sentiment, keyword rules assign urgency, and the message is filed into sorted folders with a JSON analysis report. Fully deployed with Terraform, with versioned and encrypted storage and least-privilege IAM.

**Stack:** AWS Lambda · S3 · Amazon Comprehend · Terraform · Python

### 🔎 [Data Lineage and Audit Trail](https://github.com/isaactony/DataLineage)

A data governance project that captures lineage from eight example Python jobs (ETL, financial processing, data quality, ML, data lake ingestion, compliance) using OpenLineage, stores it in Marquez on PostgreSQL, and visualizes it as a live lineage graph. Ships with Docker Compose and a pytest suite.

**Stack:** OpenLineage · Marquez · PostgreSQL · Docker · Python

### 🧾 [dbt Data Contracts Demo](https://github.com/isaactony/dbt_contracts)

A small, runnable dbt project showing how a breaking schema change from a producer team gets caught in the pull request instead of surfacing days later in a downstream dashboard.

**Stack:** dbt · SQL · CI

### 🗃️ [pgmigrate](https://github.com/isaactony/pg-migrate)

A dependency-light CLI for versioned, reversible PostgreSQL migrations. Its dry-run runs the real migration inside a transaction and rolls it back, uses advisory locks to prevent racing deploys, validates checksums to detect drift, and refuses to fake safety for non-transactional statements like CREATE INDEX CONCURRENTLY.

**Stack:** Python · PostgreSQL · SQL

### 🛍️ [Retail Customer Analytics](https://github.com/isaactony/retail-customer-analytics)

A Contoso retail analytics stack with an ingestion layer, a warehouse, dbt models, and a Metabase BI layer, all started with Docker Compose and Make.

**Stack:** dbt · Metabase · Docker · Python

### 🧩 [Spring Boot Microservices Platform](https://github.com/isaactony/job-queue-system)

An 8-service microservices system with Eureka discovery, Config Server, an API Gateway, JWT authentication with role-based authorization, Kafka messaging, Redis, PostgreSQL, and file storage, all containerized with Docker.

**Stack:** Java · Spring Cloud · Kafka · Redis · PostgreSQL · Docker

## 🎯 What I Bring To A Team

| | |
| --- | --- |
| 🧱 **Reliability first** | Health checks, retries, locks, transactions, and chaos tests so systems fail safely and recover fast |
| 📐 **Production habits** | Infrastructure as Code, least-privilege IAM, tests, Docker-based reproducibility, and no secrets in git |
| 🔍 **Data trust** | Lineage, contracts, and quality checks so teams can rely on their data |
| ✍️ **Clear communication** | Strong documentation and writing that makes complex systems easy to adopt |

## 📊 GitHub Stats

![GitHub stats](https://github-readme-stats.vercel.app/api?username=isaactony&show_icons=true&theme=tokyonight&hide_border=true&count_private=true) ![Top languages](https://github-readme-stats.vercel.app/api/top-langs/?username=isaactony&layout=compact&theme=tokyonight&hide_border=true)

## 📫 Let's Work Together

I'm open to **Data Engineer** and **Cloud Engineer** roles, and to freelance data, infrastructure, and technical writing projects.

| | |
| --- | --- |
| 🐦 X | [@IsaacTonyloi](https://x.com/IsaacTonyloi) |
| 💼 Freelance | Available on Upwork |
| 🌍 Location | Remote |

*Thanks for stopping by! ⭐ Feel free to explore my repos.*
