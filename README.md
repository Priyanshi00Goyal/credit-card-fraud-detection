# 💳 Credit Card Fraud Detection

<p align="center">
  <b>An End-to-End Machine Learning Project for Detecting Potentially Fraudulent Credit Card Transactions</b>
</p>

<p align="center">
  <a href="https://credit-card-fraud-detection-vcjbtrdmgshahd3zhc8bav.streamlit.app/">
    <img src="https://img.shields.io/badge/🚀%20Live%20Demo-Streamlit-red?style=for-the-badge" alt="Live Demo">
  </a>
  <a href="https://github.com/Priyanshi00Goyal/credit-card-fraud-detection">
    <img src="https://img.shields.io/badge/💻%20GitHub-Repository-black?style=for-the-badge" alt="GitHub">
  </a>
</p>

---

## 📌 Overview

**Credit Card Fraud Detection** is an end-to-end Machine Learning project developed as part of the **CodSoft Machine Learning Internship**.

The project focuses on analyzing transaction information and using classification models to identify transactions that may be potentially fraudulent.

The project covers the complete Machine Learning workflow:

```text
Dataset
   ↓
Data Preprocessing
   ↓
Exploratory Data Analysis
   ↓
Feature Engineering
   ↓
Model Training
   ↓
Model Evaluation
   ↓
Model Comparison
   ↓
Model Serialization
   ↓
Streamlit Application
   ↓
Cloud Deployment
```

---

## 🚀 Live Demo

### 🌐 Try the Application

**Live Application:**
https://credit-card-fraud-detection-vcjbtrdmgshahd3zhc8bav.streamlit.app/

The deployed application provides an interactive interface where users can enter transaction details and receive a machine learning-based fraud prediction and risk assessment.

---

## ✨ Key Features

### 🔍 Fraud Prediction

Enter transaction information and use the trained Machine Learning model to classify the transaction.

### 📊 Fraud Probability

When probability estimates are available, the application displays the model's estimated fraud probability.

### 🚨 Risk Assessment

Transactions are categorized into three risk levels:

| Fraud Probability | Risk Level |
| ----------------: | ---------- |
|           `< 30%` | 🟢 LOW     |
|    `30% – 69.99%` | 🟡 MEDIUM  |
|           `≥ 70%` | 🔴 HIGH    |

### 💰 Transaction Analysis

The application accepts information such as:

* Transaction amount
* Transaction category
* Gender
* Transaction hour
* Transaction day
* Transaction month

### 📍 Location Analysis

Customer and merchant geographic coordinates are used to calculate the approximate distance between them.

### 🌙 Transaction-Time Features

The application derives additional transaction features such as:

* Transaction hour
* Transaction day
* Transaction month
* Day of week
* Night transaction indicator
* Log-transformed transaction amount

### 📋 Transaction Summary

After entering transaction information, users can expand the transaction details section to review the submitted information and calculated distance.

---

## 🤖 Machine Learning Models

The project experiments with multiple classification algorithms:

### 1. Logistic Regression

A linear classification algorithm used as a baseline model.

### 2. Decision Tree

A tree-based classification algorithm capable of learning nonlinear decision rules.

### 3. Random Forest

An ensemble learning method that combines multiple decision trees for classification.

The models are compared using multiple classification metrics to select an appropriate final model.

---

## 📈 Model Evaluation

The project considers several evaluation metrics:

* **Accuracy**
* **Precision**
* **Recall**
* **F1 Score**
* **ROC-AUC**
* **Average Precision**

For fraud detection, looking beyond accuracy is important because classification performance can be affected by the distribution of legitimate and fraudulent transactions.

---

## 🧠 Feature Engineering

Several additional features are created from the transaction data.

### Transaction Amount

The original transaction amount is used as an input feature.

### Log Transaction Amount

A logarithmic transformation is applied:

```python
log_amt = np.log1p(amount)
```

This can help represent highly varied transaction amounts more effectively.

### Customer-to-Merchant Distance

The application calculates geographic distance using the Haversine formula.

```text
Customer Location
       ↓
   Haversine
       ↓
Merchant Location
       ↓
Distance in KM
```

### Night Transaction

A binary feature identifies transactions occurring during nighttime hours.

```text
Hour < 6 OR Hour >= 22
        ↓
   Night Transaction
```

---

## 🖥️ Streamlit Application

The Machine Learning model is integrated into an interactive **Streamlit** web application.

The application allows users to:

1. Enter transaction details
2. Enter customer and merchant location information
3. Calculate transaction distance
4. Submit the transaction
5. Generate a model prediction
6. View fraud probability
7. View the corresponding risk level
8. Review transaction details

---

## 🛠️ Tech Stack

| Technology                   | Purpose              |
| ---------------------------- | -------------------- |
| 🐍 Python                    | Programming Language |
| 🐼 Pandas                    | Data Processing      |
| 🔢 NumPy                     | Numerical Computing  |
| 🤖 Scikit-learn              | Machine Learning     |
| 📊 Matplotlib                | Data Visualization   |
| 📈 Seaborn                   | Data Visualization   |
| 💾 Joblib                    | Model Serialization  |
| 🎈 Streamlit                 | Web Application      |
| ☁️ Streamlit Community Cloud | Deployment           |
| 🔧 Git & GitHub              | Version Control      |

---

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

---

## 📓 Jupyter Notebook

The main Machine Learning workflow is documented in:

```text
notebooks/fraud_detection.ipynb
```

The notebook contains the development workflow used for the fraud detection model, including data analysis, preprocessing, feature engineering, model training, and evaluation.

---

## 💾 Trained Model

The selected trained model is stored using **Joblib**:

```text
models/
└── fraud_detection_model.pkl
```

The application loads this serialized model when the Streamlit application starts.

---

## 📊 Results

Model comparison results are stored in:

```text
results/model_comparison.csv
```

This file contains the recorded comparison of the experimented classification models.

---

## ⚙️ Installation

### 1. Clone the Repository

```bash
git clone https://github.com/Priyanshi00Goyal/credit-card-fraud-detection.git
```

### 2. Navigate to the Project

```bash
cd credit-card-fraud-detection
```

### 3. Create a Virtual Environment

```bash
python -m venv .venv
```

### 4. Activate the Environment

**Windows PowerShell:**

```powershell
.\.venv\Scripts\Activate.ps1
```

**Windows Git Bash:**

```bash
source .venv/Scripts/activate
```

### 5. Install Dependencies

```bash
pip install -r requirements.txt
```

### 6. Run the Application

```bash
streamlit run app.py
```

The application will open locally at:

```text
http://localhost:8501
```

---

## 📦 Dataset

The project uses the **Credit Card Fraud Detection** dataset available through Kaggle.

The original dataset is not included in this repository because of its size.

---

## 🔐 Data & Repository Practices

Large raw datasets are excluded from version control using `.gitignore`.

The repository focuses on the reproducible project components:

* Source code
* Jupyter notebook
* Trained model
* Feature information
* Evaluation results
* Dependency configuration

---

## 🎯 Learning Outcomes

Through this project, I strengthened my understanding of:

* Machine Learning classification
* Data preprocessing
* Exploratory Data Analysis
* Feature engineering
* Model comparison
* Classification metrics
* Model serialization
* Streamlit application development
* Git & GitHub
* ML model deployment

---

## 🔮 Future Improvements

Potential improvements for future versions include:

* [ ] More advanced fraud detection models
* [ ] Improved feature engineering
* [ ] Better handling of class imbalance
* [ ] Interactive model-performance dashboard
* [ ] More detailed transaction analytics
* [ ] Improved UI/UX
* [ ] Model explainability
* [ ] Automated model monitoring
* [ ] Improved production-grade prediction pipeline

---

## ⚠️ Disclaimer

This project is developed for **educational and portfolio purposes**.

The prediction generated by the application represents a machine learning model's estimate and should not be treated as definitive evidence that a transaction is fraudulent.

---

## 👩‍💻 Author

### Priyanshi Goyal

**GitHub:**
https://github.com/Priyanshi00Goyal

**Project Repository:**
https://github.com/Priyanshi00Goyal/credit-card-fraud-detection

**Live Demo:**
https://credit-card-fraud-detection-vcjbtrdmgshahd3zhc8bav.streamlit.app/

---

<p align="center">
  ⭐ If you found this project interesting, consider giving the repository a star!
</p>

<p align="center">
  <b>Built with Python • Machine Learning • Streamlit 🚀</b>
</p>
