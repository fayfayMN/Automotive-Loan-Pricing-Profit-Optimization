# 🚗 e-Car Loan Pricing Optimization Analysis
**Business Analytics & Predictive Modeling | Collaborative Team Project  | Feifei Li, Michelle Nguyen, Patrick Madla Sanchez**

## 🎯 Project Overview
This project was a collaborative effort to analyze **208,085 loan applications** for e-Car, an online lender. [cite_start]Our team identified a systematic overpricing pattern and developed a scalable, data-driven pricing engine to capture an estimated **$30–$35 Million** in annual unrealized profit[cite: 88, 109].

---

## 👥 Team Roles & Contributions
To ensure the highest level of accuracy, our team divided responsibilities into specialized workstreams:

### **Feifei  | Lead Data Analyst**
* **Technical Execution:** Developed the end-to-end analytical pipeline in **R**, including data cleaning, logistic regression modeling, and profit optimization.
* [cite_start]**Data Visualization:** Engineered high-impact visualizations (Profit Curves, ROC Curves, and Distribution Histograms) to translate complex statistical findings into actionable business insights[cite: 57, 48, 17].
* [cite_start]**Statistical Validation:** Conducted ROC analysis to verify a model AUC of 0.814, ensuring "excellent discriminatory power" for business decision-making[cite: 49].

### **Michelle & Patrick | Research & Data Quality Assurance**
* [cite_start]**Domain Research:** Conducted deep-market research into automotive lending trends and competitor APR benchmarks to ground our model in industry reality [cite: 137-142].
* [cite_start]**Data Integrity & Audit:** Performed rigorous detail-checking and data validation to ensure no "pricing errors" or anomalies compromised the integrity of the final analysis[cite: 9, 234].
* [cite_start]**Business Logic Verification:** Validated the cost-of-funds and loan-term constraints used in the profit optimization formula [cite: 54-55].

---

## 🛠️ The Data Science Solution

### 1. Segment Deep Dive
[cite_start]We focused on a "Teaching Segment" of 1,540 loans (FICO 684-712, Used Cars, 60-month terms) to prove the value of optimized pricing [cite: 31-36].


<img width="975" height="469" alt="image" src="https://github.com/user-attachments/assets/b109b29d-892a-430b-86b4-af3dddec19ee" />




### 2. Predictive Modeling
We modeled the probability of loan acceptance ($P(Accept)$) as a function of the quoted APR:
* [cite_start]**Model Equation:** $P(Accept) = 1 / (1 + exp(-(6.36 - 1.13 \times APR)))$[cite: 43].
* [cite_start]**Insight:** Every 1% increase in APR reduces the odds of acceptance by **67.6%**[cite: 46].


<img width="975" height="614" alt="image" src="https://github.com/user-attachments/assets/348f8588-1de9-4416-b8c2-1d59ae80a1a3" />



### 3. Profit Optimization
We balanced margin vs. volume using the formula:
> [cite_start]**Expected Profit** = $P(Accept) \times (APR - \text{Cost of Funds}) \times \text{Loan Amount} \times (\text{Term}/12)$[cite: 51, 115].

<img width="975" height="644" alt="image" src="https://github.com/user-attachments/assets/ca163ef9-c3ed-4ec4-ae59-e3fa68e32340" />

<img width="975" height="445" alt="image" src="https://github.com/user-attachments/assets/9fd26d78-71c9-4600-a2f5-8445b0f167b7" />

---

## 📈 Key Results (Teaching Segment)
| Metric | Current State | Optimized State | Change |
| :--- | :--- | :--- | :--- |
| **APR** | 6.45% | **4.75%** | [cite_start]-1.70 pts [cite: 59] |
| **Acceptance Rate** | 35.3% | **73.2%** | [cite_start]+37.9 pts [cite: 59] |
| **Expected Profit / Loan** | \$1,934 | **\$2,655** | [cite_start]**+37.3%** [cite: 59] |

[cite_start]**Total Segment Opportunity:** **$1.11 Million**[cite: 59].


---

## 📁 Project Artifacts
* **[Technical R Script](./final_Analysis_e-car.Rmd):** Full source code for cleaning and modeling.
* [cite_start]**[Final Executive Report](./Final--e-Car_Pricing_Optimization_Analysis.docx):** Complete business case [cite: 1-7].
* **[Presentation Deck](https://mnscu-my.sharepoint.com/personal/ed2865cl_go_minnstate_edu/_layouts/15/stream.aspx?id=%2Fpersonal%2Fed2865cl%5Fgo%5Fminnstate%5Fedu%2FDocuments%2FMIS%20380%20%2D%20Nomis%20B%20Case%20Study%20Presentation%20%28Group%201%29%2Emp4&referrer=StreamWebApp%2EWeb&referrerScenario=AddressBarCopied%2Eview%2Eeb714d76%2Daa9a%2D40f7%2Da9a9%2Defa20a632a6d&ct=1774551363551&or=Teams%2DHL&ga=1&LOF=1):** Three-part executive presentation.

---

## 🧰 Tech Stack
* **Language:** R (tidyverse, ggplot2, ROCR, readxl).
* **Concepts:** Logistic Regression, Price Elasticity, Profit Optimization, Data Auditing.
