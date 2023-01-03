# S3 Postgres Scala

`postgres`, `scala`, `databricks`

## Objective

Build an ETL pipeline that will load the S3 data into Postgres

## Postgres JAR Installation

Upload the Postgres JAR file in Databricks and Install it. 

After installation, it will look like this:

![](./img/databricks-jar-install.png)

## Databricks Notebook Code

Run this code. You can find this code in `s3-postgres-etl.scala` file which can be uploaded in databricks.

![](./img/databricks-code.png)

## Final Data Load

The final data load in Postgres:

![](./img/final-data-load-postgres.png)

## Solution

```
├── [ 160]  assets
│   └── [  64]  download-jar.sh
├── [ 18K]  data
│   └── [ 18K]  data.csv
├── [674K]  img
│   ├── [421K]  databricks-code.png
│   ├── [ 51K]  databricks-jar-install.png
│   └── [201K]  final-data-load-postgres.png
├── [ 636]  lab-15-s3-postgres-scala.md
└── [2.0K]  s3-postgres-etl.scala

 695K used in 3 directories, 7 files
```