## Table of Contents
1. [Project Overview](#dataset)
2. [Author(s)](#author)
3. [Dataset Description](#description)
4. [Data Cleaning](#cleaning)
5. [Exploratory Data Analysis](#EDA)

# Project Overview

Airbnb is one of the most popular ways to find a place to stay in most major cities around the world. It has significantly altered the traditional method of locating accommodations for both short and long-term stays. we'd like to focus on the following issues that have been raised:  

• What is the seasonal pattern of Airbnb in Chicago?  
• What kinds of Airbnb homes are popular?  
• What are the most influential features about the rental price?  


This project's results will assist businesses in narrowing their target marketing customer base to the most likely prospective customers, and it will also assist businesses in understanding how various attributes influence the client's decision to accept or reject the Airbnb home.  

# Author(s) 

1. Mysari Srinikethan 
2. Hemanth Pokala 
3. Muhammed Adeem Shaik 


# Dataset description 
Link to our dataset before and after clean - https://drive.google.com/drive/folders/1E6MlV8LWRFfwaXgGZfFbozsyBijNDJ6I?usp=share_link

Airbnb does not release any data on the listings in its marketplace, but a separate group named Inside Airbnb scrapes 
and compiles publicly available information about many cities Airbnb's listings from the Airbnb website. For this project, 
their data set scraped on September 14, 2022, on the city of Chicago, Illinois is used. It contains information on all Chicago 
Airbnb listings that were live on the site on that date (over 7,400). 
The dataset is publicly available and link to the dataset is: http://insideairbnb.com/get-the-data/
The data has certain limitations. Most noticeable one is that it scrapes the advertised price rather than the actual price paid by 
the previous customer. There are also missing values in many fields w hich needed to be cleaned based on their importance.
From the downloaded dataset we would like to use the following csv datasets. 
1) Calender.csv 
- I t contains 10,48,575 row s w ith 7 columns. 
2) Listings.csv 
- I t contains 7,414 row s w ith 75 columns. 
3) Review s.csv 
- I t contains 3,43,394 row s w ith 6 columns. 

Some of the more important features this project will look into the following: accommodates, bedrooms, bathrooms, beds, price, 
minimum_nights, maximum_nights and number_of_reviews.

# Data Cleaning 

Data cleaning is the process of fixing or removing incorrect, corrupted, incorrectly formatted, duplicate, or incomplete data within a dataset. 

-> Dropped the columns which were not informative such as id and name for our price prediction.  
-> Dropped the columns that were informative but difficult to deal with because they required NLP for further analysis.  
-> Only "neighbourhood cleansed" is required as a feature of home location, which allowed us to eliminate other columns that are related to location.  
-> Identified and eliminated all the duplicate columns and rows.  

<img width="535" alt="Screen Shot 2022-11-30 at 4 43 34 PM" src="https://user-images.githubusercontent.com/89613198/204924958-08762063-4031-4b34-87c9-78c6e6e60b9e.png">



<img width="992" alt="Screen Shot 2022-11-30 at 4 50 26 PM" src="https://user-images.githubusercontent.com/89613198/204925092-db0712a4-b64d-43ba-81f9-624097a82b14.png">


## Exploratory Data Analysis

In terms of EDA, we attempted to address our primary goals. 

Below Timeplot depicts the Seasonal pattern of Airbnb in Chicago which shows highest occupancy rate was in September 2022 and the lowest was in December 2022.  
<img width="875" alt="Screen Shot 2022-11-30 at 4 59 55 PM" src="https://user-images.githubusercontent.com/89613198/204926347-db55103a-ee89-41ad-983f-3b8193c01126.png">

Below Timeplot depicts the Seasonal price of Airbnb in Chicago which shows due to the summer, the rental price was less expensive in October 2022 and more expensive from May 2023.  
<img width="893" alt="Screen Shot 2022-11-30 at 5 02 20 PM" src="https://user-images.githubusercontent.com/89613198/204926620-c6fca138-aa49-40a9-8240-7f562c69de5f.png">

We defined popular homes by using a 70% threshold, plotted it with Bar Plot, and visualized it and you can see them below.
<img width="949" alt="Screen Shot 2022-11-30 at 5 06 31 PM" src="https://user-images.githubusercontent.com/89613198/204927156-e77c674d-7997-4176-8c9d-c0132d5f54b5.png">

We learned that the following factors had the greatest impact on the rental price:  
Property type - Entire Rental Unit was preferred more.  
Host response time - Within an hour was preferred more.  
Instant bookable - was preferred more  
<img width="1025" alt="Screen Shot 2022-11-30 at 5 08 14 PM" src="https://user-images.githubusercontent.com/89613198/204927370-3547abf5-9d6e-4053-8ff9-a55c4c44ca2d.png">
## Machine Learning Models

1) Predicting the Rental Prices of Airbnb data in chicago
a) XGBoost
Now that the data preprocessing is over, we can start applying different Supervised Machine Learning models. The evaluation metrics used will be mean squared error and r-squared. Boosting is an ensemble technique where new models are added to correct the errors made by existing models. Models are added sequentially until no further improvements can be made. GBoost (eXtreme Gradient Boosting) is an implementation of gradient boosted decision trees designed for speed and performance. Is a very popular algorithm that has recently been dominating applied machine learning for structured or tabular data.

#### RMSE value – 0.3459

b) Random Forest
A random forest is a supervised machine learning algorithm that is constructed from decision tree algorithms. It’s more accurate than the decision tree algorithm.

c) Catboost
CatBoost is an algorithm for gradient boosting on decision trees.CatBoost supports all kinds of features be it numeric, categorical, 
or text and saves time and effort of preprocessing. And the main reason for using catboost over xgboost is it provides
high ranking benchmark RMSE values compared to xgboost. 

#### RMSE value – 0.2775


d) Linear Regression
Linear regression is a simple Supervised Learning algorithm that is used to predict the value of a dependent variable(y) for a given 
value of the independent variable(x) by effectively modelling a linear relationship. It is a simple implementation and 
performance on linarly seperable datasets is good and overfitting can be reduced by regularization. 
try using Ridge and Lasso Regularization to decrease the influence of less important features. Ridge Regularization is a process which shrinks the regression coefficients of less important features.
We’ll once again instantiate the model. The Ridge and Lasso Regularization model takes a parameter, alpha , which controls the strength of the regularization.
#### RMSE value – 0.3864 

## Conclusion
Conclusion 
We spread the work evenly amongst ourselves in each and every section, such as data cleansing, EDA, and models. If we had more time, we would have come up with some intriguing ideas by evaluating the datasets, categorizing them based on reviews from other datasets and presenting some more specific graphs that would be useful to Airbnb hosts.

