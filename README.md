# Predicting Baseball Salaries

Maura Cerow

[Data Source](https://www.usatoday.com/sports/mlb/salaries/)


## Introduction

For this project, I wanted to predict baseball salaries using player position and team. I scraped the data from USA for the 2019 season.

In the project, I used the following libraries:

    - BeautifulSoup
    - Pandas
    - Numpy
    - Sklearn
    - Matplotlib
    - Seaborn

In this repo you will find the jupyter notebook with the code to scrape the website as well as clean the data, perform EDA and model.

## Data Collection

For this project, I scraped my data from USA today and used BeautifulSoup to parse the html page. From the website, I wanted to get the player name, position, team and 2019 salary. I added each item to the appropriate list and created a dictionary with my individual columns. My last step would be to convert my new dictionary to a dataframe to work with.

## Data Cleaning & EDA
