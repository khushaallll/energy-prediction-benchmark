# Benchmarking Machine Learning Approaches for Energy Prediction

## Project Overview

This project focuses on benchmarking different machine learning approaches for predicting household energy consumption. The goal is to compare multiple models under a **controlled and consistent experimental setup** and select the best-performing model based on RMSE.

The project follows a structured workflow:

* Data understanding and exploration
* Feature engineering and preprocessing
* Model benchmarking
* Hyperparameter tuning
* Final model selection and prediction

---

## Project Structure

```
energy-prediction-benchmark/
│
├── data/
│   ├── train.csv
│   ├── test.csv
│
├── notebooks/
│   ├── 01_eda.ipynb
│   ├── 02_benchmarking.ipynb
│
├── outputs/
│   ├── submission.csv
│
├── README.md
└── requirements.txt
```

---

## ⚙️ Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/YOUR_USERNAME/energy-prediction-benchmark.git
cd energy-prediction-benchmark
```

---

### 2. Create Virtual Environment

```bash
python -m venv venv
```

Activate it:

**Windows:**

```bash
venv\Scripts\activate
```

**Mac/Linux:**

```bash
source venv/bin/activate
```

---

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

If `requirements.txt` is missing:

```bash
pip install numpy pandas matplotlib seaborn scikit-learn xgboost lightgbm jupyter
```

---

### 4. Launch Jupyter Notebook

```bash
jupyter notebook
```

---

## How to Run the Project

### Step 1: Run EDA Notebook

Open and run:

```
notebooks/01_eda.ipynb
```

This notebook:

* Loads the dataset
* Performs data exploration
* Creates cleaned datasets for modelling

---

### Step 2: Run Benchmarking Notebook

Open and run:

```
notebooks/02_benchmarking.ipynb
```

This notebook:

* Builds preprocessing pipelines
* Benchmarks multiple ML models
* Performs hyperparameter tuning
* Generates predictions for test data

---

## Models Used

The following modelling approaches are compared:

* Linear Models: Linear Regression, Ridge
* Tree-Based Models: Decision Tree
* Ensemble Models: Random Forest
* Boosting Models: Gradient Boosting, XGBoost, LightGBM

---

## Evaluation Metric

The primary evaluation metric used is:

```
Root Mean Squared Error (RMSE)
```

All models are evaluated using cross-validation to ensure fair comparison.

---

## Output

Final predictions are saved as:

```
outputs/submission.csv
```

Format:

```
Household_ID,Energy_Consumption_kWh
```

---

## Key Features of the Project

* Consistent preprocessing using pipelines
* Fair benchmarking across multiple models
* Feature engineering (time-based and interaction features)
* Hyperparameter tuning for performance improvement
* Reproducible workflow

---

## Notes

* Do not modify the test dataset structure
* Ensure the same preprocessing is applied across all models
* Avoid data leakage by fitting transformations only on training data

---

## Author

Khushal

---
