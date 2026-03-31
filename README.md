# Patient-Analysis
Predicts the likelihood of a patient being readmitted within 30 days.


Overview

In the code below, I built a machine learning model to predict the likelihood of a patient being readmitted within 30 days. To generate predictions, I used a Random Forest classifier, which handles both categorical and numerical features. I trained the model using train.csv, validated its accuracy with dev.csv, and finally tested it on test.csv. During the development phase, the model achieved a ROC AUC score of 0.85, and in the testing phase, it scored 0.82.

Exploratory Data Analysis (EDA)
All datasets contained null values in both categorical and numerical columns. Some features required encoding because they were stored as non-numeric (object) data types. Additionally, columns used for targeting or containing unique identifiers were removed from the training dataset.

Preprocessing
To prepare the data, I removed any columns that were not part of the feature set. I also dropped the target column from the feature matrix to ensure proper model training. Next, I encoded categorical variables and handled missing values. Numerical columns were preprocessed, and missing values were filled using the median from the train.csv dataset.

Model Choice
As mentioned above, I selected a Random Forest classifier as my primary model due to its ability to handle both categorical and numerical data, as well as multiple features effectively. I also experimented with XGBoost to improve the ROC AUC score, but it did not outperform the Random Forest model. Initially, my model achieved a score of 0.76; however, after refining the code, I was able to improve performance to above 0.80. Model performance was evaluated using the dev.csv dataset and measured with ROC AUC.

Model Results
During the development phase, the model achieved a ROC AUC score of 0.85 locally, which matched the score on Codabench. In the testing phase, the local score initially reached 0.99; however, after further refinements, the Codabench score was 0.82.

Model Interpretation
To understand which features most influenced patient readmission within 30 days, I created a bar plot showing the top 10 most important features. The most impactful variables included age, total procedure cost, and total medication cost. These factors appear to play a significant role in determining whether a patient is likely to return to the hospital.
