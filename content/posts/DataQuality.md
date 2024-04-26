---
title: "Data Quality CSV"
date: "2024-04-26" 
tags:
  - "gis"
  - "snowflake"
  - "csv"
  - "INFER_SCHEMA"
  - "load csv"
  - "data ingestion"
  - "aws"
  - "s3" 
---

I have been working on automated data ingestion activity on snowflake.  The python code uses Snowflake INFER_SCHEMA with Evolution Changes to load the data. [data-load with schema evolution](https://docs.snowflake.com/en/user-guide/data-load-schema-evolution#examples)

The system is set up to automatically figure out the file metadata schema from a group of staged data files that contain semi-structured data, and then get the column definitions. The GENERATE_COLUMN_DESCRIPTION function uses the result of the INFER_SCHEMA function to make it easier to create new tables, external tables, or views (using the right CREATE <object> command) based on the column definitions of the staged files.

The process of loading data is done from an AWS S3 bucket, which contains many CSV files. Sometimes, the data load runs into problems because of issues with the CSV files. For example, some columns might be empty. To make sure the data is good, given that there are more than 300+ files in S3, a Python script is used. This script connects to S3 and uses pandas to find out which columns are empty.

The code spits out the CSV file name and empty columns if present in CSV (else []). The quick audit helps to understand input source and take corrective measures easily.


```python
import boto3
import pandas as pd


session = boto3.Session(profile_name="<your aws profile name>")  # ensure you logged into AWS and have active session
s3 = session.client('s3')
bucket_name = '<your own bucket>' # your S3 bucket name 
prefix = 'folder1/uat/data/source'
response = s3.list_objects(Bucket=bucket_name, Prefix=prefix)

#Read each file in the folder
for file in response['Contents']:
    file_name = file['Key']
    file_object = s3.get_object(Bucket=bucket_name, Key=file_name)
    df = pd.read_csv(file_object['Body'])  
    empty_columns = df.columns[df.isna().all()].tolist()
    print(file_name)
    print(empty_columns)
```