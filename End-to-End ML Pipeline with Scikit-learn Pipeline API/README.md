# End-to-End ML Pipeline with Scikit-learn Pipeline API

## Objective
Build a production-ready machine learning pipeline to predict customer churn using the Telco Customer Churn dataset.

---

## Dataset
- **Name:** WA_Fn-UseC_-Telco-Customer-Churn.csv
- **Source:** IBM Telco Churn Dataset
- **Description:** Includes customer demographic info, account details, and churn status.

---

## Key Steps

1. **Data Preprocessing**
   - Dropped 'customerID'
   - Converted 'TotalCharges' to numeric and filled missing values
   - Encoded categorical variables using OneHotEncoder
   - Scaled numeric columns using StandardScaler

2. **Train-Test Split**
   - Split data into 80% training and 20% testing sets

3. **Pipeline Construction**
   - Used `Pipeline` and `ColumnTransformer` to streamline preprocessing and model training

4. **Model Training**
   - Logistic Regression
   - Random Forest

5. **Hyperparameter Tuning**
   - Used `GridSearchCV` for both models to find the best parameters

6. **Evaluation**
   - Evaluated models using classification report (precision, recall, f1-score, accuracy)

7. **Model Saving**
   - Exported best model using `joblib` as `best_telco_churn_model.joblib`

---

## How to Run
1. Make sure the dataset file `WA_Fn-UseC_-Telco-Customer-Churn.csv` is in the same directory as the notebook.
2. Open and run the notebook `telco_churn_pipeline.ipynb` in Jupyter Notebook.
3. The model will be saved in the current directory.

---

## Requirements
- Python 3.x
- pandas
- numpy
- scikit-learn
- joblib
