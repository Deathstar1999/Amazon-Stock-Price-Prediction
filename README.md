# Stock Price Prediction for Amazon (AMZN)

## Objective

This project aims to predict the day-to-day price direction of Amazon.com, Inc. (AMZN) stock. Instead of forecasting the exact price, the focus is on determining whether the next day's closing price will be higher or lower than the opening price, enabling informed decisions on buying or selling.

## Dataset

The dataset spans from **1997 to 2020**, split into three parts:
- **Training Data**: 1997–2016 (`AMZN_train.csv`)
- **Validation Data**: 2016–2018 (`AMZN_val.csv`)
- **Testing Data**: 2018–2020 (`AMZN_test.csv`)

## Key Steps

### 1. **Data Exploration**
- Loaded and analyzed datasets to understand structure, trends, and attributes.
- Plotted stock price variables (`Open`, `Close`, `High`, `Low`) to identify potential patterns.

### 2. **Feature Engineering**
- Added features such as:
  - **Moving Averages**: 3-day and 7-day moving averages.
  - **Today’s Direction**: Difference between `Close` and `Open`.
  - **Price Range**: Difference between `High` and `Low`.
- Created a target variable (`Target`) indicating whether the closing price was higher than the opening price.

### 3. **Modeling**
Implemented and evaluated various machine learning models using `sklearn`:
- **Logistic Regression**
- **Decision Tree**
- **Random Forest**
- **Gradient Boosting Ensemble**

### 4. **Evaluation**
- Assessed model performance using the AUC (Area Under the Curve) metric.
- The **Gradient Boosting Classifier** achieved the best performance with an AUC of **0.55** on the validation set.

## Conclusion

Gradient Boosting emerged as the most effective model for this dataset. It demonstrated the highest AUC score among the tested algorithms and was further evaluated on the test set to simulate a production environment. A feature importance analysis highlighted the most critical features for prediction.

## Future Work

To improve prediction accuracy, the next step involves training a deep learning model with the goal of outperforming the baseline AUC of **0.55**.

## Visual Insights

### Feature Importance
A bar plot of feature importance was generated to showcase the significance of each feature in predicting the target variable.
