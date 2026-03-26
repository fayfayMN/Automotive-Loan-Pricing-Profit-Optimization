# Automotive Loan Pricing & Profit Optimization Analysis
**Predictive Analytics | Logistic Regression | R-Language**

## 🎯 Project Overview
This project leverages **208,085 loan applications** to identify and rectify pricing inefficiencies for e-Car, an online automotive lender. By modeling customer price sensitivity, I developed an optimization framework that identifies a **$30–$35 Million annual profit opportunity**.

---

## 🛠️ The Data Science Solution

### 1. Data Preparation & EDA
* Cleaned and analyzed a dataset of **208,085 approved applications**.
* Identified that **60-month terms** (49.3%) and **New/Used cars** (80%) dominate the portfolio.
* Discovered that lower APRs consistently lead to higher acceptance rates.

### 2. Predictive Modeling (Logistic Regression)
I modeled the probability of loan acceptance ($P(Accept)$) as a function of the quoted APR:
* **Model Equation:** $P(Accept) = 1 / (1 + exp(-(6.36 - 1.13 \times APR)))$.
* **Performance:** Achieved an **AUC of 0.814**, indicating excellent discriminatory power.
* **Key Insight:** Each 1% increase in APR reduces the odds of acceptance by **67.6%** (Odds Ratio: 0.324).

### 3. Profit Optimization Framework
I built a custom optimization function to find the "sweet spot" between high margins and high volume:
> **Expected Profit per Quote** = $P(Accept) \times (APR - \text{Cost of Funds}) \times \text{Loan Amount} \times (\text{Term}/12)$.

---

## 📈 Business Impact (Teaching Segment)
Focusing on a specific segment (FICO 684-712, Used Cars, 60mo, \$17.8K-\$25K):

| Metric | Current Practice | Optimal Recommendation | Improvement |
| :--- | :--- | :--- | :--- |
| **APR** | 6.45% | **4.75%** | -1.70 pts
