
# **Twitter Data Pipeline with Airflow:**

## Overview:

This project demonstrates a simple data pipeline for extracting, transforming, and loading (ETL) Twitter data using Airflow. By leveraging Airflow's capabilities, we automate the process of fetching tweets from the Twitter API, refining them with Python ETL scripts, and storing them in an Amazon S3 bucket.

## Architecture:

<img width="1425" alt="image" src="https://github.com/prashanti-ps/Twitter_Airflow_Data_Pipeline/assets/78148121/56f908b5-bf31-4091-9098-6719f773905d">

## Components:

### 1. Twitter API:
   - Provides access to Twitter's data.
   - Utilized to fetch tweets based on specified criteria (e.g., user, hashtags, keywords).

### 2. Python ETL:
   - Contains scripts responsible for Extracting, Transforming, and Loading Twitter data.
   - Fetches tweets using Tweepy, a Python library for accessing the Twitter API.
   - Refines the fetched data, extracting relevant information and structuring it into a suitable format.
   - Example script provided (`twitter_etl.py`) demonstrates fetching tweets from Elon Musk's timeline.

### 3. Airflow:
   - Apache Airflow orchestrates the entire data pipeline.
   - Allows scheduling and monitoring of workflows.
   - Written as Directed Acyclic Graphs (DAGs), where tasks and dependencies are defined.
   - Example DAG (`twitter_dag.py`) schedules the execution of the Twitter ETL script at specified intervals.
   - Ensures reliability and repeatability of the data pipeline.

### 4. Amazon S3 Bucket:
   - Serves as a storage destination for the refined Twitter data.
   - Provides scalable, durable, and secure object storage.
   - Integrated into the pipeline to store the processed data for further analysis or consumption.



## Setup Instructions:

1. **Twitter API Credentials:**
   - Obtain API keys and access tokens from the Twitter Developer Platform.

2. **Python Environment Setup:**
   - Ensure Python and necessary libraries (e.g., Tweepy, Pandas) are installed.
   - Install Airflow using `pip install apache-airflow`.

3. **Airflow Configuration:**
   - Configure Airflow with appropriate settings, including connection to your database and executor type.

4. **DAG Deployment:**
   - Place the DAG script (`twitter_dag.py`) in the Airflow DAGs directory.
   - Ensure DAG's `start_date` and `schedule_interval` are configured according to your requirements.

5. **Amazon S3 Setup:**
   - Create an S3 bucket on AWS to store the refined Twitter data.
   - Configure permissions and access keys to allow Airflow to interact with the bucket.

6. **Execute the Pipeline:**
   - Start the Airflow webserver and scheduler.
   - Monitor the DAG execution and view logs through the Airflow UI.

## Conclusion:

This project showcases a robust data pipeline architecture for handling Twitter data using Airflow, Python ETL scripts, and Amazon S3. By automating the process, it enables efficient extraction, transformation, and loading of Twitter data, facilitating downstream analytics, insights, and decision-making. Feel free to customize and extend the pipeline to suit your specific use cases and requirements.


