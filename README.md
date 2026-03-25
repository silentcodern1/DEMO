# House-Price-Prediction
# USA House Price Prediction

This project aims to predict house prices in the USA using a Linear Regression model. The dataset used contains various features related to housing, including average area income, house age, number of rooms, number of bedrooms, and population of the area.

## Project Overview

The goal of this project is to build a predictive model that can estimate the price of a house based on its characteristics. We utilized exploratory data analysis (EDA) to understand the relationships within the data, followed by training and evaluating a Linear Regression model.

## Dataset

The dataset `USA_Housing.csv` includes the following features:
- `Avg. Area Income`: Average income of residents in the area.
- `Avg. Area House Age`: Average age of houses in the area.
- `Avg. Area Number of Rooms`: Average number of rooms in houses in the area.
- `Avg. Area Number of Bedrooms`: Average number of bedrooms in houses in the area.
- `Area Population`: Population of the area.
- `Price`: The target variable, representing the house price.
- `Address`: The address of the house (excluded from the model as it's non-numeric).

## Methodology

1.  **Data Loading and Inspection**: Loaded the dataset using pandas and performed initial checks (`.head()`, `.info()`, `.describe()`) to understand its structure and identify missing values or data types.
2.  **Exploratory Data Analysis (EDA)**: 
    -   Visualized relationships between variables using `pairplot`.
    -   Examined the distribution of house prices using a `distplot`.
    -   Analyzed correlations between numerical features using a heatmap to identify strong relationships.
3.  **Model Training**: 
    -   Splitting the data into training and testing sets (60% training, 40% testing).
    -   Trained a Linear Regression model from `scikit-learn` using the training data.
4.  **Model Evaluation**: 
    -   Made predictions on the test set.
    -   Evaluated the model's performance using standard regression metrics:
        -   **Mean Absolute Error (MAE)**: Measures the average magnitude of the errors in a set of predictions, without considering their direction.
        -   **Mean Squared Error (MSE)**: Measures the average of the squares of the errors, giving more weight to larger errors.
        -   **Root Mean Squared Error (RMSE)**: The square root of the MSE, providing an error metric in the same units as the target variable (Price).

## Results

The Linear Regression model provided the following evaluation metrics on the test set:
- MAE: 82288.22
- MSE: 10460958907.21
- RMSE: 102278.83

These metrics indicate the average error in the price predictions made by the model. A lower RMSE generally implies a better fit of the model to the data.
