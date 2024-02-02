# Spotify AWS ETL Project

Hey there! 👋 Welcome to my project. Here's a quick rundown of what I'm up to:

## Project Overview

In this project, I'm building an ETL (Extract, Transform, Load) pipeline using the Spotify API and AWS (Amazon Web Services), to extract data from Spotify playlist and store it in AWS as a Dataframe where we have different dataframes for albums,songs and artists.

## Steps in the Journey

1. **Extract:** Using Spotify's API, I pull out details about artists, albums, and songs from the Top 50 Global playlist URL, using the lambda function spotify_api_data_extract.py

2. **Transform:** I convert the raw data into a neat and organized structure, and place the structured data into different sub-folders like album_data, song_data and artist_data.

3. **Load:** I use AWS tools to smoothly move and store my organized data, and apply queries in Athena to get the information I want.
   

This process of extracting data from the playlistis is automated using CloudWatch, which is stored in Amazon S3. Then I use a trigger to run the spotify_transformation_load_function.py function whenever a file is added to S3 through CloudWatch.
