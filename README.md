# Loan Approval Model Effectiveness Analysis

## 📊 Overview
This project evaluates the **effectiveness of a new loan approval model** in reducing financial risk and improving decision-making accuracy for loan officers. Using **A/B testing** and statistical analysis in R, it compares the **new (Treatment)** and **existing (Control)** models on key performance metrics such as **Type II errors**, **F1 Score**, and **Officer Agreement**.

The study aims to determine whether the new model improves the accuracy of loan decisions, minimizes bad loans, and enhances officer trust in the model’s predictions.

---

## 🧠 Objectives
1. **Minimize financial losses** by reducing Type II errors (approving bad loans).  
2. **Improve model performance** through a higher F1 Score — balancing precision and recall.  
3. **Increase officer agreement** with model predictions, indicating greater trust and consistency.  

---

## 🧩 Methodology
### Data Preparation
- Converted categorical variables (e.g., `Variant`) into factors for statistical tests.
- Filtered out incomplete data (`fully_complt = 0`).
- Normalized metrics (e.g., `typeII_fin_norm`) to ensure fair comparison across officers.

### Hypothesis
1. The new model reduces Type II errors.
2. The new model improves F1 Score.
3. Officers agree more with predictions made by the new model.

### Statistical Tests Used
- **Welch’s t-test** for comparing group means.
- **Pairwise t-test** with Bonferroni-Holm adjustment.
- **Effect size (Cohen’s d)** for measuring practical significance.

---

## 📈 Results Summary
| Metric | Control (Old Model) | Treatment (New Model) | % Improvement | p-value | Effect Size (Cohen’s d) |
|--------|---------------------|------------------------|---------------|----------|--------------------------|
| **Type II Errors** | 0.125 | 0.0856 | ↓ 31.2% | 0.0049 | -1.72 |
| **Recall** | 0.637 | 0.767 | ↑ 20.4% | < 0.005 | — |
| **F1 Score** | 0.483 | 0.647 | ↑ 33.6% | < 0.005 | 1.15 |
| **Officer Agreement** | 0.068 | 0.148 | ↑ 117% | 0.0025 | — |

✅ The **Treatment group significantly outperformed** the Control across all metrics.  
✅ The large **effect sizes** confirm meaningful and reliable improvements.  

---

## 🧠 Key Insights
- **New model reduces Type II errors** by over 30%, lowering financial risks.  
- **F1 Score improvement** indicates better overall classification balance.  
- **Increased officer agreement** reflects higher trust in the new system.  

---

## 💡 Recommendations
1. **Integrate financial impact metrics** to connect prediction quality with profitability.
2. **Enhance model training** with larger, more diverse datasets.
3. **Maintain randomization** in officer assignment to eliminate bias.
4. **Monitor performance continuously** to adapt to changing economic conditions.

---

## 🧾 Technologies Used
- **Language:** R  
- **Libraries:**  
  - `tidyverse`, `dplyr`, `effectsize`, `ggplot2`, `pwr`  
- **Techniques:**  
  - Data Cleaning & Normalization  
  - A/B Testing  
  - Statistical Hypothesis Testing  
  - Visualization with ggplot2  

---
