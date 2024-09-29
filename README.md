# Cybersecurity Incident Triage Classification

## Project Overview
This project aims to develop a machine learning model that classifies cybersecurity incidents into three categories: true positive (TP), benign positive (BP), and false positive (FP). Using Microsoft’s **GUIDE dataset**, the model supports Security Operation Centers (SOCs) by automating the triage process and providing accurate recommendations to SOC analysts. The model's performance is evaluated using the **macro-F1 score, precision, and recall** on both training and test datasets.

### Problem Statement:
The goal is to improve the efficiency of SOCs by classifying cybersecurity incidents. The model should help analysts prioritize critical incidents and reduce the number of false positives. It is built to generalize effectively to unseen data, making it reliable for real-world applications.

## Business Use Cases:
- **Security Operation Centers (SOCs):** Automating triage and prioritization of cybersecurity incidents.
- **Incident Response Automation:** Recommending guided actions for SOC analysts.
- **Threat Intelligence:** Improving threat detection accuracy using historical evidence.
- **Enterprise Security Management:** Enhancing security by reducing false positives and promptly addressing true threats.

## Approach:
### 1. Data Exploration and Understanding:
- **Initial Inspection:** Load and inspect the dataset structure, including variable types and target class distribution.
- **EDA:** Use statistical summaries and visualizations to identify patterns, correlations, and potential class imbalances.

### 2. Data Preprocessing:
- **Handling Missing Data:** Apply strategies like imputation or removing affected rows.
- **Feature Engineering:** Create new features or modify existing ones (e.g., timestamps).
- **Encoding Categorical Variables:** Convert categorical data using techniques like one-hot or label encoding.

### 3. Data Splitting:
- **Train-Validation Split:** Split the training data into training and validation sets.
- **Stratification:** Ensure balanced class distribution across splits to handle class imbalances.

### 4. Model Selection and Training:
- **Baseline Model:** Start with a simple model like logistic regression for benchmarking.
- **Advanced Models:** Use models like Random Forest, XGBoost, or Neural Networks and tune hyperparameters.
- **Cross-Validation:** Use k-fold cross-validation to validate model performance.

### 5. Model Evaluation and Tuning:
- **Performance Metrics:** Focus on macro-F1 score, precision, and recall.
- **Class Imbalance:** Use techniques like SMOTE or class weighting to address imbalances.
- **Hyperparameter Tuning:** Optimize model performance through grid search or random search.

### 6. Model Interpretation:
- **Feature Importance:** Identify the most influential features using methods like SHAP or permutation importance.
- **Error Analysis:** Investigate misclassifications to improve the model.

### 7. Final Evaluation on Test Set:
- **Testing:** Evaluate the model on the test set and report macro-F1 score, precision, and recall.
- **Comparison to Baseline:** Ensure improvements over the baseline model.

### 8. Documentation and Reporting:
- **Documentation:** Provide a detailed report of the model development process.
- **Recommendations:** Suggest ways to integrate the model into SOC workflows and future improvements.

## Dataset Overview:
The dataset includes **45 features** across 1 million cybersecurity incidents. It consists of **evidence, alert, and incident-level data**, which provides a hierarchy of supporting information for each cybersecurity incident. The dataset is divided into **train.csv** (70%) and **test.csv** (30%) and stratified by incident severity and other key features.

### Key Features:
- **IncidentID, AlertID, OrgID**
- **Category, MitreTechniques**
- **IncidentGrade (Target)**: True Positive (TP), Benign Positive (BP), False Positive (FP)

## Project Deliverables:
- **Source Code:** Includes all steps from data preprocessing to model evaluation.
- **Trained Model:** A machine learning model ready for deployment.
- **Documentation:** A comprehensive report on the methodology, challenges, and findings.
- **Presentation:** A summary of project outcomes and business impact.

## Evaluation Metrics:
- **Macro-F1 Score:** Ensures balanced performance across all classes.
- **Precision:** Minimizes false positives.
- **Recall:** Ensures detection of true threats.

## Technical Tags:
- Machine Learning, Classification, Cybersecurity, Data Science, SOC, Model Evaluation, Feature Engineering, Threat Detection
