# ACLED

## Objective

Building data pipeline using Armed Conflict Location & Event Data Project (ACLED) API

## Problem Statement

The Armed Conflict Location & Event Data Project (ACLED) collects real-time data on the locations, dates, actors, fatalities, and types of all reported political violence and protest events around the world. Let's imagine that you are working for a media organization and you want to bring processed version of the ACLED data to your analysts so that they can generate war and conflict related insights for their stories.

Your goal is to design and develop a data pipeline for it.

## Architecture Diagram

![process_flow](https://user-images.githubusercontent.com/62965911/210161885-38b0a8ef-49d9-49a0-b663-5bbecb51bd77.svg)

## What you'll build

1. Data pull from ACLED api
2. CSV data ingestion into Postgres database
3. Use PySpark for data transformation
4. Store the intermediary and final data into S3
5. Develop Data pipeline with Airflow
6. Create and Trigger the Glue crawler using Airflow operator
7. Run the analysis in Athena
8. Setting up and using connections and variables in Airflow
9. Send an Email to stakeholders about pipeline execution status

## DAG Run instructions

1. Create a free account on ACLED
2. Get the API key and add in the DAG
3. Install the python libraries mentioned in the DAG
4. Set the environment variables - ACLED key and user, S3 bucket and AWS credentials
5. Create a Glue crawler named `acled`
6. Modify the DAG - update name, owner and change catchup, scheduling and other info as required
7. Run the DAG

:::note
We first tried pipeline 1 but due to limitation in API requests, we decided to go with pipeline 2.
:::

## Solution

```
├── [ 86K]  01-sa-data-ingestion.ipynb
├── [ 59K]  airflow
│   ├── [ 49K]  airflow.cfg
│   ├── [9.0K]  dags
│   │   ├── [4.7K]  acled_v1.py
│   │   └── [4.2K]  acled_v2.py
│   └── [ 403]  run.sh
└── [2.2K]  lab-2.md

 147K used in 2 directories, 6 files
```