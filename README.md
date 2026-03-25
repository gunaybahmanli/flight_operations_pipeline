# ✈️ Flight Operations Data Engineering Pipeline

An end-to-end Data Engineering project that ingests live flight data from a public API, processes it using Medallion Architecture (Bronze → Silver → Gold), and delivers analytics-ready data for BI dashboards.

---

##  Project Architecture

<!-- 🔽 ADD ARCHITECTURE IMAGE HERE -->
<img width="1301" height="801" alt="Untitled Diagram drawio (5)" src="https://github.com/user-attachments/assets/f8bbf35d-a9a2-4c6d-afe3-cda39c8cb6d2" />


---

##  Dashboard Preview

<!-- 🔽 ADD DASHBOARD IMAGE HERE -->
![Dashboard](./images/dashboard.png)

---

##  Project Overview

This project demonstrates how a real-world data engineering pipeline is built using modern tools like **Apache Airflow**, **Snowflake**, and **Docker**.

The pipeline extracts live flight data from an external API, processes it in multiple layers, and transforms it into structured, analytics-ready datasets for reporting and visualization.

It is designed to simulate a production-level workflow with proper orchestration, scheduling, retry mechanisms, and incremental data processing.

---

##  Key Features

- Ingests **real-time flight data** from a public API
- Fully automated pipeline using **Apache Airflow**
- Implements **Medallion Architecture**
- Processes data in **30-minute time windows**
- Stores analytics-ready data in **Snowflake**
- Supports **incremental loading & historical tracking**
- Designed with **idempotent and rerunnable pipelines**
- Ready for BI tools like Power BI

---

##  Use Case

This project simulates how aviation analytics teams analyze global flight activity to:

- Monitor air traffic trends
- Detect congestion patterns
- Compare flight activity across countries
- Build historical datasets for analytics

>  Note: This project focuses on analytics, not real-time air traffic control.

---

##  Data Architecture (Medallion)

### 🥉 Bronze Layer
- Raw JSON data ingestion from API
- No transformations applied
- Acts as the source of truth

### 🥈 Silver Layer
- Data cleaning and normalization
- Schema structuring
- Removes inconsistencies and duplicates

### 🥇 Gold Layer
- Aggregated KPIs and analytics tables
- Time-windowed metrics (30-minute intervals)
- Optimized for reporting and dashboards

---

## Tech Stack

- **Apache Airflow** – workflow orchestration
- **Python** – data processing
- **Snowflake** – data warehouse
- **REST API** – live flight data ingestion
- **Docker & Docker Compose** – environment setup
- **Power BI** *(optional)* – data visualization

---

## Pipeline Workflow

1. Extract flight data from external API
2. Load raw data into Bronze layer
3. Transform and clean data in Silver layer
4. Aggregate metrics in Gold layer
5. Load final data into Snowflake
6. Serve data for dashboard consumption

---

## Data Engineering Concepts Applied

- Batch processing (near real-time)
- Incremental data loading
- UPSERT logic
- Idempotent pipelines
- Task dependency management
- Error handling & retries
- Data modeling for analytics

---
