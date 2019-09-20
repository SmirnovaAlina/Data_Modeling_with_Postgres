## Data Modeling with PostgreSQL 

### Introduction

Famous music company wants to analyze the data they've been collecting on songs and user activity on their new music streaming app. Main goal of the project is processing data sets from JSON format and write them to the DB, for that purpose we need create a Postgres database with tables designed to optimize queries, build ETL pipelines for song play analysis.

### Description 

For modeling data with Postgres DB and building ETL we use Python. Frist of all, we need to define fact and dimention tables. Second, write an ETL pipeline that transfers data from files in two local 
directories into these tables in Postgres using Python and SQL.

### Goal 

Create a Postgres database and ETL pipeline to optimize queries to help Sparkify's analytics team.

### DB Schema

Star schema:

* one fact table: songplays, and
* four dimension tables: users, songs, artists and time

![data base](/images/Image.png =100x20)


### Data Processing 
 
 1. Execute "create_tables.py". create connection with DB  and fresh instance of the sparkifydb with empty tables.
 2. Execute "etl.py". Processing data and write to the DB
 
 
### Test Result 

''' python 
%load_ext sql

%sql postgresql://student:student@127.0.0.1/sparkifydb

%%sql

SELECT COUNT(*) from songplays; 

'''