# YouTube Data Harvesting and Warehousing

## Introduction
YouTube, the online video-sharing platform, has revolutionized the way we consume and interact with media. This project focuses on extracting data from specific YouTube channels, processing and storing it in a MongoDB database, and optionally migrating it to MySQL for further analysis. The extracted data can then be analyzed and queried to provide insights based on user-defined questions.

## Developer Guide

### Tools
- Virtual code
- Jupyter notebook
- Python 3.11.0 or higher
- MySQL
- MongoDB
- YouTube API key

### Required Libraries to Install
pip install google-api-python-client pymongo mysql-connector-python sqlalchemy pymysql pandas numpy plotly-express streamlit
YouTube API libraries
import googleapiclient.discovery
from googleapiclient.discovery import build

File handling libraries
import json
import re

MongoDB
import pymongo

SQL libraries
import mysql.connector
import sqlalchemy
from sqlalchemy import create_engine
import pymysql

Pandas, NumPy
import pandas as pd
import numpy as np

Dashboard libraries
import streamlit as st
import plotly.express as px


### ETL Process

1. Extract data
   - Extract the particular YouTube channel data using the YouTube channel ID and the YouTube API.
2. Process and Transform the data
   - Take the required details from the extracted data and transform it into JSON format.
3. Load data
   - Store the JSON format data in a MongoDB database. Optionally, migrate the data to a MySQL database from MongoDB.

### EDA Process and Framework

1. Access MySQL DB
   - Create a connection to the MySQL server and access the specified MySQL database using the pymysql library.
2. Filter the data
   - Filter and process the collected data from the tables based on given requirements using SQL queries. Transform the processed data into a DataFrame format.
3. Visualization
   - Create a Dashboard using Streamlit. Provide dropdown options for the user to select a question to analyze the data. Display the output in DataFrame tables and bar charts.

## User Guide

### Step 1: Data collection zone
- Enter the YouTube channel ID in the input box and click the "Get data and store" button to extract and store the data.

### Step 2: Data Migrate zone
- Select the channel name from the list and click the "Migrate to MySQL" button to migrate the specific channel data from MongoDB to MySQL.

### Step 3: Channel Data Analysis zone
- Select a question from the dropdown menu to analyze the data.
- The results can be displayed in either DataFrame format or bar chart format.


