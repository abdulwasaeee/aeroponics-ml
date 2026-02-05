# Aeroponics Wastewater Prediction

This repository contains a machine learning workflow to predict wastewater discharge in aeroponic systems using greenhouse sensor data. The goal is to build predictive models that can help optimize water usage and reduce wastewater in soilless agriculture.

---

## 📦 Dataset

Data used in this project is sourced from the **Greenhouse Environment Dataset** available on Kaggle:

🔗 https://www.kaggle.com/datasets/sunainaroy/greenhouse-dataset

This dataset includes environmental measurements collected inside greenhouse compartments, such as temperature, humidity, CO₂ levels, irrigation, and drain water discharge. It serves as a proxy for aeroponic conditions.

---

## 🧠 Objective

Aeroponic systems aim to grow plants with minimal water waste. However, wastewater still occurs because of irrigation, environmental variations, and system inefficiencies.

The objective of this project is to:

- Predict wastewater discharge (`Drain`) using environmental and irrigation features
- Compare different machine learning models
- Extract insights that can help improve irrigation strategies

---

## 🛠 Work Done

### 1. Data Preparation

- Imported raw greenhouse CSV files
- Selected only relevant features:
  - `Tair` (air temperature)
  - `Rhair` (relative humidity)
  - `CO2air` (CO₂ concentration)
  - `Cum_irr` (cumulative irrigation)
  - `EC_drain_PC` (electrical conductivity of drain water)
  - `pH_drain_PC` (pH of drain water)
  - `water_sup` (water supply)
  - `Drain` (wastewater target)
- Converted all feature values to numeric
- Combined features and target into a clean tabular dataset
- Dropped rows with missing values

---

### 2. Exploratory Data Analysis (EDA)

- Plotted feature distributions  
- Generated correlation matrix
- Observed moderate correlation between:
  - Temperature, humidity, CO₂ and wastewater
- Irrigation-related features showed weak linear correlation

This helped inform model selection.

---

### 3. Modeling

Trained three regression models:

| Model                | Description                                |
|---------------------|--------------------------------------------|
| Linear Regression    | Simple baseline model                      |
| Random Forest        | Nonlinear model with decision trees        |
| Gradient Boosting    | Ensemble model that fits residual errors   |

**Metrics used:**
- Mean Squared Error (MSE)
- R² Score (coefficient of determination)

Observed that Gradient Boosting performed the best in capturing nonlinear relationships.

---

### 4. Experiment Tracking

Experiment runs were tracked using **MLflow**.  
This recorded:
- Model parameters
- Evaluation metrics
- Trained models

The `mlruns/` directory contains complete experiment logs for reproducibility.

---

