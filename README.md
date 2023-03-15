# Seoul Bike Sharing Predictive Model

## Overview

This project is aimed at predicting the amount of bikes rented on a particular day using the Seoul Bike Sharing data set. The data set is composed of 14 attributes and was analyzed using Python.

## Data Cleaning and Transformation

During the exploratory data analysis (EDA), it was determined that the target variable, Rented Bike Count, is numerically continuous, making it suitable for a regression model. Dew Point Temp was found to be a redundant variable, so it was dropped. The categorical variables in the data set were converted to numerical values, and no rare categories were present after dropping the Functional Day variable.

To deal with the skewness in continuous variables, Yeo-Johnson transformation was used for Temp and Wind. The other continuous variables were discretized since they did not have a normal distribution. Outliers present in Wind, Solar Radiation, Rain, and Snow variables were also handled. Feature scaling was performed for continuous variables to ensure that they all had the same scale.

## Model Development and Evaluation

A pipeline was created for data transformation and KNN regressor to prevent data leakage. Hyperparameter tuning was performed using range(2,10,2) for Discretizer Cont and Hour Transformer, Scalar Transformer Standard and MinMax, and KNN_n_neighbors = 1 was used to overfit the model to see if the data was capable of performing the prediction.

The final parameters were chosen based on validation scores, and the model was tested on test data that had not been seen by the model before. The results were a training score of 1.0, a validation score of 0.9999879, and a testing score of 0.9999878.

## Conclusion

The Seoul Bike Sharing Predictive Model was able to accurately predict the number of bikes rented on a particular day. With the insights gathered from the EDA and model development, we can make better decisions regarding bike sharing programs in Seoul.
