# 💰 Salary Prediction: Cracking the 250k Record Puzzle

What determines a professional's paycheck? I analyzed a dataset of **250,000 records** to move past generic salary estimates and build a high-precision prediction engine. This isn't just a regression exercise; it's about mapping how experience and education actually scale in the real world.

---

## 🎯 The Objective
The goal was to find a model that doesn't just "work" but provides enterprise-grade accuracy. I tested multiple linear and regularized approaches before landing on a solution that captures the non-linear growth patterns of professional income.

## 📊 The Model Bake-off
I put several algorithms to the test. While the linear models were strong, they couldn't beat the curve-fitting power of Polynomial features.

| Model | Train $R^2$ | Test $R^2$ | CV Score |
| :--- | :--- | :--- | :--- |
| Multiple Linear Regression | 0.9553 | 0.9559 | 0.9552 |
| Ridge / Lasso / ElasticNet | ~0.9553 | ~0.9559 | ~0.9552 |
| **Polynomial Regression (Deg 2)** | **0.9811** | **0.9807** | **0.9809** |

## 💡 The Winning Logic: Why Polynomial?
The baseline models hit a ceiling at **95.5%**. By moving to **Polynomial Regression (Degree 2)**, I pushed the accuracy to **98.1%**. 

The math is simple: Salary doesn't grow in a straight line. As professionals gain experience or higher degrees, their value compounds. Polynomial regression captured these "compounding" interactions that standard linear models missed, all while maintaining a nearly identical Cross-Validation (CV) score—proving the model is stable and not just memorizing data.

## 🛠️ The Toolkit
* **Data Handling:** `Pandas` and `NumPy` for managing the 250k-row pipeline.
* **Visualization:** `Seaborn` and `Matplotlib` to identify the "inflection points" where salaries jump.
* **Modeling:** `Scikit-Learn` for preprocessing, feature scaling, and regression analysis.

## 📂 Repository Structure
* `job-salary-pred_FINAL.ipynb`: The optimized Polynomial pipeline.
* `job_salary_pred(2_ER).ipynb`: Experiments with Ridge/Lasso/ElasticNet.
* `job-salary-pred.ipynb`: Initial baseline and Exploratory Data Analysis.

----

> **Note :** Achieving 98% accuracy is a milestone, but the real win is the consistency. By backing my choice with Cross-Validation (CV) and testing on unseen data, I've ensured this model is robust enough for real-world application.
