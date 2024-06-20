A)Loading and Preprocessing Data:

1) Load the dataset from a CSV file.
2)Convert Mileage, Engine, and Power columns to numeric values after splitting.
3) Fill missing values in Mileage, Engine, Power, and Seats columns with the mean of the respective columns.
4) Create dummy variables for categorical features.
5) Standardize numerical features.           

B) Splitting Data:
Split the data into training and testing sets.
# Convert Mileage column to string type and split it, then convert to numeric                                                          

Your code is a comprehensive approach to data preprocessing, model training, and evaluation using linear regression and random forest regression. Let's break down and explain each part of the process:

1. Data Loading and Initial Exploration-Loading Data: The dataset is loaded from a CSV file.
Mileage Conversion: The Mileage column values are converted to float after removing the units (km/kg and kmpl).

2.Feature and Target Split: All columns except 'Price' are used as features, and 'Price' is the target variable.
Train-Test Split: The dataset is split into training and testing sets with a 70-30 split.

3.Manufacturer Extraction: The first word in the 'Name' column is extracted and stored in a new column 'Manufacturer'.

4.Column Dropping: Columns 'Name' and 'Location' are dropped as they are not directly useful for modeling.

5.Age Calculation: The 'Year' column is transformed to represent the age of the car.

6.Numeric Conversion: The 'Engine' and 'Power' columns are split to remove units and converted to numeric values.

7. Handling Missing Values: Missing values in 'Mileage', 'Engine', 'Power', and 'Seats' columns are filled with the mean of the respective columns.

8.Dropping Column: The 'New_Price' column is dropped as it is not useful for the current analysis.

9.Dummy Variables: Categorical features are converted to dummy/indicator variables.

10.Column Alignment: Ensures that the train and test sets have the same columns by adding any missing columns in the test set with zero values.

11. Standardization: Numerical features are standardized (scaled to have mean 0 and variance 1).

12.Linear Regression: The Linear Regression model is trained and evaluated.
Random Forest: The Random Forest Regressor model is trained and evaluated.
R^2 Score: The performance of both models is evaluated using the R^2 score, which indicates how well the models explain the variance in the target variable.

13. Plotting Manufacturer Counts: Plotting: A count plot of cars based on manufacturers in the training set is generated for visualization.


This complete workflow takes raw data, preprocesses it extensively to make it suitable for machine learning, splits it into training and testing sets, trains two different models (Linear Regression and Random Forest Regressor), evaluates their performance, and visualizes the data. Each step ensures that the data is cleaned, transformed, and standardized, and that models are built on reliable and consistent data.
