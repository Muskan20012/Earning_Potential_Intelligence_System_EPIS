# Earning Potential Intelligence System (EPIS)

### An AI-Based Income Classification and Predictive Analytics Model

---

##  Overview

The **Earning Potential Intelligence System (EPIS)** is a machine learning–based classification project designed to predict whether an individual earns **more than 50K per year** or **50K or less**, using demographic data.

This project was developed as a **capstone project during my AI Internship at Infosys**, with a focus on applying end-to-end machine learning concepts in a real-world, business-oriented problem.

---

## Problem Statement

Organizations often rely on manual or rule-based approaches to identify high-income individuals for financial planning, workforce analytics, or targeted services.
Such approaches are time-consuming, error-prone, and difficult to scale.

**EPIS aims to automate this process using machine learning**, enabling accurate and efficient income classification.

---

## Dataset Description

The project uses a census-based dataset containing demographic and employment attributes such as:

* Age
* Education and education level
* Occupation and work class
* Marital status and relationship
* Capital gain and capital loss
* Weekly working hours

**Target Variable:**

* `earning_potential`

  * `<=50K`
  * `>50K`

The dataset presents common real-world challenges including:

* Missing values
* Skewed numerical features
* Mixed categorical and numerical data
* Mild class imbalance (approximately 75:25)

---

## Approach & Methodology

### 1. Exploratory Data Analysis (EDA)

* Analyzed target class distribution and feature relationships
* Identified skewness and imbalance in the dataset
* Observed strong correlations between income and factors such as education, age, and working hours

### 2. Data Preprocessing

* **Missing Value Imputation**

  * Numerical features: Median (robust to skewness)
  * Categorical features: Mode
* **Outlier Handling**

  * IQR method applied selectively
  * Capital gain and capital loss were intentionally retained due to their strong predictive importance

### 3. Feature Engineering

* One-Hot Encoding applied to categorical features
* `ColumnTransformer` used for scalable preprocessing
* Clean separation of features and target variable

### 4. Model Building

* **Random Forest Classifier** used for training
* Chosen for its robustness, ability to handle non-linear patterns, and strong performance on structured data

---

## Model Evaluation

The model was evaluated using multiple metrics to account for class imbalance:

* Accuracy
* Precision
* Recall
* F1-score

**Key Result:**

* Achieved approximately **85% accuracy**
* Retaining meaningful extreme values (capital gain/loss) significantly improved performance

This highlights the importance of **domain-aware preprocessing decisions** in machine learning projects.

---

## Key Learnings

* Outliers are not always noise; sometimes they represent valuable signals
* Median imputation is often more reliable than mean for skewed data
* Accuracy alone is not sufficient for imbalanced classification problems
* Thoughtful preprocessing can have a greater impact than complex modeling

---

## Future Enhancements

* Experiment with Gradient Boosting and XGBoost
* Perform feature importance and model explainability analysis
* Deploy the model using Flask or FastAPI for real-time predictions

---

## Tech Stack

* **Programming Language:** Python
* **Libraries:** Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn
* **Tools:** Jupyter Notebook, GitHub

---

## Author

**Muskan Verma**
AI Intern | Aspiring Machine Learning Engineer

This project reflects my hands-on learning and application of machine learning concepts in solving a practical, real-world problem.

---

⭐ *If you found this project insightful, feel free to explore the notebook and share feedback.*
