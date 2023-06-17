# Spotify-end-to-end-Data-Pipeline-ETL-Project

## Introduction
Spotify Data Pipeline (ETL) Project using Python and AWS
The Pipeline will retrieve data from the Spotify API, transform it to a desired format, and load it into an AWS Data Store

## Architecture
![Architecture Diagram](https://github.com/Areyvansh/Spotify-end-to-end-Data-Pipeline-ETL-Project/blob/main/Spotify-Project-Architecture-Diagram.jpg)

## About Dataset/ API
This API contains information about the Music Artist, Albums annd the Songs retrieved from Spotify which we have scraped using Python and AWS Services - [Spotify API](https://developer.spotify.com/documentation/web-api)

## Services Used
1. **S3 (Simple Storage Service):** Amazon S3 is a highly scalable object oriented service that can store and retrieve any amount of data from anywhere on the web. It is commonly used to store and distribute large media files, data backups, and static website files.
  
2. **AWS Lambda:** AWS Lambda is a serverless computing service that lets you to code without managing servers. You can use Lambda to run code in response to events like changes in S3, DynamoDB,, or other AWS services.

3. **Cloud Watch:** Amazon CloudWatch is a monitoring service for AWS Resources and the Applications you run on them. You can use CloudWatch to collect and track Metrics, collect and monitor Log Files, and set Alarms.

4. **AWS Glue Crawler:** AWS Glue Crawler is a fully managed service that automatically crawls your Data Sources, identifies Data Formats, and infers schemes to create an AWS Glue Data Catalog.

5. **Data Catalog:** AWS Glue Data Catalog is a fully managed MetaData Repository that makes it easy to discover and manage Data in AWS. You can use the Glue Data Catalog with other AWS Services, such as Athena.

6. **AWS Athena:** AWS Athena is an interactive query service that makes it easy to analyse Data in Amazon S3 using standard SQL. You can use Athena to analyse Data inn your Glue Data Catalog or in other S3 Buckets    

## Install Packages
```
pip install pandas
pip install numpy
pip install spotipy
```
## Project Execution Flow
1. Extract Data from API
2. Lambda Trigger (every 1 hour)
3. Run Extract Code
4. Store Raw Data
5. Trigger Transform Function
6. Transform Data and Load it
7. Query using Athena
