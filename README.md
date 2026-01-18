# Customer Growth & Retention Modeling

This project addresses a real-world business problem: 
**How to allocate a limited retention budget to maximize customer value?**

We develop an end-to-end analytical pipeline combining:
- Churn prediction (classification)
- Probabilistic churn modeling (BG-NBD)
- Survival analysis (time-to-churn)
- Customer Lifetime Value (CLV)

---

## 📊 Dataset
- `customers.csv`: customer-level information
- `transactions.csv`: historical transaction records

---

## 🧠 Methodology Overview

### 1. Customer Value Foundations
- RFM analysis
- Behavioral segmentation
- Relationship between RFM and churn

### 2. Churn Prediction (Classification)
- Binary churn label (60-day horizon)
- Feature engineering: RFM + frequency trends
- Models: Logistic Regression, Random Forest
- Metrics: ROC-AUC, Precision–Recall, Confusion Matrix

### 3. Churn via BG-NBD
- Purchase frequency modeling
- Probability customer is alive (P(alive))
- Expected future transactions
- Comparison with churn classification

### 4. Survival Analysis
- Time-to-churn modeling
- Cox Proportional Hazards & Weibull
- Survival curves
- Expected remaining lifetime

### 5. Customer Lifetime Value (CLV)
- BG-NBD + Gamma–Gamma
- Expected monetary value
- CLV estimation over fixed horizon

---

## 🎯 Final Business Question

**If the retention budget allows targeting only 20% of the customer base, which customers should be selected?**

### Compared Strategies
1. High churn probability (classification-based)
2. Low P(alive) (BG-NBD-based)
3. High CLV × High churn risk (survival-based)

### ✅ Recommendation
The **High CLV × High churn risk** strategy delivers the highest expected retained value and should be adopted for retention targeting.

---

## 📈 Key Results
- Classification AUC (60-day): ~0.92
- Strong consistency between churn labels and P(alive)
- Survival-based prioritization improves ROI over risk-only approaches

---

## 📁 Repository Structure
See `/notebooks` for step-by-step analysis and `/outputs` for final deliverables.

---

## 👤 Author
Nhu Y Luong 
