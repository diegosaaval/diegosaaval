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

### MIDAS | Financial Data Pipeline · [repo](https://github.com/diegosaaval/midas-data-pipeline)

Daily batch pipeline that turns the raw files of a fintech into trusted gold tables
(landing → bronze → silver with PySpark → gold with dbt), orchestrated with Airflow.

Key concepts:

- Medallion architecture and data contracts
- Quarantine with reasons, deduplication and late-arriving data
- Schema evolution and idempotent reprocessing (dynamic partition overwrite)
- Spark optimization: broadcast joins, partition pruning, window functions, salting for skew
- Live stage view: per-stage rows, retries, quarantine and Spark explain plans
- CI with tests, dbt parse, Airflow DAG validation, pip-audit, CodeQL and Docker builds

### ATLAS | Data Quality & Reliability Monitor · [repo](https://github.com/diegosaaval/atlas-data-quality)

Monitor that validates every table as soon as it lands: on time, complete,
compliant with business rules and behaving as usual. One incident per table,
with evidence and an escalation email.

Key concepts:

- Availability, weekday-aware volume and schema monitors
- Business rules created without code and compiled to SQL
- Statistical outliers with a robust baseline (median, MAD, standard deviation)
- Incident management with automatic resolution and run links back to the pipeline
- Connectors to Parquet/CSV sources, local or published by URL
- AI only explains: deterministic checks decide

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
- Data: PySpark, dbt, DuckDB, Pandas, Impala, Parquet, ETL, batch pipelines
- Orchestration and delivery: Apache Airflow, Docker, GitHub Actions (CI/CD), Render
- Reliability: data quality, data contracts, idempotency, retries, checkpointing, caching
- Tools: Git, Azure DevOps, FastAPI, Streamlit, HTML, Power BI

## Engineering Approach

I use Spec-Driven Development for AI-assisted engineering:

1. Define requirements and constraints.
2. Establish acceptance criteria.
3. Design the solution and split the work.
4. Implement with AI assistance where useful.
5. Test and verify the result against the specification.

## Current Focus

Taking MIDAS to AWS:

- S3, Glue Catalog and Athena
- Terraform (least-privilege IAM)
- dbt on Athena with Apache Iceberg

## Contact

- LinkedIn: https://www.linkedin.com/in/diegosaaval/
- Email: diegosaaval@gmail.com
