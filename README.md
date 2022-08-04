# Challenge 8: Extract, Transform, Load

## Challenge Overview

- This challenge synthesizes the work done in the module into two functions. 
- These changes allow for a more efficient runtime and open the possibility to have the Extract, Transform, Load (ETL) process automated for future use. 
- The challenge gives a basic look at how to operationalize the ETL workflow.

## Function Overview

- The functions in this challenge accomplish the following tasks:
    1. Creates a function called `clean_movie` that cleans the data by removing alternate column titles and giving the columns more appropriate names. 
    2. Creates a function called `extract_transform_load` that does the following
        - reads the data files in to Pandas DataFrames
        - runs the `clean_movies` function. 
        - uses regular expressions to extract IMDb ID's and drop duplicates
        - uses list comprehension to clean the `box_office`, `budget`, and `release_date` columns of the movie data pulled from Wikipedia.
        - cleans the data pulled from Kaggle.
        - merges the Kaggle and Wikipedia DataFrames
        - cleans the ratings data and merges into complete DataFrame.
        - uses SQLAlchemy to connect to SQL database, create database tables, and record the amount of time passed. 

## Summary

- After using jupyter notebook to prototype cleaning the data, moving that functional code into a single function allows for better performance and automated data extraction, transformation, and loading in the future. 

- One way to consider refactoring this code would be to incoporate input statements that would then supply the arguments to run the function. 
    - This step could remove the need to use jupyter notebook to clean and run the data.