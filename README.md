# Diego Alejandro Saavedra

Data & Automation Engineer focused on building reliable data pipelines,
automated workflows and data quality solutions.

## Featured: MIDAS + ATLAS

> **MIDAS turns raw data into gold. ATLAS verifies it is real gold.**

[![MIDAS + ATLAS · watch the 1:49 demo](https://raw.githubusercontent.com/diegosaaval/midas-data-pipeline/main/media/miniatura-midas-atlas.png)](https://youtu.be/PXF2G3ek3ZU)

Two independent projects that talk through a contract (gold tables + manifest, tested in CI). One day tells the whole story: on October 1 the card payment gateway fails and 2 out of 3 card payments are declined. Every record is valid, so the pipeline publishes everything as OK. ATLAS compares the day with its history, sees the approval rate drop from 0.92 to 0.59 (7σ below normal), opens an incident for the owning team and links back to the exact MIDAS run that produced it.

| | **MIDAS** · data pipeline | **ATLAS** · data quality monitor |
|---|---|---|
| **What it does** | Turns the raw files of a fintech (customers, merchants, payments, refunds, chargebacks) into trusted gold tables | Watches every table that lands and answers: on time? complete? valid? behaving as usual? |
| **Highlights** | PySpark medallion (bronze → silver → gold), data contracts, quarantine with reasons, deduplication, late-arriving data, schema evolution, idempotent reprocessing, dbt, Airflow, live stage view | SLA, volume and schema monitors, business rules compiled to SQL, statistical outliers, one incident per table with evidence and an escalation email |
| **Live demo** | [midas-data-pipeline.onrender.com](https://midas-data-pipeline.onrender.com) | [Connected to MIDAS](https://atlas-midas.onrender.com) · [Standalone](https://atlas-data-quality.onrender.com) |
| **Video** | [MIDAS · 2 min](https://youtu.be/KFIgQx3N6a8) | [ATLAS · 2:47](https://youtu.be/R8pWRAv-FZo) |
| **Code** | [diegosaaval/midas-data-pipeline](https://github.com/diegosaaval/midas-data-pipeline) | [diegosaaval/atlas-data-quality](https://github.com/diegosaaval/atlas-data-quality) |
| **Stack** | Python, PySpark, dbt, DuckDB, Airflow, Docker, GitHub Actions | Python, SQL, FastAPI, SQLite, WebSocket, Docker, Render |

<sub>Personal projects with synthetic data. Live demos run on free instances: they may take about a minute to wake up.</sub>

## About

I am an Industrial Engineer with a Data Science focus and experience
in data engineering, automation and analytics within financial services.

I build end-to-end solutions with Python and SQL, incorporating
orchestration, data quality, idempotency, recovery, observability
and operational traceability.

## Selected Work

### ATLAS | Data Quality & Observability Platform

Configuration-driven platform designed to anticipate source failures,
compare primary and replicated data, detect anomalies, reuse valid
results through selective caching and recover interrupted executions
through checkpointing.

Key concepts:

- Data quality and observability
- Configuration-driven source onboarding
- Selective cache invalidation
- Checkpoint and recovery
- Source and replica comparison
- Historical persistence
- Executive dashboard

### NEXO | Calendarized Data Pipeline

End-to-end data pipeline integrating multiple sources and calendar
rules through modular SQL transformations.

Key concepts:

- Input and output validation
- Modular SQL
- Partition filtering
- Idempotent publishing
- Error preservation
- Execution traceability
- Reproducible packaging

## Technical Stack

- Languages: Python, SQL
- Data: Pandas, Impala, Parquet, ETL, batch pipelines
- Engineering: workflow orchestration, scheduling, data modeling
- Reliability: data quality, checkpointing, retries, caching, idempotency
- Tools: Git, Azure DevOps, Streamlit, HTML, Power BI

## Engineering Approach

I use Spec-Driven Development for AI-assisted engineering:

1. Define requirements and constraints.
2. Establish acceptance criteria.
3. Design the solution and split the work.
4. Implement with AI assistance where useful.
5. Test and verify the result against the specification.

## Current Focus

Currently strengthening:

- Apache Airflow
- Docker
- CI/CD
- AWS fundamentals

## Contact

- LinkedIn: https://www.linkedin.com/in/diegosaaval/
- Email: diegosaaval@gmail.com
