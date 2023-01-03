# Movie Sentiment Airflow

`airflow`, `redshift`, `airflow`, `sentiment-analysis`, `nlp`, `tensorflow`

## Objective

Build a pipeline that expresses the fact artist review sentiment and film review sentiment, based on the data provided by IMDb and TMDb.

The goal of our Data Pipeline is to publish a PDF report to S3 with the following summarised information:

- Top 10 Films
- Worst 10 Films
- Review Sentiment Distibution
- Top 10 Actors/Actresses in Best Reviewed Films
- IMDb Average Voting vs TMDb Sentiment Reviews through Years

Process steps:

1. Modify the variables in DAG
2. Export the Variables before starting airflow
3. Run the DAG

The project follows the follow steps:

* Step 1: Scope the Project and Gather Data
* Step 2: Explore and Assess the Data
* Step 3: Define the Data Model
* Step 4: Run ETL to Model the Data
* Step 5: Complete Project Write Up

## Problem Statement

The project expresses the fact artist review sentiment and film review sentiment, based on the data provided by [IMDb](https://www.imdb.com/) and [TMDb](https://www.themoviedb.org/)

## Data Sources

* [IMDB Large Movie Reviews Sentiment Dataset](https://www.kaggle.com/jcblaise/imdb-sentiments)
* [TMDB Movies (2000-2020) with imdb_id](https://www.kaggle.com/hudsonmendes/tmdb-movies-20002020-with-imdb-id)
* [TMDB Reviews, movies released from 2000 and 2020](https://www.kaggle.com/hudsonmendes/tmdb-reviews-movies-released-from-2000-and-2020)
* [IMDB Cast (Links)](https://datasets.imdbws.com/title.principals.tsv.gz)
* [IMDB Cast (Names)](https://datasets.imdbws.com/name.basics.tsv.gz)

## Choice of Technology

The present solution allows Data Analysts to perform roll-ups and drill-downs into film review sentiment facts linked to both films and actors.

Since the raw data provided into S3 and reported on demand to the Data Analysis Team who can then perform further analysis on the database, a single write step is required, whereas many reads and aggregations will be performer.

Given those requirements, the choice of technology was the following:

1. AWS S3 to store the raw files from IMDb and TMDb films, reviews and casting.
2. AWS Redshift to produce a Data Warehouse with the required dimension and fact tables.
3. Tensorflow to allow us training a model and running the classification
4. Apache Airflow to automate our Data Piepeline.

## Pipeline

![](https://user-images.githubusercontent.com/62965911/210338764-b1199f75-1e0c-437e-8974-d7e7e7cb6a26.png)

## Solution

```
.
├── [ 17K]  DAG\ -\ Movie\ Review\ Sentiment\ Classifier\ Trainer.ipynb
├── [ 68K]  DAG\ -\ Movie\ Review\ Sentiment\ Data\ Warehouse.ipynb
├── [261K]  Data_Engineering_Movie_Review_Sentiment_Analysis_Pipeline.ipynb
├── [ 72K]  Movie\ Review\ Sentiment\ Analysis.ipynb
├── [8.6K]  _report.md
├── [ 59K]  dags
│   ├── [3.3K]  check_no_missing_id_operator.py
│   ├── [ 17K]  data_warehouse_dag.py
│   ├── [1.7K]  model_training_dag.py
│   ├── [2.6K]  s3_download_and_upload_operator.py
│   ├── [ 14K]  s3_pdf_sentiment_report_operator.py
│   ├── [3.7K]  s3_to_redshift_operator.py
│   ├── [2.8K]  s3_unzip_and_upload_operator.py
│   ├── [6.2K]  tensorflow_postgres_model_classification_operator.py
│   └── [8.2K]  tensorflow_review_classifier_trainer_operator.py
├── [1.6M]  images
│   ├── [285K]  dag-data_warehouse.png
│   ├── [224K]  dag-model_training.png
│   ├── [ 11K]  film_review_distro_fig.png
│   ├── [ 11K]  redshift1.png
│   ├── [8.6K]  redshift2.png
│   ├── [293K]  report.png
│   ├── [ 12K]  review_distro_fig.png
│   ├── [222K]  star-cast-film-review-sentiment.png
│   ├── [170K]  star-film-review-sentiment.png
│   ├── [208K]  star-schema.png
│   ├── [177K]  the_movie_db.png
│   ├── [ 18K]  tmdb-logo.png
│   └── [8.4K]  year_review_distro_fig.png
├── [3.3K]  lab-14-movie-sentiment.md
└── [ 247]  model
    └── [ 151]  download.sh

 2.1M used in 3 directories, 29 files
```