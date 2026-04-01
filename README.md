## Data Loading and Preprocessing:

The diabetic_data.csv was loaded.
Target variable readmitted was separated from features.
Categorical features were handled by filling missing values with "missing" and then LabelEncoder was applied.
Missing numerical values were imputed with the median.
The data was split into training (70%) and validation (30%) sets, stratified by the target variable.

## Model Training:

A RandomForestClassifier was trained on the preprocessed training data (X_train_split, y_train_split).

## Prediction:

Predictions were made on the validation set (X_val_split) to obtain readmission probability scores (y_proba).

## Feature Importance Analysis:

The top 10 most influential features according to the RandomForest model were identified and visualized in a bar plot. These included patient_nbr, num_lab_procedures, diag_1, diag_2, diag_3, num_medications, time_in_hospital, age, number_inpatient, and discharge_disposition_id.
A new binary target readmitted_30_days (1 for readmission within 30 days, 0 otherwise) was created for further analysis.

## Distribution Graphs:

Distribution plots (histograms and count plots) were generated for selected top features (num_lab_procedures, time_in_hospital, age, number_inpatient) against the readmitted_30_days status. These visualizations helped in understanding how the distributions of these features vary for readmitted vs. non-readmitted patients.

## Correlation Matrix:

A correlation matrix was computed for the top 10 features and the readmitted_30_days target. This was visualized as a heatmap, providing insights into the linear relationships between these important features and the likelihood of 30-day readmission.
In essence, the analysis involved preparing the data, building a predictive model, identifying key drivers of readmission, and then performing detailed exploratory data analysis to visualize and understand the relationships between these important features and the 30-day readmission outcome.
