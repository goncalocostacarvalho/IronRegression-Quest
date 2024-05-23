# IronRegression-Quest

![](https://github.com/goncalocostacarvalho/IronRegression-Quest/blob/main/IronRegression-Quest.png)

# Project Overview 💻

## Context <br /> 
In this project, it’s provided a dataset (CSV file) of house sale prices for King County, including Seattle, over an one year period from May 2014 to May 2015. <br /> Link to dataset: https://www.kaggle.com/datasets/minasameh55/king-country-houses-aa

## Main Task <br /> 
Develop a machine learning model to predict the house sale prices

## Approach <br /> 
Doing several notebooks with slightly differences between them and checking the results <br /> I will only present the final results on this README file and upload the last notebook

# Exploring the data 🔍

| Function | Output |
| :---: | :---: |
| .shape | 21613 rows and 21 columns |
| .dtypes | 1 categorical column (date), 20 numerical columns (5 as float) |
| .isnull().sum() | 0 null values |
| .eq(" ").sum() | 0 empty values |
| .multiplicated().sum() | 0 multiplicate values |

# EDA 📊

- Part of the EDA was to analyze all the distributions for every column
- After analysis, I decided to transform only the columns, "waterfront", "view" and "yr_renovated" and treated them as boolean: <br /> 

 ![](https://github.com/goncalocostacarvalho/IronRegression-Quest/blob/main/IronRegression-Quest-Waterfront.png)
   ![](https://github.com/goncalocostacarvalho/IronRegression-Quest/blob/main/IronRegression-Quest-View.png)
   ![](https://github.com/goncalocostacarvalho/IronRegression-Quest/blob/main/IronRegression-Quest-Yr_Renovated.png)
  
- A correlation matrix was also done and since there was no correlation above 0.9, none of columns was dropped:

![](https://github.com/goncalocostacarvalho/IronRegression-Quest/blob/main/IronRegression-Quest-Correlation-Matrix.png) 

- Finally, was ploted boxplots for every columns and took off the results outside the InterQuartile range. Below and example:

| Before | After |
| :---: | :---: |
|![](https://github.com/goncalocostacarvalho/IronRegression-Quest/blob/main/IronRegression-Quest-Boxplot-Outliers.png)|![](https://github.com/goncalocostacarvalho/IronRegression-Quest/blob/main/IronRegression-Quest-Boxplot-NoOutliers.png)|

# Results 💥

![](https://github.com/goncalocostacarvalho/IronRegression-Quest/blob/main/IronRegression-Quest-Results.png)

# Conclusions 💭

- Less data doesn't mean a more accurate model
- Accuracy results doesn't change too much with the data cleaning and featuring engineering
- XGBoost got the best results suggesting a non linear relationship between features and target
