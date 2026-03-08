# Code_Files Folder Guide

This folder contains the Databricks notebooks, SQL, and pipeline scripts used in the project.

- `bronze_adls.ipynb`: Loads historical and mapping JSON files from ADLS into bronze Delta tables.
- `eventstreamIngest.py`: Reads ride events from Azure Event Hubs and creates the `rides_raw` streaming table.
- `ridesMergeIngest.py`: Merges historical (`bulk_rides`) and streaming (`rides_raw`) records into `stg_rides`.
- `silver_obt.ipynb`: Notebook used to validate parsing, transformation logic, and OBT development steps.
- `silver_obt.sql`: SQL pipeline that builds the streamable `silver_obt` table by joining map/reference tables.
- `model.py`: Builds gold fact and dimension tables with SCD Type 1 and SCD Type 2 logic.


