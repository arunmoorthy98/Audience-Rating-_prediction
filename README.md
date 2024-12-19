## Presentation for Building and Validating a Model to Predict 'Audience Rating'

# 1. Problem Statement

# Objective: 

Build a model to predict the audience_rating of movies based on their features.

Dataset: Rotten Tomatoes movies dataset with features such as:

Rating (e.g., PG, R)

Genre (e.g., Comedy, Action)

Directors

Runtime in Minutes

Tomatometer Rating

Tomatometer Count

# 2. Data Overview

# Dataset Size 
Includes both numerical and categorical data with missing values in some columns.

Target Variable: audience_rating

Key Features:

Categorical: rating, genre, directors

Numerical: runtime_in_minutes, tomatometer_rating, tomatometer_count

# 3. Data Preprocessing

# Steps Performed:

Handling Missing Values:

For numerical features: Impute missing values using the mean.

For categorical features: Impute missing values using the most frequent value.

Feature Scaling:

Standardized numerical features using StandardScaler.

One-Hot Encoding:

Converted categorical variables into numerical format using OneHotEncoder.


# 4. Model Building

# Model Chosen: Random Forest Regressor

Suitable for handling mixed types of data and capturing non-linear relationships.

Pipeline:

Integrated preprocessing and model training using Pipeline for seamless data flow.

Data Split:

80% for training, 20% for testing using train_test_split.

# 5. Model Validation

# Evaluation Metrics:

Mean Absolute Error (MAE): 11.49

Average prediction error in audience ratings.

Mean Squared Error (MSE): 217.50

Penalizes larger errors more heavily.

Root Mean Squared Error (RMSE): 14.75

Typical error in predictions.

R-squared (R²): 0.67

Model explains 67% of the variance in the audience ratings.

Visualization:

Scatter plot showing Actual vs. Predicted Audience Ratings.

Most points align near the diagonal, indicating good predictions.

# 6. Feature Importance

# Key Insights:

tomatometer_rating and genre are the most important predictors of audience ratings.

runtime_in_minutes and directors contribute less but are still considered.

Visualization:

Bar chart ranking features based on their importance in the Random Forest model.

# 7. Conclusions

# Strengths:

Integrated pipeline ensures modular and reusable code.

Random Forest effectively handles categorical and numerical features.

Areas for Improvement:

Explore other models (e.g., Gradient Boosting) to reduce errors.

Perform hyperparameter tuning to optimize Random Forest.

Investigate additional data or engineered features for better accuracy.

# 8. Demo with Notebook

# Interactive Notebook Features:

Preprocessing and training pipeline implemented.

Visualizations for model performance and feature importance.

Evaluation metrics provided for accuracy validation.

