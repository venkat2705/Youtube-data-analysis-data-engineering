# Youtube-Data-Analysis-Data-Engineering-Project

## Overview

In this project we focus mainly on how to manage, streamline, and perform analysis on structured and semi-structured youtube videos data based on video category and the trending metrics.

## Project Goals

1. Data Ingestion: We need to build a proper mechanism to ingest data from various sources.
2. ETL System: We always get the data in raw format, so we must transform this data into usable format by using required transformations.
3. Data lake: We get data from different sources so we need to have a centralized repo to store them.
4. Scalability: You never know when we are going to get huge volumes of data, so we need to make sure that our system is able to cope up with that sudden change.
5. Cloud: When we have vast data it is always better to go with cloud because it is easy to use and scalable. Here we are using AWS cloud environment.
6. Reporting: Build a dashboard to better understand the insights.

## Services that we are using for this project

1. Amazon S3: Amazon S3 is an object storage service that provides manufacturing scalability, data availability, security, and performance.
2. AWS IAM: This is nothing but identity and access management which enables us to manage access to AWS services and resources securely.
3. QuickSight: Amazon QuickSight is a scalable, serverless, embeddable, machine learning-powered business intelligence (BI) service built for the cloud.
4. AWS Glue: A serverless data integration service that makes it easy to discover, prepare, and combine data for analytics, machine learning, and application development.
5. AWS Lambda: Lambda is a computing service that allows programmers to run code without creating or managing servers.
6. AWS Athena: Athena is an interactive query service for S3 in which there is no need to load data it stays in S3.

## Dataset Used

This Kaggle dataset contains statistics (CSV files) on daily popular YouTube videos over several months. There are up to 200 trending videos published every day to many locations all over the world. The data for each region is in its own file. The video title, channel title, publication time, tags, views, likes and dislikes, description, and comment count are among the items included in the data. A category_id field, which differs by area, is also included in the JSON file linked to the region

Link: https://www.kaggle.com/datasets/datasnaek/youtube-new

## Architecture used

![AWS_Architecture](https://github.com/venkat2705/Youtube-data-analysis-data-engineering/assets/60357150/1b33b3df-ba47-4c8e-9518-973b3c0c67f3)


## High level project Flow

Kaggle Dataset --> Landing Area --> Glue job and Lambda function --> enriched/cleansed --> ETL pipeline --> Analytics/Reporting --> Quicksight Dashboard.

## Detailed Project Flow

1. Ingest all the data from kaggle data set to an S3 bucket (You can use CLI or direct upload)
2. Now build tables by crawling all the data and build a Glue Catalog for ETL.
3. Go to AWS Lambda to preprocess the data to handle json data to convert into tables (I provided the scripts required) and put in in clean bucket.
4. Again we need to build another crawler on the cleansed data. Now lets go to AWS Athena (Ad hoc query tool) and query our cleaned/enriched data.
5. Its finally time to build an ETL pipeline on our enriched/cleansed data to make it available for analytics purpose. For this process we use AWS Glue Studio  and select the source as Cleaned data and Raw data from glue catalog and join them on category ID. Then store the destination data in new AWS S3 bucket and call it analytics bucket.

![ETL_Pipeline](https://github.com/venkat2705/Youtube-data-analysis-data-engineering/assets/60357150/45f1627f-8087-41b2-b1ca-b89d3ac6a9fd)

6. Lets Do some Visualization using AWS Quicksight and select all the buckets we previously created. We need to visualize on the analytics bucket data and build the dashboard according our requirement.

You need to have good knowledge on AWS services and be able to build required IAM roles and permissions on the fly when required.













