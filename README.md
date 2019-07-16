# Data Modeling with Postgres Project

## Purpose of the project
The purpose of this project is to create a database that simplifies the querying of data on songs and user activity for the analytics team.

## Database Schema Design
The database schema used for this project is the star schema. It consists of one Fact table (song_play) and four Dimension Tables (users, songs artists and time). This schema design helps with simplifying complex queries and allows for greater performance when reading data from the database.

## File Structure
The files in the repository are as follows:
### sql_queries.py
This contains the queries that drops the tables if they exist, creates the tables, inserts extracted data from the datasets to the tables and a select query that gets the songid and artistid.

### create_tables.py
This file contains the methods that execute the drop and create table queries found in the sql_queries file .

### etl.py
Extracts data from the data files and inserts them in the database tables.

## Running Scripts
### Requirements
    Python 3
    Postgresql
    
To drop or create the tables, ensure you are in the project's directory then run the following command:
    
    python create_tables.py
    
To run the ETL pipeline that will extract data from the datasets and store them in the tables simply run:
    
    python etl.py
