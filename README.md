## Project Description

### Online Payment Fraud Detection 

This project involves building and evaluating models for detecting fraudulent transactions in an online payments dataset. The dataset was downloaded from Kaggle (https://www.kaggle.com/datasets/rupakroy/online-payments-fraud-detection-dataset/), and it contains more than 6 million records of different types of transactions, with each record labeled as either fraudulent or genuine.

Key stages in the project included data importation, data exploration, data cleaning, feature engineering, model building, and model evaluation.

#### Data Importation

The first step was to import the necessary libraries and load the dataset. Libraries used included pandas for data handling, seaborn and matplotlib for visualization, scikit-learn for machine learning, and a few others.

#### Data Exploration

Next, I analyzed the dataset using descriptive statistics and visualization. I noticed that the dataset was highly imbalanced, with genuine transactions significantly outnumbering fraudulent ones. The majority of fraudulent transactions were found in the 'TRANSFER' and 'CASH_OUT' types. 

#### Data Cleaning

In the data cleaning step, columns 'nameOrig', 'nameDest', and 'isFlaggedFraud' were dropped from the dataset as they were deemed not necessary for the model building process. 

#### Feature Engineering

The categorical feature, 'type', was one-hot encoded to convert it into a format that could be provided to the machine learning algorithms. The numerical features were scaled using the RobustScaler from scikit-learn, which is less affected by outliers than other methods.

#### Model Building

I divided the dataset into a training set and a test set, with 80% of the data used for training and 20% used for testing. 

Two different machine learning models were used: Logistic Regression and Random Forest. The models were trained using Stratified K-Fold cross-validation to ensure that each fold was a good representative of the whole dataset. GridSearchCV and RandomizedSearchCV were used to tune the hyperparameters of the models.

#### Model Evaluation

After training, the models were evaluated on the test set. The evaluation metrics used were the confusion matrix, accuracy score, and classification report. 

The RandomForest Classifier achieved an accuracy of around 99.97%, with excellent precision and recall, particularly for the minority class (fraudulent transactions). This model significantly outperformed the Logistic Regression model, which achieved an accuracy of approximately 99.93%.

In conclusion, the RandomForest Classifier was a highly effective tool for detecting fraudulent transactions in this online payment dataset. It could potentially be used in real-world systems to prevent fraudulent activity, protecting both businesses and customers from financial losses.
