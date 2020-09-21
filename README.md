# Movies-ETL Analysis

## Overview of the Movies ETL analysis

The purpose of this project is:
	• To create an automated pipeline that will read and extract new data,
	• To perform the appropriate transformations on the newly read data; and
	• To load the transformed data into existing PostgreSQL database.
	
## Results

These are the observations from the Movies ETL analysis :
### 1) Extract
* Wikipedia data(wikipedia-movies.json), Kaggle metadata(movies_metadata.csv) and MovieLens ratings data(ratings.csv) are read.
* Three DataFrames create three separate DataFrame : wiki_movies_df, kaggle_metadata and ratings.

## 2) Transform
* wiki_movies_df is cleaned for duplicates entries which have similar data, converted to uniform format across the rows and columns will null values are removed.
* kaggle_metadata is cleaned for converted to uniform format across the rows and columns with null values are removed.
* ratings is cleaned up for uniform format across the column.
* wiki_movies_df and kaggle_metadata is inner merged on imdb_id to create movies_df
* the common columns and analyzed and duplicates are removed.
* movies_df and ratimgs are merged on kaggle_id.

## 3) Load
* Database engine is created and the transformed movies_df and ratings.cvs are loaded into the PostgreSQL database.

## Summary

