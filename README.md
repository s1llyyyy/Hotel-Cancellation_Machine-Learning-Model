# Hotel Demand Forecasting and Cancellations Prediction

This project aims to predict hotel booking demand and cancellations using machine learning. The data used for this project comes from a hotel located in Portugal and is provided by Purwadhika Digital Technology School. This project is part of my 3rd capstone project in the Data Science Program at Purwadhika.

## Project Author

**Fareza Duta Pradana**  
- [LinkedIn](https://www.linkedin.com/in/muhammad-fareza-duta-pradana/)  
- [GitHub](https://www.github.com/s1llyyyy)  
- [Portfolio](https://www.datascienceportfol.io/farezaduta)

## Business Problem Statement

The hotel industry is highly competitive, with fluctuating demand based on seasonality. Managing room cancellations and optimizing room rates are critical challenges due to the perishable nature of hotel inventory (unsold rooms result in lost revenue).

**Objective:**  
The goal is to create a model that accurately predicts customer cancellations and demand trends, helping the hotel optimize room rates, manage inventory efficiently, and maximize revenue.

## Research Question

How can we accurately predict customer cancellations to minimize lost revenue and optimize room occupancy?

## Dataset Overview

The dataset contains booking details such as:
- **Country**
- **Market Segment**
- **Previous Cancellations**
- **Booking Changes**
- **Deposit Type**
- **Days in Waiting List**
- **Customer Type
- **Room Type**
- **Special Requests**
- **Car Parking Spaces**
- **Whether the booking was canceled or not**

## Approach

### Analytic Approach

The project emphasizes the importance of managing false negatives (missed cancellations) over false positives, as unsold rooms directly impact revenue. The model aims to minimize these false negatives using the **F2 score** as the evaluation metric.

### Modeling Steps

- **Data Preprocessing:**
  - Handled missing values and duplicated data.
  - Performed encoding for categorical variables (Binary, Ordinal, and One-Hot Encoding).
  - Applied Robust Scaling for numerical features.

- **Model Selection:**  
  Various machine learning models were tested, including:
  - KNN
  - Logistic Regression
  - Decision Tree
  - Random Forest
  - AdaBoost
  - Gradient Boost
  - XGBoost (Best model)

- **Resampling Techniques:**  
  To handle imbalanced data, methods like **SMOTE**, **Random Over Sampling**, **Random Under Sampling** and **NearMiss** were applied. Random Under Sampling (RUS) proved the most effective.

- **Hyperparameter Tuning:**  
  Hyperparameter tuning was performed using **Bayesian Optimization** and **RandomizedSearchCV** to improve model performance.

- **Evaluation Metric:**  
  The **F2 score** was chosen to emphasize reducing false negatives due to the business need to minimize lost revenue from cancellations.

- **Threshold Tuning:**  
  The optimal threshold for classifying cancellations was fine-tuned to maximize the F2 score.

## Model Performance

The final model selected was **XGBoost**, with a tuned F2 score of **0.7553** after threshold tuning.

## Conclusion

The project successfully developed a machine learning model to predict hotel cancellations, allowing the hotel to make more informed decisions about inventory management and pricing strategies. By focusing on reducing false negatives, the hotel can minimize the financial impact of unsold rooms.

---
