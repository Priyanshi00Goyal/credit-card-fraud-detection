# 💳 Credit Card Fraud Detection

An end-to-end Machine Learning project that detects potentially fraudulent credit card transactions using classification algorithms and an interactive Streamlit application.

## 🚀 Live Application

The Streamlit application will allow users to enter transaction details and receive:

* Fraud probability
* Risk level
* Transaction classification
* Customer-to-merchant distance
* Model performance information

## 🎯 Project Objective

The goal of this project is to build a machine learning system capable of identifying potentially fraudulent transactions while handling the challenges of an imbalanced classification problem.

## 🧠 Machine Learning Models

Three classification algorithms were evaluated:

* Logistic Regression
* Decision Tree
* Random Forest

The models were compared using multiple evaluation metrics rather than relying only on accuracy.

## 📊 Evaluation Metrics

The project evaluates models using:

* Accuracy
* Precision
* Recall
* F1 Score
* ROC-AUC
* Average Precision

For fraud detection, **Precision, Recall, and F1 Score** are particularly important because missing fraudulent transactions can be costly.

## ⚙️ Machine Learning Pipeline

```text
Dataset
   ↓
Data Cleaning
   ↓
Exploratory Data Analysis
   ↓
Feature Engineering
   ↓
Data Preprocessing
   ↓
Model Training
   ↓
Model Evaluation
   ↓
Model Comparison
   ↓
Best Model Selection
   ↓
Model Serialization
   ↓
Streamlit Application
```

## ✨ Features

### 🔍 Fraud Prediction

Enter transaction information and obtain a machine learning prediction.

### 📈 Fraud Probability

The application displays the model's estimated fraud probability when probability estimates are available.

### 🚨 Risk Assessment

The application presents a simple:

* LOW
* MEDIUM
* HIGH

risk indicator based on the predicted probability.

### 📍 Distance Analysis

The application calculates the geographic distance between the customer and merchant locations.

### 📊 Model Comparison

The Streamlit application can display the performance of the evaluated machine learning models.

## 🛠️ Tech Stack

| Technology   | Purpose             |
| ------------ | ------------------- |
| Python       | Programming         |
| Pandas       | Data manipulation   |
| NumPy        | Numerical computing |
| Scikit-learn | Machine Learning    |
| Matplotlib   | Visualization       |
| Seaborn      | Visualization       |
| Joblib       | Model serialization |
| Streamlit    | Web application     |

## 📁 Project Structure

```text
credit-card-fraud-detection/
│
├── app.py
├── README.md
├── requirements.txt
├── .gitignore
│
├── models/
│   ├── fraud_detection_model.pkl
│   └── feature_info.pkl
│
├── notebooks/
│   └── fraud_detection.ipynb
│
└── results/
    └── model_comparison.csv
```

## 📦 Dataset

This project uses the **Credit Card Fraud Detection** dataset available on Kaggle.

The original dataset files are not included in this repository because of their large size.

## ▶️ Run Locally

Clone the repository:

```bash
git clone https://github.com/Priyanshi00Goyal/credit-card-fraud-detection.git
```

Move into the project:

```bash
cd credit-card-fraud-detection
```

Create and activate a virtual environment:

```bash
python -m venv .venv
```

Install the dependencies:

```bash
pip install -r requirements.txt
```

Run the Streamlit application:

```bash
streamlit run app.py
```

## ⚠️ Disclaimer

This project is developed for educational and portfolio purposes. The model's predictions should not be treated as definitive evidence of fraudulent activity.

## 👩‍💻 Author

**Priyanshi Goyal**

GitHub: `Priyanshi00Goyal`

---

⭐ If you find this project interesting, consider starring the repository.
