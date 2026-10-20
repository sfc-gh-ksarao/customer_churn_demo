# Customer Churn - End-to-End Snowflake ML

Binary classification (churn yes/no) on `CUSTOMER_CHURN_DB.CHURN.CUSTOMER_CHURN_TRAINING`, covering training, experiment tracking, model registry, and inference.
`Customer_Churn_Load.ipynb` loads the data. `Customer_Churn_ML_Lifecycle.ipynb` trains Logistic Regression, Elastic Net, Random Forest and XGBoost and logs each run to a Snowflake Experiment.
The top model by AUC is registered in the Model Registry, with lineage back to the training Dataset, and scored in SQL with `MODEL(...)!PREDICT_PROBA(...)`.
