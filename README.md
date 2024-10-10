# Rainfall Prediction using Time Series Forecasting

## Overview

This project focuses on predicting rainfall for various locations in Australia using historical weather data. The dataset used in this project is from the **Weather Australia** dataset available on Kaggle. The goal is to forecast whether it will rain tomorrow (`RainTomorrow`) based on a variety of meteorological features.

## Project Structure

- **Preprocessing**: The raw data was preprocessed to handle missing values, encode categorical variables, and perform feature scaling. The final preprocessed dataset is named `rain_data`.
- **Modeling**: The XGBoost algorithm was applied to the time series data for predicting rainfall. XGBoost is effective for handling structured data and capturing relationships between features.
- **Train-Test Split**: 
  - Training data: 2008 to 2015 for all locations.
  - Test data: 2015 to 2017 for all locations.

## Files

- **Timeseries.zip**: Contains all the preprocessed data (`rain_data`) and the model training code.
- **rain_data.csv**: Preprocessed dataset used for training the model.
- **model.py**: Python script containing the XGBoost model training process.
- **results.csv**: Prediction results from the model on the test dataset.

## How to Run

1. Clone the repository:
   ```bash
   git clone <repository-url>

2. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Run the model training script:
   ```bash
   python model.py
   ```

## Model Architecture

- The model is built using the XGBoost algorithm:
  - XGBoost handles the structured data efficiently and is capable of capturing complex relationships between features.
  - The model was tuned with hyperparameters to improve prediction accuracy.

## Results

- **Accuracy**: 84%
- **Precision**:
  - Class 0: 86%
  - Class 1: 74%
- **Recall**:
  - Class 0: 96%
  - Class 1: 42%
- **F1-Score**:
  - Class 0: 90%
  - Class 1: 54%
- **ROC AUC Score**: 0.830

- Class Imbalance: The dataset has more instances of non-rainy days compared to rainy days (100,000 Class 0, 30,000 Class 1).

## Dataset

The dataset contains weather observations from 41 different locations in Australia, with features like temperature, humidity, wind speed, and pressure. The target variable is `RainTomorrow`, indicating whether it rained the next day.

## Future Work

- Improving model performance through further hyperparameter tuning and exploring feature importance from the XGBoost model.
- Exploring additional models or ensemble techniques to compare with XGBoost.

## License

This project is licensed under the MIT License - see the LICENSE file for details.
```

Everything is in proper Markdown format now! You can paste this directly into your `README.md` file.
