# Movies-ETL

# Project Overview

This project is to perform an Extract, Transform, Load (ETL) process to create data pipelines using Python, Pandas and PostgreSQL from 3 very large data files.

# Resources

-Data: wikipedia-movies.json, movies_metadata.csv, ratings.csv

-Software: Python, Jupter Notebook, PostgreSQL

# Process

1. Extract: Read json and csv files by using Pandas and do a cleaning movie process to drop all the duplicates columns. Then create a extract_transform_load() function

2. Transform: 
   - Clean wikipedia movie data by using regular expressions to parse and transform the data into a consistent format, and then drop the redundant columns
   - Clean Kaggle movie data by droping all the 'adult' columns and change the data types of the 'budget', 'id', 'polularity' and 'release_date' into the right types
   - Merge wiki movie and kaggle movie into movie dataframe
   - Clean the rating data 
   - Merge the movie dataframe and rating data into the final dataset
   
3. Load: Export transformed data into a database.

# Summary

After loading all the data into postgreSQL, we can see that there were a movies table created with 6,052 rows. and a ratings table created with 26,024,289 rows.
![movies_query](https://github.com/ivorfanning/Movies-ETL/blob/main/Resources/movies_query.png)
![rating_query](https://github.com/ivorfanning/Movies-ETL/blob/main/Resources/ratings_query.png)
