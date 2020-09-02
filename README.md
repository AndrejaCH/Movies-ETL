# Movies ETL
*An ETL Movies Analysis*

## Project Overview

### Purpose
The Amazing Prime, a video streaming company, decided to sponsor a *hackathon*, where participant trying to predict which low budget movies being released will become popular. Participants of a hackathon need a clean data in order to perform analyses for their algorithms. In order to provide organized and clean dataset this project focuses on *ETL** or **Extract, Transform and Load** process and includes the following:

-	**Extracting** data from two different sources, 

    - a web scrape of Wikipedia website for all movies released since 1990, and
    - data from Kaggle website for rating data.
-	**Transforming** data using Jupyter Notebook, Python, Pandas and Python RegEx module.
-	**Loading** data using PostgreSQL and pgAdmin to host final cleaned data set.

### Background
Raw data exists in multiple places and in order to perform any kind of data analysis, this data needs to be cleaned and structured. Data pipeline process ETL – Extract, Transform, and Load is a core concept in data engineering ensuring that data is consistent and maintains its integrity, and strives to automatization of data wrangling. Without a consistent and robust data structure, it’s nearly impossible to perform any meaningful analysis. 

## Resources

Data Sources: 

-	Wikipedia web scrape [JSON file](Resources/wikipedia-movies.json)
-	Kaggle data from [Kaggle.com](https://www.kaggle.com/rounakbanik/the-movies-dataset) - two files: movies_metadata.csv and ratings.csv

Enviroment:
-	Python 3.7

Dependencies:
-	Please see Jupyter Notebook [ETL_create_database.ipynb](ETL_create_database.ipynb) for complete list of dependencies

Software:
-	Jupyter Notebook
-	PostgreSQL and PgAdmin

