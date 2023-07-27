# Youtube-Data-Analysis-data-engineering

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

I have attached the architeture Diagram in the files.












