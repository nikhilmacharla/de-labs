# Data Engineering Labs

## Labs

1. [Setup Airflow](./assets/lab-1-setup-airflow.md): Install Airflow in MacOS/Unix on Local/AWS/GCP - `airflow`, `docker`, `ec2`, `ecs`, `composer`, `mwaa`
1. [ACLED Data Pipeline](./assets/lab-2-acled.md): Build data pipeline using ACLED API - `airflow`, `athena`, `postgres`, `api`, `glue`, `s3`, `pyspark`, `sns`
1. [Email Notifications in Airflow](./assets/lab-3-airflow-email.md): Enable email notification in Airflow - `airflow`, `ses`
1. [CSV to JSON ETL Pipeline](./assets/lab-4-airflow-csv-json.md): Building an airflow DAG to convert CSV to JSON - `airflow`, `faker`
1. [Python Airflow connection](./assets/lab-5-airflow-connection.md): Set Airflow connection using Python - `airflow`, `secret-manager`
1. [Scooter ETL Pipeline](./assets/lab-6-airflow-scooter-etl.md): Build an Airflow ETL pipeline using Scooter dataset - `airflow`
1. [Data Quality Pipeline](./assets/lab-7-airflow-redshift-ge.md): Simple EL Pipeline with Data Quality Checks Using Redshift and Great Expectations - `airflow`, `redshift`, `great-expectations`, `nyctaxi`
1. [Bash Echo Pipeline](./assets/lab-8-airflow-bash-echo.md): Building a simple Bash command echo pipeline with Airflow - `airflow`
1. [Github NFT Pipeline](./assets/lab-9-airflow-github-nft.md): Building an ETL pipeline to pull NFT data from Github and store in SQLite database - `airflow`, `api`, `sqlite`
1. [NYC Taxi Fare Prediction](./assets/lab-10-taxi-fare-prediction.md): Airflow Data Pipeline to Train ML model that will predict NYC Taxi Fare prices - `airflow`, `pyspark`, `nyctaxi`

## Techstack

### Database Engines

1. Postgres - An open-source database for both OLTP and OLAP
1. Athena - A serverless database engine service of AWS based on Presto
1. SQLite - A self-contained serverless engine supports OLTP 

### Workflow Orchestration

1. Airflow - An open-source tool for building data pipelines and manage workflows
1. Cloud Composer - A managed Airflow service on Google cloud
1. MWAA - A managed Airflow service on AWS cloud

### Data Ingestion

1. API - Getting data from sources via get/post methods
1. Faker - A python library to generate synthetic data which helps during ingestion/sourcing process

### Cloud Compute

1. EC2 - AWS service for VMs on the cloud
1. Pyspark - Python+Spark for distributed data processing

### Cloud Storage

1. S3 - AWS elastic object storage service

### DevOps

1. Docker - Containerize the applications
2. ECS - AWS service for container orchestration

### Data Quality

1. Great expectations - Python library for data quality and validation

### Notifications

1. SNS - AWS service to send notification emails/sms
1. SES - AWS service to send notification emails

### Credentials Management

1. AWS Secret Manager - comes with encryption and rotation features

### Datasets

1. NYC Taxi

## Training style

1. No docker-based setups: We will not be using Docker to setup tools initially because I believe it is a bad practice to use dockers during learning phase. We should setup things from scratch and then use dockers to automate the processes.

## About me

Hi, I am Sparsh and I am a Data Engineer and a Data Scientist. I provide trainings to individuals and groups. Either you are a fresher looking for a data science/ data engineering jobs, a working professional looking for a career switch into these fields or a curious learner, I got you all covered with these labs.

We will create a customized learning plan as per your goals and then schedule the regular sessions on Google Calendar.

You can connect me via following channels:

1. Email me at `sprsag@gmail.com`
2. Whatsapp me at `+91 838-480-5365`
3. Create a git Issue in this repo