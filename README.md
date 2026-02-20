# Telco Subscriber ETL — PySpark

## About this project

I built this project while practicing PySpark ETL workflows using telecom-style data.
The idea was to simulate how data is first loaded in bulk and then updated incrementally over time.

The pipeline reads raw data from SQL, processes it in Spark, joins related tables, and produces a cleaned subscriber dataset.

## How it works

**Initial Load**

* Pulls full tables from SQL through JDBC
* Saves them as CSV
* Loads into Spark and joins subscriber, address, city, country and plan data

**Incremental Load**

* Reads update files (delta data)
* Applies the same transformations
* Produces updated subscriber records

**Final Step**

* Combines historical + incremental data
* Removes duplicates using window logic
* Keeps the latest record per subscriber
* Writes final output

## Running it

Update paths in the config files and run:

```
python extract_historical_data_from_sql.py
python subscriber_details_final.py
```

## Why I made this

Mainly to get hands-on with:

* PySpark joins
* Spark SQL
* Handling incremental loads
* Window functions
* Structuring ETL scripts

---

Kiran Kumar
