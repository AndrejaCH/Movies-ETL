# Movies ETL
*An ETL Movies Analysis*

## Project Overview

### Background
Raw data exists in multiple places and forms. In order to perform any kind of data analysis, this data needs to be cleaned and structured. Data pipeline process **ETL – Extract, Transform, and Load** is a core concept in data engineering, ensuring that data is consistent, maintains its integrity, and nontheless strives for automatization of data wrangling. Without a consistent and robust data structure, it’s nearly impossible to perform any meaningful analysis. 


### Purpose
The Amazing Prime, a video streaming company, decided to sponsor a *hackathon*, where participant trying to predict which low budget movies being released will become popular. Participants of a hackathon need a clean data in order to perform analyses for their algorithms. In order to provide organized and clean dataset this project focuses on *ETL** or **Extract, Transform and Load** process and includes the following:

-	**Extracting** data from two different sources 

    - a web scrape of Wikipedia website for all movies released since 1990, and
    - data from Kaggle website for rating data.
-	**Transforming** data using Jupyter Notebook, Python, Pandas and Python RegEx module.
-	**Loading** data using PostgreSQL and pgAdmin to host final cleaned data set.

The goal of this analysis is to create automated pipeline that extracts, transform and loads data. This analysis consists of four parts, where each step is building up from beginning of extracting data and function testing, through transformation and cleaning process to its final step connect and load to the database.  The entire process of ETL is can be executed with a single call of the function ***extract_transform_load***. The ETL procedure is broken down into four jupyter notebook the files:

1.	[ETL_function_test.ipynb](ETL_function_test.ipynb)
    - Data is extracted from the website in JSON and CSV formats.
    - Data is transformed into Pandas data frames.
    - JSON file require extra step – loading file first and then transforming into data frame.

2.	[ETL_clean_wiki_movies.ipynb](ETL_clean_wiki_movies.ipynb)
    - Function *clean_movie* combines scattered data of alternative languages into one column *alt_titles*. 
    - Its subfunction *change_column_name* organizes column names into consistent pattern.
    - In the function *extract_transform_load* the transformation process of wiki movies data begins and includes:
 
         - Python **list comprehensions**.
         - apply() and map() methods in combination with **lambda functions**.    
         - regular expresions or **RegEx**.
        
3.	[ETL_clean_kaggle_data.ipynb](ETL_clean_kaggle_data.ipynb)
    - Function *extract_transform_load* gets new tasks for cleaning Kaggle data and includes:
    
        - Changing datatypes, using methods pd.to_numeric, astype() and python comparison operators for Boolean types.
        - Filling missing values and filtering unwanted columns.
        - Merging data frames using *pd_merge* method.
        
4.	[ETL_create_database.ipynb](ETL_create_database.ipynb)
    - Finally, the function in its final step connect to the data base by **sqlalchemy** library and **to_sql** method. 
    - Complete ETL process can be executed with a single function *extract_transform_load* call.


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

