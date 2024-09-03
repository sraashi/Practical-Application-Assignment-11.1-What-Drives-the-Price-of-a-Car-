# Practical-Application-Assignment-11.1-What-Drives-the-Price-of-a-Car-
Building a model on used cars dataset to predict the variables that affect price of the car using the CRISP-DM approach

Link to main Jupyter notebook: https://github.com/sraashi/Practical-Application-Assignment-11.1-What-Drives-the-Price-of-a-Car-/tree/main


Steps:
1. Business understanding: Objective here is to try out different models and arrive at the best one to predict the price of used cars
2. Data understanding: Explore data, describing the data. Here, it seemed that dropping all the null rows would result in a smaller dataset of a little over 33000 data rows. Instead, deleting one of the columns that had the largest number of null values ('size') allowed for over 100000 data rows to be maintained in the final model. This was an important distinction in understanding the data and deciding how to prepare it for modeling. This also includes visualizing data to understand how many unique values are in each column and how the data is distributed within each column
3. Data preparation: Drop any null cells, drop any columns that are unique to each index, merge and reformat data as needed. 
4. Data modeling: Split the data into train-test sets and build and evaluate different models
5. Data evaluation and deployment:
With the linear regression model, the Test MSE was high. The model score was 0.45, with year, odometer being less important than transmission and drive of the car
With linear regression with polynomial features, the model score was higher, 0.65 with the condition of the car being new, fuel type diesel and drive as rwd being most important for the price
With Ridge regression using GridsearchCV, the R2 score was lower - 0.45



Findings:
This is a second jupyter notebook with a differing data preparation/exploration method. 
The first one is an analysis done with selectively dropping null value columns, another is with all null values dropped over the entire dataset which results in a smaller dataset to start with and yields different results. Thus, data exploration is key to this analysis as well. 

While this is not an extensive analysis, it indicates that the condition of the car being new or like new, the transmission type and the fuel type have a big impact on the price of the car. Some other factors like color, state possibly could have an effect and they could be further evaluated. 
Dealerships should pay attention to these features while determining price of car. 


Report: 

Aim: 
The objective was to identify key factors that affect the price of used cars. The process was to build data using a dataset and help identify the main factors that affect price to the dealership

Methodology: 
I started with exploring the dataset for distribution of null values. It seems that removing all the null values would have resulted in fewer rows (34868 rows) than removing the column that had the most % of null values ('size') and then removing any rows that had null values (resulting in over 100000 rows). I also removed any columns with unique identifiers for each car. This analysis indicates that data exploration and prep is a key step in modeling as well. 

After getting the dataset to train/test, built different models (linear regression with polynomial features, ridge regression with Gridsearch) to evalute the model with the highest R2 score and coefficients that most impacted the price prediction. 

Findings and recommendations: 
It seems that the condition of the car (new or like new), fuel and transmission most importantly affected the price of the car. 





