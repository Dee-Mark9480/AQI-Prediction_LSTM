# AQI Prediction using LSTM

Overview
This repository contains the implementation of an AQI (Air Quality Index) prediction model using LSTM (Long Short-Term Memory) neural networks. The project follows a structured pipeline, including data preprocessing, AQI calculation, feature engineering, hyperparameter tuning, and model training.


Project Structure
The repository consists of three Jupyter notebooks:

1. Data Preprocessing (imputation.ipynb)
This notebook handles raw data cleaning and preprocessing, ensuring the dataset is ready for further analysis and modeling.
- Handles missing values and removes unwanted rows/columns.
- Implements KNN imputation using the best hyperparameters to fill missing values.
- Saves the processed dataset for the next steps.

2. AQI Calculation (AQI calci.ipynb)
This notebook computes the AQI based on pollutant concentration levels.
- Introduces a new column for AQI values.
- Uses AQI formula based on pollutants such as CO, NO₂, PM₂.₅, PM₁₀, SO₂, etc.
- Adds a new column for AQI values, which serves as the target variable for prediction in the next steps.

3. Feature Engineering & Model Training (better_model.ipynb)
This notebook performs feature engineering, hyperparameter tuning, and model training.
- Extracts time-based features and compute lagged and rolling features.
- Uses hyperparameter tuning to optimize the LSTM model.
- Trains an LSTM model to predict AQI for the next 6 hours.
- Evaluates the model using RMSE, R2, MAPE, and MAE.


Installation & Dependencies
To run the notebooks, ensure you have the required Python libraries installed:
```numpy pandas matplotlib seaborn scikit-learn keras tensorflow```


Usage
Run imputation.ipynb to preprocess the raw data.
Run AQI calci.ipynb to compute AQI values.
Run better_model.ipynb to train and evaluate the LSTM model.
