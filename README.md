# Spotify End-To-End Data Engineering Project

### Introduction 
In this project, we aim to create an ETL (Extract, Transform, Load) pipeline using Spotify API on the AWS cloud platform. The pipeline's primary purpose is to retrieve data from the Spotify API, transform this data into a desired format, and Load it into an AWS data repository.

### Architecture
![Architecture Diagram](https://github.com/GauravJagtap-git/Spotify-end-to-end-data-engineering-project/blob/main/spotify%20etl%20pipline%20framework.jfif)

### About Dataset/API
This API contains information about the Top 50 global music artists, albums, and songs.
[Spotify API](https://developer.spotify.com/documentation/web-api)

### Services Used
1. **S3 (Simple Storage Service):** Amazon S3 (Simple Storage Service) is a highly scalable object storage service that can store and retrieve any amount of data anywhere on the web. it is commonly used to store and distribute large media files, data backups, and static website files.
   
2. **AWS Lambda:** Lambda is a computing service that allows programmers to run code without creating or managing servers

3. **Cloud Watch:** Amazon CloudWatch is a monitoring service for AWS resources and the applications you run on them. You can use CloudWatch to collect and track metrics, and monitor log files, and set alarms.

4. **GlueCrwaler:** AWS Glue crawler is a fully managed service that automatically crawls your data sources, identifies data formats, and infers schema to create an AWS Glue Data Catalog.

5. **Data Catalog:** AWS Glue Catalog  is a fully managed metadata repository that makes it easy to discover and manage data in AWS. you can use the Glue Data Catalog with other Aws services,such as Athena.

6. **Amazon Athena:** Amazon Athena is an interactive query service that makes it easy to analyze data in Amazon S3. You can use Athena data in your glue data catalog or another S3 bucket.

### Install Packages
```
pip install Pandas 
pip install numpy 
pip install spotipy
```
### Project Execution Flow
Extract data from API --> lambda Trigger (every 1 hr) --> Run Extract Code --> Store Raw Data --> Trigger Transform Function --> Transform Data and Load it --> Query Using Athena
