### Telco Subscriber ETL — PySpark
#### About

This project is for practicing PySpark ETL.
It loads full data first and then processes incremental updates.
Tables are joined and a final subscriber dataset is generated.

#### Steps

#Extract full data from SQL and save as CSV

#Load into Spark and join tables

#Read incremental files and apply same logic

#Merge data, remove duplicates, keep latest record

#Write final output

#### Run
python extract_historical_data_from_sql.py                                                                                                                             
python subscriber_details_final.py
