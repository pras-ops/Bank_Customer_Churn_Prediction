#   Bank Customer Churn Prediction using H2O Auto ML

This project aims to predict customer churn in a bank using H2O Auto ML. Churn refers to the degree of customer inactivity or disengagement observed over a given time, and it can manifest in various forms within the data. The goal of this project is to identify the factors contributing to customer churn and build a prediction model that classifies if a customer is likely to churn or not. Additionally, the model should provide a probability of churn to assist customer service in targeting preventive measures effectively.

## Report

The analysis and modeling process for the Bank Customer Churn Prediction project involved the following steps:

1.  Data Analysis: Initial exploration of the dataset to understand its structure and relationships. This included visualizations such as pie charts and count plots to examine the proportion of customers who churned and retained based on various categorical variables.
    
2.  Feature Engineering: Creation of new features to enhance the predictive power of the model. Two new features were engineered in this project: `BalanceSalaryRatio` and `TenureByAge`. Visualizations, such as box plots, were used to analyze the relationships between these new features and customer churn.
    
3.  Data Preprocessing: Label encoding and one-hot encoding were performed on categorical variables to convert them into numerical form for model training. Additionally, scaling was applied to certain continuous variables using the MinMaxScaler.
    
4.  Model Building and Prediction using ANN: An Artificial Neural Network (ANN) model was built using the Keras library. The model consisted of three dense layers with ReLU activation and a final sigmoid activation layer for binary classification. The model was trained and evaluated using the training and test datasets, respectively. Performance metrics such as accuracy, precision, recall, and F1-score were computed, and a confusion matrix was visualized.
    
5.  Model Building and Prediction using H2O Auto ML: H2O Auto ML, an open-source, distributed machine learning platform, was utilized to build and compare multiple models automatically. The dataset was imported into H2O, and a train-test split was performed. The H2OAutoML class was used to define the model, specifying a maximum runtime, maximum number of models, seed, verbosity, and number of folds for cross-validation. The model was trained on the training dataset, and the leaderboard was generated to compare the performance of different models. The best-performing model, a Stacked Ensemble model, was selected for further analysis. Model details and parameters were examined, and predictions were made on the test dataset.
    

The results of the H2O Auto ML model showed promising performance in predicting customer churn. The selected Stacked Ensemble model demonstrated superior performance compared to other models in the leaderboard. The model's accuracy, precision, recall, and F1-score can be seen in the classification report. The confusion matrix provides a visual representation of the model's predictions compared to the actual values.

Overall, this project provides insights into customer churn in a bank and offers a predictive model to identify customers at risk of churn. By leveraging H2O Auto ML, the project demonstrates the automation of model building and evaluation, making it easier for organizations to implement churn prevention strategies effectively.
