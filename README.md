# BTTAI_2
## Breakthrough_AI_project_2

### Airbnb Listings Review Score Prediction
#### Project Overview
This project aims to predict the ```review_scores_value``` for Airbnb listings based on various attributes related to the listings, hosts, and reviews. By understanding the factors that influence review scores, Airbnb hosts can optimize their listings to improve guest satisfaction and increase booking rates.

#### Dataset Description
The dataset used in this project includes various attributes of Airbnb listings such as host details, listing characteristics, and review scores. It contains 28,022 entries and 50 columns.

Key Columns:
    host_response_rate
    host_acceptance_rate
    host_is_superhost
    host_listings_count
    price
    instant_bookable
    calculated_host_listings_count
    reviews_per_month
    n_host_verifications
    review_scores_value (target variable)

#### Problem Statement

The goal is to predict the review_scores_value for Airbnb listings based on the given features. This is a regression problem, as we are predicting a continuous numerical value.

Project Steps
1. Data Preparation
Handling Missing Values: Imputed missing values using the mean for numerical features and the most frequent value for categorical features.
Encoding Categorical Features: Converted boolean and categorical features to numerical values using one-hot encoding.
Scaling: Scaled numerical features to a standard range using StandardScaler.
2. Model Training and Evaluation
Linear Regression Model
Model Training: Trained a Linear Regression model on the prepared data.
Evaluation:
MAE (Mean Absolute Error): 0.308
RMSE (Root Mean Squared Error): 0.514
Random Forest Regressor (Improved Model)
Model Training: Used GridSearchCV to find the best parameters for the Random Forest Regressor.
Evaluation:
Best Parameters: {'max_depth': 10, 'n_estimators': 200}
MAE: 0.298
RMSE: 0.504
3. Visualizations
Actual vs. Predicted Values
Scatter plots showing the relationship between actual and predicted review scores for both models.
Residuals
Residual plots showing the distribution of errors for both models.
#### Key Findings
Model Performance: The Random Forest Regressor performed slightly better than the Linear Regression model, capturing non-linear relationships and interactions between features.
Feature Importance: Features such as price, host_response_rate, and reviews_per_month are likely influential in predicting review_scores_value.
Business Insights: Airbnb hosts can improve their listings by focusing on responsiveness, acceptance rates, competitive pricing, and offering features that guests value.
#### Conclusion
Predicting the review_scores_value for Airbnb listings provides valuable insights into what factors contribute to higher guest satisfaction. By optimizing these factors, hosts can improve their review scores, leading to better guest experiences and potentially higher booking rates.

How to Use This Project
Clone the Repository:

```git clone https://github.com/gir-ma/airbnb-review-score-prediction.gitcd airbnb-review-score-prediction```


Install Dependencies:

Run the Notebook:
Open and run the Jupyter Notebook ```Airbnb_Review_Score_Prediction```.ipynb to see the complete analysis and results.

#### Files in the Repository

   - ```Airbnb_Review_Score_Prediction```.ipynb: Jupyter Notebook containing the data analysis, model training, and evaluation steps.
  - ```data/airbnbListingsData.csv```: The Airbnb listings dataset (make sure this file is placed correctly in the directory).

#### Future Work
1. Feature Importance Analysis: Further analyze feature importance from the Random Forest model to identify the most influential features.
2. Advanced Models: Explore more advanced models like Gradient Boosting Machines (e.g., XGBoost) for potentially better performance.
3. Model Deployment: Deploy the model in a real-world scenario where hosts can input their listing features and get predicted review scores.


License
This project is licensed under the eCornell and UCLA License.

