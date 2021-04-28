# Project: Data Modeling with Postgres

## Introduction
A startup called Sparkify wants to analyze the data they've been collecting on songs and user activity on their new music streaming app. The analytics team is particularly interested in understanding what songs users are listening to. Currently, they don't have an easy way to query their data, which resides in a directory of JSON logs on user activity on the app, as well as a directory with JSON metadata on the songs in their app.


## Project Description
In this project, I had to apply what I've learned on data modeling with Postgres and build an ETL pipeline using Python. To complete the project, I needed to define fact and dimension tables for a star schema for a particular analytic focus, and write an ETL pipeline that transfers data from files in two local directories into these tables in Postgres using Python and SQL.


## Schema for Song Play Analysis
Using the song and log datasets, I created a star schema optimized for queries on song play analysis. This includes the following tables.

### Fact Table
**songplays** - records in log data associated with song plays i.e. records with page NextSong
*songplay_id, start_time, user_id, level, song_id, artist_id, session_id, location, user_agent*

### Dimension Tables
**users** - users in the app
*user_id, first_name, last_name, gender, level*

**songs** - songs in music database
*song_id, title, artist_id, year, duration*

**artists** - artists in music database
*artist_id, name, location, latitude, longitude*

**time** - timestamps of records in songplays broken down into specific units
*start_time, hour, day, week, month, year, weekday*

## Project structure
### Files used on the project:

**data** folder nested at the home of the project, where all needed jsons reside.
**sql_queries.py** contains all sql queries.
**create_tables.py** drops and creates tables.
**test.ipynb** displays the first few rows of each table to check your database.
**etl.ipynb** reads and processes a single file from song_data and log_data and loads the data into tables.
**etl.py** reads and processes files from song_data and log_data and loads them into tables.
**README.md** Read me, please.

