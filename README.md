Portfolio Project 2: Analysis of Car Sell Dataset
Overview
The second analysis task involves two main objectives: (1) training linear regression models to predict the selling prices of cars, and (2) assessing data ethics issues related to the presentation of results. The analysis follows a standard data science workflow, focusing on feature selection and the impact of training/testing data sizes on model performance.

Project Workflow
1. Data Acquisition
Dataset: The project uses a cleaned car sales dataset named car_sells_clean_data.csv, containing 3,657 entries.
2. Data Exploration
Initial Inspection: Utilized Pandas to load the dataset and examined its structure with head() and info() methods to identify column types and data types.
Correlation Analysis: Calculated correlations between relevant features (year, km_driven, seller_type, fuel, owner) and selling price. Categorical features were converted to numerical values using OrdinalEncoder.
3. Data Cleaning
Feature Encoding: Converted categorical columns (seller_type, fuel, owner) into numerical codes for analysis.
4. Data Analysis
Correlation Results:
The correlation of year with selling_price is the highest (0.41), indicating a significant positive impact.
Other features like km_driven and owner_code showed weaker negative correlations.
Hypothesis:
The car's year will be the strongest predictor of selling price.
Features such as km_driven may contribute less but should still be included for a complete model.
5. Train/Test Data Splitting
Randomly split the dataset into training and testing sets with varying sizes:
Case 1: 10% training data and 90% testing data.
Case 2: 90% training data and 10% testing data.
6. Model Training
Linear Regression Models: Trained four models to evaluate performance based on feature selection:
Model A: Case 1 with two most correlated features.
Model B: Case 1 with two least correlated features.
Model C: Case 2 with two most correlated features.
Model D: Case 2 with two least correlated features.
7. Model Evaluation
Performance Metrics: Evaluated models using Mean Squared Error (MSE) and Root Mean Squared Error (RMSE).
Results showed varying performance across models, with Model C achieving the lowest MSE and RMSE, indicating better feature selection and data size contributed to improved model performance.
8. Visualization
Comparative Analysis: Visualized MSE and RMSE for each model to compare performance.
The analysis demonstrated that models trained with the most correlated features and more training data typically performed better.
9. Ethical Considerations
Data Ethics Evaluation: Discussed the potential ethical concerns in data presentation, highlighting how sorting criteria can manipulate perceptions of success among countries.
Emphasized the importance of context in data reporting to avoid misleading interpretations.
Conclusion
This analysis confirms the significance of feature selection and data size in training predictive models. Ethical considerations in data presentation are crucial to ensure transparency and prevent bias in audience interpretation.
