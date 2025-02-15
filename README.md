# BFSI Loan Application Analysis

This project analyzes loan application data from a Banking, Financial Services, and Insurance (BFSI) domain to understand patterns and trends in loan defaults, customer behavior, and various demographic factors. It involves Exploratory Data Analysis (EDA), feature engineering, and predictive modeling to predict potential loan defaulters.

---

## Table of Contents
- [Project Overview](#project-overview)
- [Datasets](#datasets)
- [Objective](#objective)
- [Analysis and Insights](#analysis-and-insights)
  - [Univariate Analysis](#univariate-analysis)
  - [Bivariate Analysis](#bivariate-analysis)
  - [Multivariate Analysis](#multivariate-analysis)
- [Predictive Modeling](#predictive-modeling)
- [Technologies Used](#technologies-used)
- [Installation](#installation)
- [Usage](#usage)
- [Results and Insights](#results-and-insights)
- [Contributing](#contributing)
- [License](#license)

---

## Project Overview
The BFSI Loan Application Analysis project involves analyzing two datasets:
- **Application Data:** Contains information about current loan applications, including loan ID, contract type, applicant demographics, income level, credit amount, real estate ownership, and the target variable indicating potential default.
- **Previous Application Data:** Contains details of all previous home loan applications, including contract status, payment method, portfolio type, and yield type.

The project aims to:
- Explore demographic trends and loan application behaviors.
- Identify key factors influencing loan defaults.
- Build predictive models to classify potential defaulters.

---

## Datasets
1. **Application Data:**
   - **Rows:** 3,07,511
   - **Columns:** 122
   - **Primary Key:** `SK_ID_CURR`
   - **Target Variable:** `TARGET` (0 - Non-Defaulter, 1 - Defaulter)
   - **Details:** Loan details, applicant demographics, income levels, property ownership, and document submissions.

2. **Previous Application Data:**
   - **Rows:** 16,70,214
   - **Columns:** 37
   - **Primary Key:** `SK_ID_PREV`
   - **Details:** Historical loan application data, including contract type, credit amount, approval status, payment methods, and yield groups.

---

## Objective
- To understand loan application patterns and default rates.
- To analyze the relationship between demographic attributes and loan default behavior.
- To build a predictive model to classify potential loan defaulters.

---

## Analysis and Insights

### Univariate Analysis
- **Gender Distribution:** Significantly higher representation of female applicants (~66%) compared to males (~34%).
- **Occupation Type:** Higher default rates observed in lower-skilled occupations.
- **Income Type:** Different income types show varied default rates, with Unemployed applicants having the highest default rate.

### Bivariate Analysis
- **Gender vs. Default Rate:** Females show a lower default rate (7%) compared to males (11%).
- **Contract Type vs. Default Rate:** Cash loans are more prevalent across all demographics, but Revolving loans have a slightly higher default rate.
- **Housing Type vs. Default Rate:** Renters and those living with parents have higher default rates, indicating financial vulnerability.

### Multivariate Analysis
- **Correlation Analysis:** Investigated correlations between external sources and default rates.
- **Default Rate by Income Type and Gender:** Analyzed default trends across different income types segmented by gender.

---

## Predictive Modeling
- Created a balanced dataset using resampling techniques to handle class imbalance (Target 0: 91.93%, Target 1: 8.07%).
- Built and evaluated multiple models, including:
  - Logistic Regression
  - Random Forest Classifier
  - Gradient Boosting
- Performance metrics include Accuracy, Precision, Recall, F1-Score, and ROC-AUC.

---

## Technologies Used
- **Programming Language:** Python
- **Libraries Used:**
  - `Pandas`, `NumPy` for data manipulation and analysis.
  - `Matplotlib`, `Seaborn` for data visualization.
  - `scikit-learn` for predictive modeling.
- **Tools:** Jupyter Notebook, GitHub for version control.
  
---

## Usage
1. Place the datasets (`application_data.csv` and `previous_application.csv`) in the project directory.
2. Run the analysis scripts in Jupyter Notebook:
    ```bash
    jupyter notebook
    ```
3. Execute the notebooks in sequence to:
   - Perform Exploratory Data Analysis (EDA)
   - Conduct Feature Engineering
   - Build and evaluate predictive models

---

## Results and Insights
- **Default Rates:** Higher default rates observed among male applicants, renters, and those in lower-skilled occupations.
- **Predictive Model Performance:** 
  - Random Forest Classifier achieved the highest accuracy and F1-Score.
  - Logistic Regression provided valuable interpretability of influential features.
- **Key Features Influencing Default:** Credit amount, income type, occupation type, and housing type were among the top predictors of default risk.

---
