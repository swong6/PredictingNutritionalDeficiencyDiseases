# Predicting Vitamin Deficiency Diseases

## Overview
Vitamin deficiencies affect millions globally and often go undiagnosed until symptoms become severe. This project builds a predictive model to identify individuals at risk of vitamin deficiency-related diseases early, enabling proactive healthcare interventions and improved patient outcomes.

## Objective
Can we accurately predict the likelihood of vitamin deficiency diseases based on demographic, dietary, lifestyle, and clinical data to support early diagnosis and treatment recommendations?

## Tools Used
- **Python** (Pandas, Scikit-learn, Matplotlib, Seaborn)
- **Jupyter Notebook** for analysis and modeling
- **Machine Learning** (Logistic Regression, CART Decision Trees)

## Process
1. **Data Exploration & Cleaning** – Analyzed dataset structure, handled missing values (32% for Alcohol Consumption, 33% for Symptoms), and identified key variables
2. **Outlier Management** – Retained clinically meaningful outliers (BMI, lab values) representing severe deficiency cases
3. **Feature Engineering** – Incorporated demographic, lifestyle, dietary, and clinical variables
4. **Model Development** – Tested Logistic Regression and CART models with cross-validation
5. **Model Evaluation** – Compared performance and selected optimal model
6. **Results & Insights** – Documented actionable findings for healthcare stakeholders

## Data Preparation

![Data Preparation](images/data-preparation.png)

**Key Highlights:**
- Complete dataset with no missing values across 4,000 patients
- Clinical validity ensured—outliers represent real, severe cases
- 32 balanced and comprehensive variables ready for modeling

## Model Performance

### Logistic Regression Overview

![Logistic Regression Overview](images/logistic-regression-overview.png)

**Model Details:**
- Estimates probability for each of 5 deficiency diseases
- Predictors: Demographic & Lifestyle, Dietary Intake (% RDA), Lab Values, Symptoms
- Train/Test Split: 80% / 20%
- **Test Accuracy: 93.1%** – Strong overall predictive ability

### Logistic Regression Results

![Logistic Regression Performance](images/logistic-regression-performance.png)

**Key Findings:**
- Correctly identifies most Healthy (296), Rickets/Osteomalacia (198), and Anemia (225) cases
- Night Blindness (14) and Scurvy (12) have fewer correct predictions—indicates misclassification
- Most confusion occurs between Night Blindness and Anemia due to overlapping symptoms

### CART Model Performance

![CART Model Performance](images/cart-model-performance.png)

**Model Highlights:**
- Tuned using GridSearchCV (5-fold cross-validation)
- Optimal hyperparameters: Full-depth tree (max_depth=None, no pruning)
- Optimized for macro F1-score (multi-class fairness)
- **Test Accuracy: 99.25%** – Excellent classification across all disease categories

## Key Insights
- ✅ **CART model significantly outperforms logistic regression** (99.25% vs 93.1% accuracy)
- ✅ **Data quality is critical**: Proper handling of outliers and missing values directly improved model performance
- ✅ **Demographic, dietary, and clinical variables are strong predictors** of vitamin deficiency diseases
- ✅ **Early detection is possible**: High accuracy enables proactive healthcare interventions

## Business Impact
- **Improved Diagnosis**: 99.25% accuracy enables confident early detection of vitamin deficiency diseases
- **Healthcare Efficiency**: Automated risk screening can support triage and resource allocation
- **Patient Outcomes**: Early intervention reduces severity and improves treatment efficacy

## Deliverables
- **Jupyter Notebook** – Complete analysis, data cleaning, modeling, and evaluation workflow
- **Presentation Slides** – Executive summary and key findings
- **Dataset** – Processed vitamin deficiency data (4,000 patients, 32 variables)

## Files
| File | Description |
|------|-------------|
| `Vitamin Deficiency w_ RQ.ipynb` | Complete analysis notebook with EDA, feature engineering, and modeling |
| `Vitamin Deficiency Project Slides.pdf` | Executive presentation with visualizations and recommendations |
| `vitamin_deficiency_disease_dataset_20260123.csv` | Source dataset (4,000 patients with demographics, lifestyle, diet, lab values, symptoms) |
| `images/` | Supporting visualizations from the analysis |
| `README.md` | This file |

---

**Note:** This project was completed as part of my Master's in Business Analytics program. It demonstrates the application of predictive analytics to real-world healthcare challenges, combining data science with business acumen to drive meaningful outcomes.
