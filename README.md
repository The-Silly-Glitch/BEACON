# 🧠 BEACON (Borrower Economic Analysis & Credit Outcome Network)

An end-to-end AI-powered loan underwriting system that evaluates borrowers using multiple machine learning models.

Instead of relying on a single prediction model, this system combines:

- Default risk prediction  
- EMI affordability analysis  
- 5-year financial health simulation  
- A final AI decision engine  

This creates a complete intelligent loan evaluation pipeline.

---

# 🚀 System Overview

The system evaluates loan applicants using three independent ML models:

## 🔹 Model 1 — Default Prediction
Predicts the probability that a borrower will default using **XGBoost Classification**.

**Output:**
- Default Probability (0–1)

---

## 🔹 Model 2 — EMI Stress Analysis
Predicts how financially stressful the EMI will be using **XGBoost Regression**.

**Output:**
- EMI Stress Score (0–100)
- Stress Category (Low / Moderate / High / Severe)

---

## 🔹 Model 3 — 5-Year Financial Health Prediction
Simulates borrower finances over 5 years and predicts long-term financial sustainability.

**Output:**
- Financial Health Score (0–100)
- Financial Stability Category

---

## 🔹 Final Decision Engine

Combines all three model outputs and generates:

- ✅ Approve  
- ⚠ Approve with Caution  
- ❌ Reject  
- Detailed Risk Report  

---

# 🏗️ System Architecture

```
Borrower Input
↓
Model 1 → Default Probability
Model 2 → EMI Stress Score
Model 3 → Financial Health Score
↓
Final AI Decision Engine
↓
Loan Approval Recommendation
```

---

# 📂 Project Structure

```
AI-Loan-Risk-System/
│
├── Model1_Defaulter_Classification.ipynb
├── Model2_EMI_Stress.ipynb
├── Model3_Longtime_prediction.ipynb
├── final_decision_engine.ipynb
│
├── Model1/
├── Model2/
├── Model3/
├── Models/
│
├── requirements.txt
├── README.md
└── kaggle.json
```

---

# 🛠️ Installation

### 1️⃣ Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/ai-loan-risk-system.git
cd ai-loan-risk-system
```

### 2️⃣ Install dependencies

```bash
pip install -r requirements.txt
```

---

# 📊 Dataset Requirements

This project uses datasets from **Kaggle**:

* "Give Me Some Credit" Dataset (for Model 1)
* "LendingClub Loan Dataset" (for Model 2 & Model 3)

---

# ⚠️ Important: Kaggle API Required

To download datasets directly in Google Colab or locally, you must have a Kaggle API key file:

```
kaggle.json
```

### How to get it:

1. Go to: [https://www.kaggle.com/settings](https://www.kaggle.com/settings)
2. Scroll to the **API** section
3. Click **Create New API Token**
4. Download the `kaggle.json` file

Place it in:

```
~/.kaggle/kaggle.json
```

OR upload it to Colab before running dataset download commands.

Without this file, dataset download will fail.

---

# 📦 Dependencies

Core libraries used:

* pandas
* numpy
* scikit-learn
* xgboost
* joblib
* matplotlib
* seaborn

---

# 📈 Model Performance

* **Model 1:** High ROC-AUC for default prediction
* **Model 2:** High R² for EMI stress regression
* **Model 3:** High R² for financial health simulation

---

# 🔮 Future Improvements

* Streamlit web application interface
* Explainable AI (SHAP integration)
* FastAPI backend deployment
* Advanced financial simulation modeling
* Production-grade deployment

---

# 🎯 Purpose

This project demonstrates:

* Multi-model AI architecture
* Financial risk modeling
* Loan underwriting intelligence
* Machine learning pipeline integration
* Real-world ML system design

---

# 📜 License

This project is intended for educational and research purposes.
