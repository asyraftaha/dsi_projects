# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 2 - Ames Housing Data and Kaggle Challenge

## Table of Contents

I have spread the tasks of the projects into 3 jupyter notebooks, numbered in order. 

**1. Train & Test Data Cleaning**
- Train DataFrame Cleaning
- Test DataFrame Cleaning

**2. Kaggle Submission**
- Exploratory Data Analysis
    - Train Data
    - Test Data
- Data Modelling
- Kaggle Submission

**3. Business Problem Analysis**
- [Problem Statement](#Problem-Statement)
- Exploratory Data Analysis & Feature Engineering
- Data Modelling & Prediction
    - Linear Model
    - Lasso Model
    - Ridge Model
- [Conclusion](#Conclusion)
    - [Findings](#Findings)
    - [Limitations](#Limitations)
    - [Further Exploration](#Further-Exploration)


## Problem Statement
In this project, we were tasked to solve a business problem using the Ames Housing Data. This will be a independent analysis from the Kaggle Submission in Part 2.

**Through notebook 3, I will explore how individuals can look to increase their prices of their houses by improving their houses.** 

Understanding that building a completely new house on the existing land is not cost effective and would require a large sum of money to invest in, I will zoom in to features or variables that a homeowner is able to manipulate or influence (i.e. via renovation or home improvement, etc) and would require a relatively lower budget (as compared to changing the structural integrity of the house) and ultimately how it can help predict the price for future sales. 


## Datasets

For this project, I will be using the Ames Housing Dataset.

To read further on the discription of the data as well as the data dictionary, [click here](http://jse.amstat.org/v19n3/decock/DataDocumentation.txt).


## Modelling Method

For this project, I am using the Linear, Lasso and Ridge Regression and comparing the 3 models to see which performs better for our analysis. 


## Conclusion


### Findings

- There were a large number of null values in the dataset. Instead of dropping them, we filled them methodically, always having a logical reason behind why we are filling a certain value in.

- From our data exploration and various modelling using lasso regression, we learnt that certain features such as (BsmtFin Type_SF1, Exter Qual and Kitchen Qual) were important to increase price of a home. Having such knowledge may help an owner to decide on what are the more important areas to improve on when trying to raise the value for future sales.

- Regularisation of data helps to improve prediction for the model.

- We also saw that there was a strong multicollinearity between features. Systematically creating interaction terms and combining features have helped to deal with these multicollinearity. Although there were other highly correlated features still present, we did not combine them as there was no logical way to do so.

- Ridge and Lasso models were the best performing models.

### Limitations

- We have dropped features with a large value of null data that could not be logically filled. That may have affected our model.
- Strong multicollinearity between the feautures of the dataset may still exist, albeit us mitigating them and could still affect our model.


### Further Exploration

- We have only worked with Linear, Lasso and Ridge models in this project. There may exist other models that could be a better fit that were not explored.
- Further feature engineering could also be done as we discover more on the relationships between features that may produce a better output for our model.
- Further comparative study on the prices of the works that could be done to the house would allow us to understand the cost and benefit of the changes with respect to the Sale Price of the house.
