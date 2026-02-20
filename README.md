# Telco Subscriber ETL — PySpark

## Overview

This project implements a PySpark ETL pipeline to process telecom subscriber data using an initial (historical) load followed by incremental (delta) updates. The pipeline enriches subscriber data through joins and produces a curated dataset.

---

## Tech Stack

* Python
* PySpark
* Spark SQL
* JDBC
* CSV

---

## ETL Workflow

### Initial Load

* Extract full datasets from SQL via JDBC
* Store raw data as CSV
* Load into Spark
* Join subscriber, address, city, country, and plan tables
* Create baseline enriched dataset

### Incremental Load

* Read delta datasets
* Apply transformations using Spark SQL
* Generate incremental subscriber updates

### Merge

* Union historical and incremental data
* Deduplicate using window functions
* Select latest record per subscriber
* Write final curated output

---

## Run

Update configs and execute:

```id="p6rjzq"
python extract_historical_data_from_sql.py
python subscriber_details_final.py
```

---

## Concepts Demonstrated

* Initial & incremental ETL loading
* DataFrame joins
* Spark SQL transformations
* Window-based deduplication
* Config-driven pipeline design

