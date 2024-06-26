# Spotfiy-End-To-End-Data-Pipeline-

## Project Overview:

This project extracts divers data from the Spotify API,including album,artist,songs from a playlist and stores it in AWS Simple Storage Service(S3) for analysis. The ultimate goal is to establish an automated pipeline hosted on AWS for data extraction and processing.

#### Data Processing pipeline steps:

**1.Data Extraction** : A Python script on AWS Lambda extracts the information in JSON format and uploads it to AWS S3 bucket.This triggered using Amazon CloudWatch on a daily basis.

**2.Data Transformatiom**: A second Lambda function is triggered whenever a new data is created in the S3 bucket.It takes the data from s3bucket and extracts the info for album,artist and songs and then stores in three different CSV files in S3bucket.

**3.Data Loading into Snowflake**: Data is loaded into the snowflake warehouse by creating Storage intigration to the S3 bucket and creating the file format.

**4.Snowpipe**: Snow pipes are designed to automate the data loading process by continuously loading data from external sources into Snowflake tables. by using snowpipe automatically data will be updated in album,artist and songs tables in snowflake.

**Tools used in this project:**

**- Spotify API,**

**- Python,**

**- Amazon CloudWatch,**

**- Amazon Lambda,**

**- Amazon Simple Storage Service(S3),**

**- Snowflake**


![spotify_Snowflake_Project](https://github.com/DeepakRajole/Spotfiy-End-To-End-Data-Pipeline-/assets/169185254/42699155-2f59-47ba-aef7-efbd531d7c24)
