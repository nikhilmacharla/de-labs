# Data Quality Pipeline

## Objective

Simple EL Pipeline with Data Quality Checks Using Redshift and Great Expectations

In this lab, we are going to load the NYC Taxi data into Redshift warehouse and then validate the data using great expectations. The process will be converted to a pipeline using Airflow.

## Solution

```
.
├── [6.6K]  01-sa-main.ipynb
├── [7.7K]  _100-data-transformation-dbt.md
├── [3.0K]  _README.md
├── [5.1K]  _robust-data-pipeline.mdx
├── [ 49K]  airflow.cfg
├── [ 19K]  airflow_pipeline.ipynb
├── [ 15K]  dags
│   ├── [1.5K]  asparsh_robust_dag.py
│   ├── [1.6K]  asparsh_robust_dag_2.py
│   ├── [1.6K]  asparsh_robust_dag_3.py
│   ├── [1.6K]  asparsh_robust_dag_4.py
│   ├── [2.0K]  csv_json.py
│   ├── [1.4K]  dummy_dag.py
│   ├── [2.3K]  etl.py
│   ├── [1.3K]  robust_dag.py
│   └── [1.5K]  robust_dag0.py
├── [ 58K]  data.zip
├── [ 15K]  dbt
│   ├── [ 571]  _README.md
│   ├── [  96]  analysis
│   ├── [ 367]  dbt_project.yml
│   ├── [  96]  macros
│   ├── [2.7K]  models
│   │   └── [2.6K]  taxi
│   │       ├── [ 362]  schema.yml
│   │       ├── [1.7K]  staging
│   │       │   ├── [1.1K]  schema.yml
│   │       │   ├── [ 292]  taxi_trips_stage.sql
│   │       │   └── [ 173]  taxi_zone_lookup_stage.sql
│   │       └── [ 396]  trips_with_borough_name.sql
│   ├── [ 252]  profiles.yml
│   ├── [ 497]  requirements.txt
│   ├── [ 10K]  seeds
│   │   └── [ 10K]  taxi_zone_lookup.csv
│   ├── [  96]  snapshots
│   └── [  96]  tests
├── [ 18K]  great_expectations
│   ├── [1.9K]  checkpoints
│   │   ├── [ 910]  yellow_tripdata_sample_2019_01.yml
│   │   └── [ 910]  yellow_tripdata_sample_2019_02.yml
│   ├── [2.2K]  expectations
│   │   └── [2.0K]  my_suite.json
│   ├── [4.2K]  great_expectations.yml
│   ├── [ 987]  plugins
│   │   └── [ 891]  custom_data_docs
│   │       └── [ 795]  styles
│   │           └── [ 699]  data_docs_custom_styles.css
│   └── [8.9K]  scripts
│       ├── [ 581]  checkpoint_taxi_data_load_2019_3.py
│       ├── [ 919]  checkpoint_taxi_data_load_2019_3.yml
│       ├── [ 556]  create_checkpoint.py
│       ├── [ 556]  create_checkpoint_taxi_data_load_2019_1.py
│       ├── [ 784]  create_datasource.py
│       ├── [ 893]  my_checkpoint.yml
│       ├── [ 915]  my_checkpoint_taxi_data_load_2019_2.yml
│       ├── [ 915]  my_checkpoint_taxi_data_load_2019_3.yml
│       ├── [ 929]  sparsh_my_checkpoint_taxi_data_load_2019_3.yml
│       ├── [ 556]  taxi_data_load_2019_1.py
│       └── [1.0K]  yellow_tripdata_taxi_checkpoints.py
├── [ 549]  lab-7-airflow-redshift-ge.md
├── [ 46K]  main.ipynb
├── [246K]  nbs
│   ├── [ 72K]  Data_Engineering_Lab___Airflow,_dbt_and_Great_Expectations.ipynb
│   ├── [ 54K]  Data_Engineering_Lab___Great_Expectations.ipynb
│   ├── [116K]  Data_Engineering_Lab___Transforming_Data_with_dbt.ipynb
│   └── [4.8K]  session1.ipynb
├── [ 153]  requirements.txt
└── [ 545]  setup-simple.sh

 491K used in 18 directories, 50 files
```