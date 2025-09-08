# Transit Analytics Pipeline (Airflow + dbt + DuckDB/Postgres + Metabase)

This repository demonstrates an **end-to-end data pipeline** for public transit analytics.  
It ingests **GTFS static data** (routes, trips, stop times) and **mock ridership/turnstile logs**, then transforms the data into a warehouse with dbt, and visualizes insights in dashboards.  
The pipeline is designed to run both in **offline mode (mock data)** and **online mode (download GTFS feeds)**.

---

## 🚆 Project Goals
- Build a reproducible **data pipeline** using open/public transit data
- Showcase skills in **Airflow orchestration**, **dbt modeling**, and **BI dashboards**
- Provide example analytics for ridership, peak hours, headway, and dwell time
- Include **data quality checks** and **offline mock mode** so the project can be run by anyone

---

## 🛠️ Tech Stack
- **Airflow** → workflow orchestration (DAGs, scheduling, retries)
- **dbt** → data modeling and transformation (staging/marts, tests, docs)
- **DuckDB / Postgres** → data warehouse
- **Metabase** → dashboards and visualizations
- (Optional) **MinIO/S3** → data lake for parquet files

---

## 🗺️ Architecture

GTFS.zip + mock_turnstile.csv
└── Airflow (Ingest DAGs)
└── Land (parquet files)
└── dbt (Transform models)
└── Warehouse (DuckDB/Postgres)
└── Metabase (Dashboards)
