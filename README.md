# Data-modeling-with-Apache-Cassandra
## Sparkify ETL 
In this project, the following concepts have been used.
  1. Design NoSQL Database - Apache Cassandra
  2. Develop ETL Pipeline - Python, Pandas

### Project Introduction:
A startup called Sparkify wants to analyze the data they've been collecting on songs and user activity on their new music streaming app. The analysis team is particularly interested in understanding what songs users are listening to. Currently, there is no easy way to query the data to generate the results, since the data reside in a directory of CSV files on user activity on the app.

### Objective:
As a data engineer, I have to create an Apache Cassandra database which can create queries on song play data to answer the questions. My role is to create a database for this analysis & test database by running queries.

### ETL Process:
**Song Play Dataset**

For this project, I will be working with one dataset: **event_data.** The directory of CSV files partitioned by date. Here are examples of filepaths to two files in the dataset:

  >event_data/2018-11-08-events.csv

  >event_data/2018-11-09-events.csv

**Quries to be performed**

  1. Give me the artist, song title and song's length in the music app history that was heard during sessionId = 338, and itemInSession = 4

  2. Give me only the following: name of artist, song (sorted by itemInSession) and user (first and last name) for userid = 10, sessionid = 182

  3. Give me every user name (first and last) in my music app history who listened to the song 'All Hands Against His Own'

### Project structure:
**Files used in the project:**

  -**event_data** The data are stored as a collection of csv files partitioned by date.
  
  -**event_datafile_new.csv** ETL copies data from the date-partitioned csv files to a single csv file *event_datafile_new.csv* which is used to populate the denormalized Cassandra tables optimised for the 3 queries above.
  
  -**Project_1B_Project_Template.ipynb** The ETL pipeline and data modeling are written in a single jupyter notebook.
  
