# 🌊 Flood Risk Prediction Using Machine Learning

An end-to-end predictive machine learning framework designed to assess, classify, and forecast flood risks based on hydrological, meteorological, and environmental geospatial indicators.

---

## 📌 Project Overview

Floods cause catastrophic infrastructural and economic damage globally. Timely and accurate prediction enables proactive disaster management and emergency resource allocation. 

This project develops an end-to-end data pipeline that:
* Ingests and cleans multi-variable hydrological and environmental data.
* Performs exploratory data analysis (EDA) to evaluate non-linear relationships between precipitation, runoff, and terrain features.
* Implements robust feature scaling, missing value imputation, and correlation analysis.
* Trains and benchmarks multiple classification and regression algorithms (e.g., Logistic Regression, Random Forest, XGBoost, LightGBM).
* Evaluates predictive performance using precision-recall dynamics, ROC-AUC curves, and confusion matrix analysis.

---

## 📊 Dataset & Features

The model analyzes environmental metrics that directly impact water runoff and waterlogging vulnerability:

| Feature Name | Description |
| :--- | :--- |
| `Rainfall / Precipitation` | Cumulative rainfall depth over specified duration (mm) |
| `River Water Level` | Gauge readings indicating proximity to flood crest stage |
| `Elevation / Slope` | Digital Elevation Model (DEM) topographical attributes |
| `Soil Moisture / Type` | Saturation capacity and infiltration rates |
| `Drainage Capacity` | Local hydrological discharge throughput |
| `Flood Occurrence (Target)` | Binary indicator (`0: No Flood`, `1: Flood Event`) or continuous flood probability score |

---

## ⚙️ Model Architecture & Benchmarking

The modeling workflow evaluates diverse statistical and ensemble learners:
* **Baseline Linear Models:** Logistic Regression / Ridge Classification
* **Tree-Based Ensembles:** Random Forest Classifier (`RandomForestClassifier`)
* **Gradient Boosting:** XGBoost (`XGBClassifier`) / Gradient Boosting Trees
* **Validation Strategy:** Stratified $K$-fold cross-validation to account for seasonal and class imbalances.

### Performance Metrics
* **Accuracy & Macro $F_1$-Score**
* **Precision & Recall** (optimizing for high recall to minimize false negatives in disaster scenarios)
* **ROC-AUC Score**

---

## 🚀 Getting Started

### 1. Clone the Repository
```bash
git clone [https://github.com/Rimi-351/flood_prediction.git](https://github.com/Rimi-351/flood_prediction.git)
cd flood_prediction
