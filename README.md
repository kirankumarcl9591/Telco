### Telco Subscriber ETL — PySpark

## Overview

I built this project to practice implementing an ETL workflow in PySpark using telecom subscriber data.
It starts with loading historical data and then processes incremental updates to keep the dataset current.
The pipeline performs joins across multiple tables and produces a curated subscriber output.

## Tech Stack

* Python
* PySpark
* Spark SQL
* JDBC
* CSV

## Workflow

### Initial Load

* Extract full datasets from SQL using JDBC
* Save raw data as CSV
* Load into Spark and join subscriber, address, city, country, and plan data
* Generate the baseline dataset

### Incremental Load

* Read delta/update files
* Apply transformations using Spark SQL
* Produce incremental subscriber updates

### Final Merge

* Combine historical and incremental datasets
* Remove duplicates using window functions
* Keep the latest record per subscriber
* Write final output

## Run

Update config paths and run:

```
python extract_historical_data_from_sql.py
python subscriber_details_final.py
```

## What I Practiced

* Handling initial vs incremental loads
* PySpark joins and transformations
* Spark SQL processing
* Window-based deduplication
* Structuring modular ETL scripts

