# Auto MPG Fuel Efficiency Analysis

This project explores the relationship between vehicle characteristics and fuel efficiency using the **Auto MPG dataset**. The goal is to analyze how different features such as weight, horsepower, and engine displacement influence miles per gallon (MPG), and to build regression models that can predict fuel efficiency.

## Project Overview

Fuel efficiency is an important factor in both automotive design and consumer decision making. In this project, the historical **Auto MPG dataset** is used to analyze patterns between car specifications and fuel consumption.

The project includes:

- Data cleaning and preprocessing
- Exploratory data analysis (EDA)
- Visualization of key relationships
- Simple linear regression modeling
- Multiple linear regression modeling
- Model evaluation using R² and RMSE

The objective is to understand which vehicle attributes most strongly affect MPG and evaluate how prediction performance improves when additional variables are included.

## Dataset Information

Source:  
UCI Machine Learning Repository  
https://archive.ics.uci.edu/dataset/9/auto+mpg

Originally collected from the **StatLib library at Carnegie Mellon University** and used in the **1983 American Statistical Association Exposition**.

Dataset characteristics:

- **Number of instances:** 398 cars  
- **Number of attributes:** 9 (including target variable)

### Attributes

| Attribute | Type | Description |
|---|---|---|
| mpg | Continuous | Miles per gallon (target variable) |
| cylinders | Discrete | Number of engine cylinders |
| displacement | Continuous | Engine displacement |
| horsepower | Continuous | Engine horsepower |
| weight | Continuous | Vehicle weight |
| acceleration | Continuous | Time to accelerate |
| model_year | Discrete | Model year |
| origin | Discrete | Country of origin (1 = USA, 2 = Europe, 3 = Japan) |
| car_name | String | Unique car name |

### Missing Values

The **horsepower column contains 6 missing values** which are represented as `"?"`.  
These values are replaced with the **median horsepower value** during preprocessing. :contentReference[oaicite:0]{index=0}

## Data Cleaning

Data preprocessing steps include:

- Replacing `"?"` values with NaN
- Converting horsepower to numeric format
- Filling missing values using the median
- Dropping the `car_name` column since it is not useful for regression

## Exploratory Data Analysis

Several visualizations are used to understand the dataset:

- **MPG Distribution Histogram**  
  Shows the spread of fuel efficiency values.

- **Correlation Heatmap**  
  Identifies relationships between variables such as weight, horsepower, displacement, and MPG.

- **Scatterplot (Weight vs MPG)**  
  Visualizes the negative relationship between vehicle weight and fuel efficiency.

## Modeling

### Simple Linear Regression

A basic regression model is built using **weight as the only predictor** for MPG.

Metrics evaluated:

- R² score
- RMSE
- slope and intercept of the regression line

### Multiple Linear Regression

A second model is built using **all numeric features** as predictors:

- cylinders
- displacement
- horsepower
- weight
- acceleration
- model year
- origin

This model provides a more complete understanding of how multiple variables interact to influence fuel efficiency.

## Model Evaluation

Two metrics are used to evaluate model performance:

**R² (Coefficient of Determination)**  
Measures how well the model explains variance in MPG.

**RMSE (Root Mean Squared Error)**  
Measures prediction error magnitude.

Results showed that the **multiple regression model performed significantly better** than the simple regression model.

## Key Insights

Some important observations from the analysis include:

- Heavier cars tend to have **lower MPG**
- Higher horsepower and displacement often correlate with **lower fuel efficiency**
- Newer model years generally show **better fuel economy**
- Cars from different regions show noticeable differences in MPG

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn

## Learning Outcome

Through this project I practiced:

- Data cleaning and preprocessing
- Exploratory data analysis
- Regression modeling
- Model evaluation and interpretation

This project demonstrates how regression techniques can be used to extract insights from real world datasets and understand relationships between variables.

## Author

Jeongwoo Kim  
Arizona State University  
Data Science
