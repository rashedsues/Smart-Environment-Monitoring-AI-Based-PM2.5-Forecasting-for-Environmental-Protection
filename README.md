
# 🧠 Smart Environment Monitoring: Green Intelligence  
### AI-Based PM2.5 Forecasting for Environmental Protection

## 📌 Overview
This project applies deep learning techniques to predict hourly PM2.5 concentrations — one of the most dangerous airborne pollutants — using historical meteorological data. By accurately forecasting PM2.5 levels, this model supports early air pollution warnings, public health protection, and smart urban environmental management.

## 🎯 Objectives
- Predict PM2.5 concentrations using time-series weather data
- Compare traditional ML models (Random Forest, XGBoost, CatBoost) vs Deep Learning (LSTM)
- Visualize and interpret air quality trends
- Achieve high accuracy (R² > 0.95) using LSTM sequence models

## 📊 Dataset
**Source**: UCI Machine Learning Repository  
**Name**: Beijing Multi-Site Air-Quality Data  
**Station Used**: PRSA_Data_Aotizhongxin_20130301-20170228.csv

**Features**:
- PM2.5: Target variable (µg/m³)
- Meteorological: TEMP, PRES, DEWP, WSPM, RAIN
- Time: year, month, day, hour
- Pollutants (optional): PM10, SO2, NO2, CO, O3
- Wind direction: wd

## 🧪 Methodology

### ✅ Preprocessing:
- Combined time columns into a single datetime index
- Dropped rows with missing PM2.5 or weather values
- Normalized input features using MinMaxScaler
- Created lagged time-series sequences (24 hours history) for deep learning input

### ✅ Models Trained:

| Model         | R² Score | MSE       |
|---------------|----------|-----------|
| Random Forest | ~0.43    | ~4000     |
| XGBoost       | ~0.42    | ~4000     |
| CatBoost      | ~0.42    | ~4078     |
| **LSTM (Deep)**   | **0.955**  | **~0.05** |

## 📈 Visualizations
- PM2.5 trend over time
- Predicted vs actual PM2.5 (full test set + first 100 samples)
- Training vs validation loss
- Average PM2.5 by hour of day
- Correlation heatmaps between pollutants and weather

## 🧠 Technologies Used
- Python 3.11
- Pandas, NumPy
- Scikit-learn
- TensorFlow / Keras
- Matplotlib, Seaborn
- Jupyter Notebook / Google Colab

## 📁 Folder Structure
```
Smart-PM25-Prediction/
├── data/
│   └── PRSA_Data_Aotizhongxin_20130301-20170228.csv
├── notebook/
│   └── Smart_Environment_Monitoring_AI_Based_PM2_5_Forecasting.ipynb
├── README.md
└── requirements.txt
```

## ✅ How to Run
1. Clone the repo
2. Open the notebook in Jupyter/Colab
3. Install requirements: `!pip install -r requirements.txt`
4. Run all cells to train and evaluate the model

## 💡 Future Work
- Predict multiple hours ahead (multistep forecasting)
- Add more stations and spatial features
- Build a Streamlit web dashboard
- Integrate real-time data from APIs

## 🙌 Acknowledgements
- UCI Machine Learning Repository
- Beijing Environmental Monitoring Center
- TensorFlow and Scikit-learn developers

## 🌍 Why This Project Matters in Environmental Science

Air pollution is one of the leading causes of premature death and disease globally. PM2.5, or fine particulate matter, poses a serious threat to human health because of its ability to penetrate deep into the lungs and bloodstream. Real-time and predictive analysis of PM2.5 levels is crucial for:

- 🌱 Guiding environmental policy and urban planning
- 🏥 Issuing early health warnings to sensitive populations
- 🚦 Implementing dynamic traffic and industrial control strategies
- 📊 Supporting environmental research and decision-making

By using AI-powered forecasting models like LSTM, environmental scientists and policymakers can make **data-driven decisions** to **reduce pollution**, **improve air quality**, and **protect public health** in urban environments.
