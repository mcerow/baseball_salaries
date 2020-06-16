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

When I began my EDA, my full dataset ranged from $555k to $42.1m -- hello outliers. I decided to use the IQR to remove the outliers from my data in hopes it would provide for a more accurate model. With those observations dropped, my dataset went from 877 observations to 796 observations.

Before I can start running my regression models, I need to create dummy variables for my categories - position & team. I drop the first column to handle multicollinearity.

## Modeling & Evaluation

For this project, I wanted to use Decision Trees, Random Forest & Adaboost to predict salaries. My first model is a simple decision tree. My MSE for this model is 16396140.1. Now I'm a fan of ensemble methods. I like the idea of the 'wisdom of the crowd' to predict my outcome. I used a straightforward Random Forest not tuning any hyperparameters. My MSE improved to 15203172.1. I know the default settings for Random Forest may not be set to best suit my data. I used GridSearch to find the best parameters for my data and rerun my Random Forest with the returned parameters. My MSE dropped to 11012030.3. One last method I want to try is Adaboost where I'm no longer taking independent trees to compile my 'crowd'. Instead, Adaboost works to improve what the previous tree got wrong. Adaboost is iterative. When I ran this model, I got an MSE of 11969117.9.

Based on my MSE, my best model is Random Forest tuned using GridSearch.

## Blog Post
[Show Me the Money](https://medium.com/@mauracerow/show-me-the-money-7241d0881a52)
