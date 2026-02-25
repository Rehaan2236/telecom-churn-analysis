# 📱 Telecom Customer Churn — End-to-End Data Analysis

> **Exploratory Data Analysis, Hypothesis Testing, and Predictive Modeling on the Churn Phone Dataset**

---

## 🗂️ Project Overview

This project applies a full data science workflow to a telecommunications churn dataset of **3,333 customer records**. The goal is to identify behavioral patterns that distinguish churners from retained customers, test those patterns statistically, and build a baseline predictive model.

**Key results:**
- Identified customer service call frequency and daytime usage as the strongest churn signals
- Confirmed significance with t-tests (p < 10⁻²⁶ and p < 10⁻¹⁰⁷) and chi-square tests
- Achieved **AUC = 0.80** with Logistic Regression baseline
- Engineered a rule-based `high_svc_caller` flag that identifies a segment with **2.5× baseline churn rate**

---

## 📁 Repository Structure

```
├── churn_analysis.ipynb   # Main notebook — full analysis end-to-end
├── README.md              # This file
└── data/
    └── churn.csv          # Dataset (or download link below)
```

---

## 📊 What's Inside the Notebook

| Section | Contents |
|---------|----------|
| 1. Data Summary | Schema, shape, variable dictionary, target definition |
| 2. EDA | Distributions, categorical breakdowns, correlation matrix |
| 3. Data Cleaning | Missing value imputation, encoding, redundancy removal |
| 4. Feature Engineering | `total_minutes`, `total_charge`, `high_svc_caller` flag |
| 5. Hypothesis Testing | t-tests + chi-square with effect sizes |
| 6. Modeling | Logistic Regression + Random Forest with ROC, confusion matrix, feature importance |
| 7. Recommendations | Actionable business takeaways |

---

## 🔍 Key Findings

**1. Daytime usage predicts churn**
Churners average 209.7 day minutes vs. 181.6 for retained customers — a statistically significant difference (t = 10.69, p = 2.94×10⁻²⁶, Cohen's d = 0.52).

**2. Customer service calls are the #1 signal**
Churners average 3.79 service calls vs. 2.02 for retained customers (t = 22.88, p < 10⁻¹⁰⁷). Customers with 4+ calls churn at **38.8%** — nearly 2.5× the 15.6% baseline.

**3. International plan has no effect**
Chi-square test confirms no significant association (χ² = 0.14, p = 0.71). This feature can be deprioritized in models.

**4. Model performance**
| Model | AUC | 5-Fold CV AUC |
|-------|-----|--------------|
| Logistic Regression | 0.80 | 0.81 ± 0.02 |
| Random Forest | 0.77 | 0.79 ± 0.02 |

---

## 🚀 Getting Started

```bash
# Clone the repo
git clone https://github.com/yourusername/churn-analysis.git
cd churn-analysis

# Install dependencies
pip install pandas numpy matplotlib seaborn scikit-learn scipy jupyter

# Launch notebook
jupyter notebook churn_analysis.ipynb
```

---

## 🛠️ Tech Stack

`Python 3.10` · `pandas` · `numpy` · `matplotlib` · `seaborn` · `scikit-learn` · `scipy`

---

## 📬 Contact

**[Your Name]** — [LinkedIn](https://linkedin.com/in/yourprofile) · [Portfolio](https://yoursite.com)

*Feel free to open an issue or reach out with questions or feedback!*
