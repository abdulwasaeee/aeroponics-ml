# Aeroponics Wastewater Prediction

This project uses data from an aeroponic-style greenhouse system to **predict wastewater discharge** using machine learning.

The goal is simple:

👉 understand when wastewater happens

👉 learn how data-driven models can help reduce it  

This repository focuses on **insight and clarity**, while detailed technical explanations are provided separately in the report.

---

## 📦 Dataset

The data comes from a real greenhouse experiment and is used as a **proxy for an aeroponic system**.

🔗 Dataset source (Kaggle):  
https://www.kaggle.com/datasets/sunainaroy/greenhouse-dataset

The dataset includes:
- temperature
- humidity
- CO₂ concentration
- irrigation and water supply
- wastewater discharge (drain water)

---

## 🎯 Objective

- Predict wastewater discharge using environmental and system data  
- Compare simple and advanced models  
- Use results to support better water-control decisions  

---

## 🧩 What Was Done (High-Level)

### 1. Data Understanding & Cleaning
- Selected only relevant sensor readings
- Converted data into a clean table
- Removed missing or invalid rows

### 2. Exploratory Data Analysis (EDA)
- Studied data distributions
- Checked relationships between inputs and wastewater
- Found that wastewater depends on **multiple interacting factors**

### 3. Model Building
- Trained three models:
  - Linear Regression (baseline)
  - Random Forest
  - Gradient Boosting
- Compared models using error metrics
- Gradient Boosting performed best, showing **nonlinear behavior**

### 4. Experiment Tracking
- Used MLflow to record:
  - model runs
  - performance scores
  - saved models
- Ensures results are reproducible

---

## 📊 Key Visual Results

Below are selected visuals to quickly understand the work.

### Dataset Overview
Shows a sample of the cleaned dataset used for modeling.

📁 <img width="1821" height="826" alt="datasets-sample" src="https://github.com/user-attachments/assets/a937ccde-a892-4b7a-a25d-466467e69ff9" />


---

### Correlation Analysis
Shows how environmental factors relate to wastewater.

📁 <img width="629" height="560" alt="correlation-matrix" src="https://github.com/user-attachments/assets/ff9f60a7-1db7-43bf-b393-f115feac028c" />


---

### Model Comparison
Compares performance of different models.

📁 <img width="1663" height="868" alt="model-comparision" src="https://github.com/user-attachments/assets/5bc83f25-2068-4e89-9987-336d21e5f406" />


---

### Experiment Tracking
Shows how model experiments were logged and compared.

📁 <img width="1920" height="919" alt="mlflow-tracking" src="https://github.com/user-attachments/assets/d9585a89-6e92-4361-b02e-f3d9bc259392" />


---

### Project Structure
Overview of how the project is organized.

 <img width="273" height="279" alt="file-structure" src="https://github.com/user-attachments/assets/96df1d03-bf04-40ab-8d25-04660f502bba" />


---

## 📂 Repository Structure (Simplified)

aeroponics-ml/

├── data/                   Raw sensor data and processed datasets

├── notebooks/              Exploratory Data Analysis (EDA) and model prototyping

├── results/                Model outputs and evaluation metrics

   └── screenshots/         Key visuals and charts for reports

├── mlruns/                 MLflow experiment tracking logs and metadata

├── requirements.txt        Python dependencies and library versions

└── README.md               Project overview and setup instructions
