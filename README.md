# Hi, I'm Thu Mai 👋

Data Engineer Intern from Ho Chi Minh City, Vietnam. I study Management Information Systems at UEL (VNU-HCM) and I like turning messy source data into tables people can trust.

# 🎯 What I focus on

- **Batch & streaming pipelines:** ELT, log-based CDC and lakehouse architecture
- **Data modeling:** star schemas and medallion layers (bronze → silver → gold)
- **Data quality:** idempotent reruns, validation rules and row-count reconciliation
- **Orchestration:** scheduling and testing pipelines end to end with Airflow and dbt

# 🧩 Projects

<table>
<tr>
<td width="50%" valign="top">

### 🔁 "Reruns create duplicates"
**[NYC Taxi Lakehouse on Azure →](https://github.com/maithethu/nyc-taxi-lakehouse-azure)**

4M+ trips/month with two drifting schemas and 8.19% bad rows.
Delta `replaceWhere` makes every rerun **idempotent (0 duplicates)**. Bad rows go to quarantine, not the bin, and the run fails if bronze → silver → gold counts don't match.

<sub>Data Factory · ADLS Gen2 · Databricks · Delta Lake</sub>

</td>
<td width="50%" valign="top">

### 📉 "The owner can't see revenue"
**[Bike Store Data Warehouse →](https://github.com/maithethu/bike-store-data-warehouse)**

No analytics layer, only a production DB.
Meltano copies the data out through a read-only login, dbt builds a star schema, and mart revenue **matches the source to the cent**. Airflow runs load → transform → test every day.

<sub>Meltano · PostgreSQL · dbt · Airflow · Metabase</sub>

</td>
</tr>
<tr>
<td width="50%" valign="top">

### ⚡ "Analytics queries lock production"
**[Bike Store Lakehouse →](https://github.com/maithethu/bike-store-lakehouse)**

Debezium reads the Postgres WAL instead of running queries, so production never notices.
Changes stream through Kafka into Iceberg, and dbt on Spark keeps gold marts **near real-time**.

<sub>Debezium · Kafka · Iceberg · Spark · Trino · MinIO</sub>

</td>
<td width="50%" valign="top">

### 🧱 "The backend is untestable"
**[Bike Store Web →](https://github.com/maithethu/bike-store-web)**

Clean Architecture keeps business rules separate from frameworks.
Async FastAPI, JWT refresh-token rotation, roles. CI runs **ruff + mypy + unit/integration/E2E** tests on every push.

<sub>FastAPI · SQLAlchemy · Angular · GitHub Actions</sub>

</td>
</tr>
</table>

# 💻 Tech Stack:
![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54) ![Bash](https://img.shields.io/badge/bash-%23121011.svg?style=for-the-badge&logo=gnu-bash&logoColor=white) ![JavaScript](https://img.shields.io/badge/javascript-%23323330.svg?style=for-the-badge&logo=javascript&logoColor=%23F7DF1E) ![dbt](https://img.shields.io/badge/dbt-FF694B?style=for-the-badge&logo=dbt&logoColor=white) ![Apache Airflow](https://img.shields.io/badge/Apache%20Airflow-017CEE?style=for-the-badge&logo=Apache%20Airflow&logoColor=white) ![Apache Kafka](https://img.shields.io/badge/Apache%20Kafka-000?style=for-the-badge&logo=apachekafka) ![MS SQL Server](https://img.shields.io/badge/Microsoft%20SQL%20Server-CC2927?style=for-the-badge&logo=microsoft%20sql%20server&logoColor=white) ![Azure](https://img.shields.io/badge/azure-%230072C6.svg?style=for-the-badge&logo=microsoftazure&logoColor=white) ![Databricks](https://img.shields.io/badge/Databricks-FF3621?style=for-the-badge&logo=databricks&logoColor=white) ![Docker](https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white) ![MinIO](https://img.shields.io/badge/MinIO-C72E49?style=for-the-badge&logo=minio&logoColor=white) ![FastAPI](https://img.shields.io/badge/FastAPI-005571?style=for-the-badge&logo=fastapi)
