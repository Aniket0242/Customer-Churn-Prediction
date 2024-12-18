
# Customer Churn Project : Telco

This project is a machine learning project focusing on customer churn prediction. The project consists of 4 main steps: 
- Data Preprocessing and Model Development (CatBoost)
- Interface (Streamlit)
- API (FastAPI)
- Automation (Docker)


## Project Folder Structure
```bash
Telco Customer Churn Project/
│
├── data/
│   ├── churn_data_regulated.parquet
│   ├── WA_Fn-UseC_-Telco-Customer-Churn.csv
│   ├── ...
│
├── model/
│   └── cat_model.cbm
│
├── notebooks/
│   ├── telco-customer-churn-eda.ipynb
│   ├── telco-catboost-xgboost-shap-lime.ipynb
│
├── src/
│   ├── fast-api.py
│   ├── predict.py
│   ├── streamlit-app.py
│   └── train_model.py
│
└── Dockerfile
└── requirements.txt
```

## Project Files

- **data/**: Contains the data files used for the project.
- **model/**: Contains the trained model file.
- **notebooks/**: Includes Jupyter Notebooks used for data analysis and model development.
- **src/**: Contains the source code of the project. Model training, prediction and service/application development are located in this folder.

## Steps
1. **Data Preprocessing and Model Development**: Using the script `train_model.py`, Telco Customer data is preprocessed and a machine learning model is created using the CatBoost model.
2. **Interface**: Using the model, the `streamlit-app.py` script allows the user to enter new customer information and based on this information the churn probability is estimated. Furthermore, the overall SHAP graph of the model and the specific SHAP graph of the selected customer are shown.
3. **API**: The `fast-api.py` script creates an API using the model created with train_model.py. This API takes customer data and returns the churn probability.
4. **Automation**: Using Docker, the project is containerized and made executable through the `predict.py` script. This script takes customer data and calculates the churn probability.
