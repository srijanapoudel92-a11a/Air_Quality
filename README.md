# Air Quality Prediction
# Dataset and Problem

This project uses the UCI Air Quality dataset to predict carbon monoxide (CO) concentration. The dataset contains air-quality and environmental information such as temperature and humidity.

# Data Loading and Inspection

The dataset was loaded using ucimlrepo and Pandas. The data was checked for columns, data types, missing values, and basic statistics. Different charts were used to understand the data.

# Data Cleaning

The value `-200` was treated as missing data and replaced with NaN. Missing values were filled using median values. Duplicate records were also checked and removed. Outliers were examined but not automatically removed because they may represent real pollution levels.

# Feature Engineering

The `Date` and `Time` columns were combined into a datetime feature. Features such as year, month, day, hour, day of week, weekend, and rush hour were created to help the model understand time patterns.

# Model Development

Three models were tested:

* Linear Regression
* Random Forest Regression
* Gradient Boosting Regression

The models used preprocessing pipelines with imputation and scaling where needed.

# Testing and Evaluation

The data was split chronologically into 70% training, 15% validation, and 15% testing. The models were evaluated using MAE, RMSE, and R².

# Model Saving and Prototype

The final Random Forest model was saved as air_quality_model.pkl, and the feature list was saved as air_quality_features.pkl. A Gradio GUI was created so users can enter information and get a predicted CO concentration.

# Conclusion

This project demonstrates a complete machine-learning process, from data cleaning and analysis to model training, evaluation, saving, and deployment through a simple GUI.
