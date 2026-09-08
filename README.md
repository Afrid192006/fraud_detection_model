# AI-Powered Financial Fraud Detection System

An end-to-end **Machine Learning-based fraud detection system** designed to identify potentially fraudulent financial transactions.

The project analyzes transaction behavior and financial attributes to classify transactions as **fraudulent or legitimate**, with a focus on exploratory data analysis, feature relationships, model development, and deployment-ready inference.

---

## Project Overview

Financial fraud detection is a highly imbalanced classification problem where fraudulent transactions represent only a small fraction of all transactions.

This project uses a large-scale transaction dataset containing **6,362,620 transactions** and develops a machine learning pipeline to identify fraudulent activity.

The analysis focuses on:

* Transaction behavior
* Transaction types
* Transaction amounts
* Sender account balances
* Receiver account balances
* Fraud distribution
* Feature relationships
* Machine learning-based fraud classification

---

## Objectives

* Analyze financial transaction patterns.
* Identify characteristics associated with fraudulent transactions.
* Perform exploratory data analysis and visualization.
* Prepare transaction data for machine learning.
* Train a fraud classification model.
* Evaluate model performance using appropriate classification metrics.
* Save the trained pipeline for future predictions and deployment.

---

## Dataset

The dataset contains **6,362,620 transaction records** with 11 columns.

| Feature          | Description                                    |
| ---------------- | ---------------------------------------------- |
| `step`           | Time step of the transaction                   |
| `type`           | Type of transaction                            |
| `amount`         | Transaction amount                             |
| `nameOrig`       | Originating customer identifier                |
| `oldbalanceOrg`  | Originating account balance before transaction |
| `newbalanceOrig` | Originating account balance after transaction  |
| `nameDest`       | Destination customer identifier                |
| `oldbalanceDest` | Destination account balance before transaction |
| `newbalanceDest` | Destination account balance after transaction  |
| `isFraud`        | Fraud label                                    |
| `isFlaggedFraud` | Existing fraud flag                            |

The dataset contains **8,213 fraudulent transactions** and **6,354,407 legitimate transactions**, demonstrating the severe class imbalance present in the problem.

---

## Exploratory Data Analysis

The analysis includes:

### Transaction Distribution

Transaction types are analyzed to understand the frequency of different transaction categories.

### Fraud Distribution

Fraudulent and legitimate transactions are compared to understand the class imbalance.

### Fraud by Transaction Type

Fraud distribution is analyzed across transaction types, with particular attention to **TRANSFER** and **CASH_OUT** transactions.

### Correlation Analysis

Correlation analysis is performed on:

* `amount`
* `oldbalanceOrg`
* `newbalanceOrig`
* `oldbalanceDest`
* `newbalanceDest`
* `isFraud`

The analysis also reveals strong relationships between some balance-related variables, such as `oldbalanceOrg` and `newbalanceOrig`.

---

## Machine Learning Pipeline

The project follows a structured machine learning workflow:

```text
Raw Transaction Data
        ↓
Data Cleaning
        ↓
Exploratory Data Analysis
        ↓
Feature Selection / Engineering
        ↓
Data Preprocessing
        ↓
Model Training
        ↓
Model Evaluation
        ↓
Trained Pipeline
        ↓
Fraud Prediction
```

The trained machine learning pipeline is saved as:

```text
fraud_detection_pipeline.pkl
```

---

## Technologies Used

### Programming Language

* Python

### Data Analysis

* Pandas
* NumPy

### Visualization

* Matplotlib
* Seaborn

### Machine Learning

* Scikit-learn

### Model Persistence

* Pickle

### Development Environment

* Jupyter Notebook

---

## Project Structure

```text
AI-Fraud-Detection/
│
├── analysis_model.ipynb
├── fraud_detection_pipeline.pkl
├── AIML Dataset.csv
├── README.md
│
└── screenshots/
    ├── transaction_distribution.png
    ├── fraud_distribution.png
    └── correlation_matrix.png
```

> Dataset files may be excluded from the repository if they are too large. In that case, provide instructions for downloading the dataset separately.

---

## Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/AI-Fraud-Detection.git
cd AI-Fraud-Detection
```

### 2. Create a virtual environment

```bash
python -m venv venv
```

Activate it:

**Windows**

```bash
venv\Scripts\activate
```

**Linux / macOS**

```bash
source venv/bin/activate
```

### 3. Install dependencies

```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```

### 4. Launch Jupyter Notebook

```bash
jupyter notebook
```

Open:

```text
analysis_model.ipynb
```

---

## Key Findings

The dataset is extremely imbalanced, with fraudulent transactions representing only a small percentage of the total dataset.

The analysis also examines fraud behavior across transaction types and investigates relationships between transaction amounts, account balances, and fraud labels.

Because fraud detection is an imbalanced classification problem, **accuracy alone is not sufficient** for judging model performance. Precision, recall, F1-score, ROC-AUC, and other appropriate metrics should be considered.

---

## Important Considerations

This project is intended for **educational and research purposes**.

The dataset represents simulated financial transactions and should not be interpreted as a production banking fraud-detection system.

A real-world deployment would require additional considerations such as:

* Real-time transaction processing
* Model monitoring
* Concept drift detection
* Threshold optimization
* False-positive management
* Data privacy
* Security
* Explainable AI
* Continuous model retraining

---

## Future Improvements

Planned improvements include:

* [ ] Build an interactive fraud detection dashboard
* [ ] Add real-time transaction prediction
* [ ] Implement SHAP-based model explainability
* [ ] Add automated model evaluation
* [ ] Create a REST API using Flask/FastAPI
* [ ] Add risk scoring
* [ ] Add transaction-level prediction interface
* [ ] Deploy the model as a web application
* [ ] Add model monitoring and drift detection

---

## Author

**Singapuri Afrid**

B.Tech Computer Science & Engineering — Artificial Intelligence & Machine Learning

Interested in:

**Artificial Intelligence • Machine Learning • Data Science • Software Development • Generative AI**

---

## If You Find This Project Useful

Give the repository a ⭐ and feel free to explore, improve, or contribute to the project.

---

## 📄 License

This project is intended for educational purposes. Add an appropriate open-source license if you plan to distribute or modify the project publicly.
