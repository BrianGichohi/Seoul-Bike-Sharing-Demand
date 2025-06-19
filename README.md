# Seoul-Bike-Sharing-Demand
To determine the key factors affecting rental bike demand across the year in Seoul, Korea (2017-2018) using Regression Models

##  Table of Contents

- [Project Overview](#project-overview)
- [Dataset](#dataset)
- [Tools & Libraries](#tools-and-libraries)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [Modeling](#modeling)
- [Results](#results)
- [Conclusions](#conclusions)
- [Screenshots](#screenshots)
- [How to Run](#how-to-run)
- [License](#license)
  

# project overview 
----------------------------
The goal of the project is to predict the rental bike demand based on the variables present: Hour, temperature, humidity, windspeed, visibility, dew point temperature, solar radiation, rainfall, snowfall, seasons, holidays
and functional days.

It applies common data science techniques such as :
- Data Cleaning and Processing.
-  Exploratory data analysis
-  Data Visualization
-  Feature Engineering
-  Model training (Linear Regression, Polynomial Regression, Gradient Boosting and GridSearch CV)
-  Evaluation with R-squared

# dataset
------------------------------
- Source : https://archive.ics.uci.edu/dataset/560/seoul+bike+sharing+demand
- Duration : December 1st 2017 to November 31st 2018
- Observations : 8760
- Features : Date, Rented Bike Count, Hour, temperature, humidity, windspeed, visibility, dew point temperature, solar radiation, rainfall, snowfall, seasons, holidays

# tools and libraries
-----------------------------------------------
- 'Python 3.13.0'
- 'Pandas and NumPy': **Data Manipulation**
- 'Matplotlib and Seaborn' : **Data Visualization**
- 'Scikit-learn' : **Modelling and Evaluation**
- 'Jupyter' : **Notebook interface**

# exploratory data analysis
-------------------------------------------------
Some of the Key Insights observed during the EDA process include:
- There is a steady increase in demand for the bikes from the hours of 10:00am to 6:00pm before it gradually starts decreasing as the night begins:
![Average Bike Rentals by hours of the day](https://github.com/user-attachments/assets/54feaf03-3e2e-490a-a28b-48ac34dafa2d)

- During the weeks in which it is **Summer** it is when the rate at which rental bikes are in high demand while in the weeks in which it is **Winter** the demand for rental bikes is low:
  ![Average Rental Demand by week across each season](https://github.com/user-attachments/assets/40cffe7b-69b1-4e5d-b9c6-df8953906f30)

  - The **Summer Period** is when there is a high demand for rental bikes:
    ![Average Rentals by Season](https://github.com/user-attachments/assets/9740bad0-4b45-45ef-825a-c851e2eb7685)

-  The demand for rental bikes increases with the increase in temperature with the relationship between the two being strongly Positive:
  ![Relationship between Temperature and Rental Bike Count](https://github.com/user-attachments/assets/86e29eba-9d87-4348-be17-3abcb3ee71b7)


# modeling
------------------------------------
At the start of the modeling phase, the categorical variables dataset was subjected to **One Hot Encoding** and the dataset was subjected to **Normalization** using a **Standard Scaler**
The model was trained using :
**a) Multilinear Regression**
**b) Polynomial Regression**
**c) Gradient Boosting Regressor**

The Hyperparameter Tuning was done using **GridSearchCV**
The data was split into training and testing data with 70% of it being training data and 30% being testing data.

# results
| Model                           | R-squared score     |
----------------------------------|-------------------- |
| Multilinear Regression          |  0.551696           |
| Polynomial Regression           |  0.718120           |
| Gradient Boosting Regressor     |  0.855677           |
| GridSearchCV                    |  0.933446           |       





    
 
 

  

  
