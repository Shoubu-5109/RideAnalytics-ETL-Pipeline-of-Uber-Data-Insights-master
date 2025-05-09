# RideAnalytics ETL Pipeline of Uber Data Insights

## Overview

RideAnalytics is an ETL (Extract, Transform, Load) pipeline designed to process and analyze Uber ride data, providing valuable insights into various aspects of the uber data. This project aims to demonstrate the power of data engineering and analytics in the transportation domain.

The pipeline extracts raw ride data, transforms it into a structured format, and loads it into a data store where it can be easily analyzed and visualized.

## Table of Contents
1. [Features](#features)
2. [Architecture](#architecture)
3. [Technology Used](#technology-used)
4. [Installation](#installation)
5. [Data Model](#data-model)
5. [Uber Dashboard](#uber-dashboard)
5. [Data Pipeline and Dashboard Setup Guide](#data-pipeline-and-dashboard-setup-guide)

## Features

- Data Extraction: Utilizes the Uber API to fetch ride data.
- Data Transformation: Cleans, aggregates, and enriches the raw data for analysis.
- Data Loading: Stores the processed data in a database or data warehouse.
- Insights Generation: Provides a set of predefined queries or scripts to extract valuable insights.
- Visualization: Creates visual representations of the data for better understanding.

## Architecture

![Architecture](https://github.com/SahilChowkekar/RideAnalytics-ETL-Pipeline-for-Uber-Data-Insights/blob/master/images/diagram.jpeg)

## Technology Used
- Programming Language - Python
- Google Cloud Platform
   - Google Storage
   - Compute Instance 
   - BigQuery
   - Looker Studio

Modern Data Pipeine Tool - https://www.mage.ai/

Contibute to this open source project - https://github.com/mage-ai/mage-ai

## Installation

1. Clone the repository:
    ```bash
   git clone https://github.com/yourusername/RideAnalytics-ETL-Pipeline-for-Uber-Data-Insights.git
2. Navigate to the project directory:
   ```bash
   cd RideAnalytics-ETL-Pipeline-for-Uber-Data-Insights
   ```




## Data Model

![Data model](https://github.com/SahilChowkekar/RideAnalytics-ETL-Pipeline-for-Uber-Data-Insights/blob/master/images/data_model.png)

## Uber Dashboard

- [Dashboard](https://lookerstudio.google.com/reporting/59221cae-d9ef-485b-bc7d-d001b903a0fe)



# Data Pipeline and Dashboard Setup Guide



This guide will walk you through setting up a data pipeline and creating a dashboard using various tools, including Google Cloud Platform, Mage AI, BigQuery, and Lookerstudio.




## Google Cloud Platform Setup
1. Create a new project and give it a name.

2. **Cloud Storage Setup:**
   - Create a bucket.
   - Upload the `uber_data.csv` file. Ensure you make the data public by granting edit access.

3. **Compute Engine Setup:**
   - Create an instance.
   - Connect to the instance using SSH.

4. **Install Necessary Packages and Libraries:**
   ```bash
   sudo apt-get update
   sudo apt-get install python3-distutils python3-apt wget
   wget https://bootstrap.pypa.io/get-pip.py
   sudo python3 get-pip.py
   sudo pip3 install pandas google-cloud google-cloud-bigquery mage-ai
5. **Create a Mage AI Project:**
    ```bash
    mage start demo_project
    ```
    Note down the external IP address and port for later use.

5. **Configure firewall rule to access Mage AI:**
    - Go to Firewall settings and create a new rule.
    - Set source IPv4 range to your IP address or 0.0.0.0/0.
    - Select TCP port and specify the port number used by Mage AI.


## Setting Up Mage AI

1. Create a pipeline in Mage AI to organize your data processing tasks.

2. Run `data_loader.py` and input the URL of the uploaded dataset in Cloud Storage.

3. Run `transformer.py` to perform necessary data transformations.

4. Configure the `io_config.yaml` file for `data_exporter.py` as follows:
   - Provide Google service account key details (obtainable from Google Cloud Console).
   - Configure the dataset and table ID in BigQuery.

## BigQuery Data Analysis

1. Access Google BigQuery and enter the SQL query provided in the [BigQuery file](https://github.com/SahilChowkekar/RideAnalytics-ETL-Pipeline-of-Uber-Data-Insights/blob/master/BigQuery/uber-query.sql).

2. Replace `'gothic-sled-395917.uber_data_engineering_yt.tbl_analytics'` with your project name and dataset name in the SQL query.

## Creating a Lookerstudio Dashboard

1. Navigate to Lookerstudio to begin creating your dashboard.

2. Create a new blank report and select BigQuery as the data source.

3. Utilize Lookerstudio's visualization tools to design and create a personalized Uber dashboard.





