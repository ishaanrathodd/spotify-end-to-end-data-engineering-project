# Spotify AWS ETL Project

Hey there! 👋 Welcome to my project. Here's a quick rundown of what I'm up to:

![Architecture Diagram](https://github.com/ishaanrathodd/spotify-end-to-end-data-engineering-project/assets/90642857/d3534425-04e2-4839-9b71-065e73de5f5b)


## Project Overview

In this project, I'm building an ETL (Extract, Transform, Load) pipeline using the Spotify API and AWS (Amazon Web Services), to extract data from Spotify playlist and store it in AWS as a Dataframe where we have different dataframes for albums,songs and artists.

## Project Execution Flow
1. **Extract:** Using Spotify's API, I pull out details about artists, albums, and songs from the Top 50 Global playlist URL, using the lambda function spotify_api_data_extract.py

2. **Transform:** I convert the raw data into a neat and organized structure, and place the structured data into different sub-folders like album_data, song_data and artist_data.

3. **Load:** I use AWS tools to smoothly move and store my organized data, and apply queries in Athena to get the information I want.
   
This process of extracting data from the playlists is automated using CloudWatch, which is then stored in Amazon S3. Then I use a trigger to run the spotify_transformation_load_function.py function whenever a file is added to S3 through CloudWatch.

## About Dataset/API
This API contains information about music artist, albums and songs - [Spotify API](https://developer.spotify.com/documentation/)

## Services Used
1. **S3 (Simple Storage Service):** Amazon S3 (Simple Storage Service) is a highly scalable object storage service that can store and retrieve any amount of data from anywhere on the web. It is commonly used to store and distribute large media files, data backups, and static website files.
   
2. **AWS Lambda:** AWS Lambda is a serverless computing service that lets you run your code without managing servers. You can use Lambda to run code in response to events like changes in S3, DynamoDB, or other AWS services.

3. **Cloud Watch:** Amazon Cloudwatch is a monitoring service for AWS resources and the applications you run on them. You can use CloudWatch to collect and track metrics, collect and monitor log files, and set alarms.

4. **Glue Crawler:** AWS Glue Crawler is a fully managed service that automatically crawls your data sources, identifies data formats, and infers schemas to create an AWS Glue Data Catalog.

5. **Data Catalog:** AWS Glue Data Catalog is a fully managed metadata repository that makes it easy to discover and manage data in AWS. You can use the Glue Data Catalog with other AWS services, such as Athena.

6. **Amazon Athena:** Amazon Athena is an interactive query service that makes it easy to analyze data in Amazon S3 using standard SQL. You can use Athena to analyze data in your Glue Data Catalog or in other S3 buckets.

## Install Packages
```
pip install pandas
pip install numpy
pip install spotipy
```
