# Corizo-Major-project
# Semiconductor Manufacturing Yield Prediction

## Domain: Semiconductor Manufacturing Process

Modern semiconductor manufacturing is a highly complex process monitored using hundreds of sensor signals collected at various process points. However, not all signals are equally informative — some are noisy or redundant. This project applies feature selection and machine learning to identify the most relevant signals and predict yield outcomes (Pass/Fail) for production units.

---

## Context

In semiconductor fabrication lines, engineers monitor hundreds of signals per unit. These signals contain:
- Useful process information  
- Irrelevant or redundant signals  
- Noise  

By applying feature selection, we aim to isolate the most impactful signals contributing to yield excursions (unexpected drops in yield), which in turn can help:
- Increase process throughput  
- Reduce per-unit production cost  
- Improve time-to-learn for anomalies  

---

## Dataset Description

**File**: `sensor-data.csv`  
**Shape**: (1567 rows, 592 columns)  
- **Features**: 591 sensor signals per production unit  
- **Target**: `Yield`
  - `-1` → Pass  
  - `1` → Fail  

Each row represents a production unit and its associated sensor readings at a specific test point.

---

## Project Objective

To:
- Build a classifier to predict whether a unit will pass or fail.
- Analyze whether all features are necessary, or if performance can be retained or improved by selecting the most relevant ones.

---

## Project Steps

### 1. Data Import & Exploration
- Load and understand the structure, shape, and types of data.

### 2. Data Cleansing
- Handle missing values
- Drop irrelevant or constant features
- Apply domain-driven assumptions for cleaning

### 3. Data Analysis & Visualization
- Perform relevant statistical analysis
- Conduct univariate, bivariate, and multivariate analysis
- Provide detailed interpretation after each analysis

### 4. Data Preprocessing
- Separate features and target
- Check for class imbalance and apply balancing techniques (e.g., SMOTE)
- Train-test split and standardization if required
- Validate if train/test sets preserve the original data distribution

### 5. Model Training, Testing, and Tuning
- Choose and train supervised learning models
- Use cross-validation for robustness
- Apply GridSearchCV for hyperparameter tuning
- Techniques that may enhance performance:
  - Dimensionality reduction
  - Attribute removal
  - Standardization/Normalization
  - Target balancing

- Evaluate models using classification reports and confusion matrices
- Compare multiple models such as:
  - Random Forest  
  - Support Vector Machine (SVM)  
  - Naive Bayes  
  - And potentially other advanced models

- Compare all models using training and testing accuracy
- Select the final best model with detailed justification
- Save the final model for deployment or future use

### 6. Conclusion & Future Scope
- Summarize key findings
- Discuss potential improvements or next steps

---

## Notes

- This project not only helps optimize yield prediction but also demonstrates practical use of feature selection and model evaluation techniques in high-dimensional data scenarios.
