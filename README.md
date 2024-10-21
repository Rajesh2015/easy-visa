# Easy Visa (Visa Application Analysis and Classification)
https://www.kaggle.com/code/mariyamalshatta/easy-visa-ensemble-techniques

## Overview

This project focuses on analyzing and predicting visa application outcomes using machine learning. The Office of Foreign Labor Certification (OFLC) processes thousands of applications for employers seeking to bring foreign workers into the U.S. every year. As the number of applications increases, it becomes increasingly tedious to manually review all cases.

This project aims to:

- Facilitate the process of visa approvals using a machine learning classification model.
- Recommend a suitable profile for applicants based on the significant factors that influence visa approval or denial.

## Objective

In FY 2016, the OFLC processed 775,979 employer applications for 1,699,957 positions, a 9% increase from the previous year. Given this increasing number of applications, the goal of this project is to develop a **Machine Learning** solution that helps predict visa certification outcomes and shortlists candidates with a higher likelihood of approval. 

## Dataset Description

The dataset contains attributes related to both the employee (foreign worker) and the employer. Below are key columns in the data:

- **case_id**: ID of each visa application.
- **continent**: Continent of the employee.
- **education_of_employee**: Employee's education level.
- **has_job_experience**: Indicates if the employee has previous job experience (Y/N).
- **requires_job_training**: Indicates if job training is required (Y/N).
- **no_of_employees**: Number of employees in the employer's company.
- **yr_of_estab**: Year the employer's company was established.
- **region_of_employment**: U.S. region where the foreign worker is employed.
- **prevailing_wage**: Average wage paid to similarly employed workers in the occupation area.
- **unit_of_wage**: Wage unit (Hourly, Weekly, Monthly, Yearly).
- **full_time_position**: Whether the position is full-time (Y/N).
- **case_status**: Visa certification status (Certified/Denied).

## Exploratory Data Analysis (EDA) Questions

The EDA seeks to answer key questions that will help us understand the drivers of visa certification:

1. **Education and Certification**: Does education level impact visa certification?
2. **Continent and Visa Status**: How does visa certification vary across different continents?
3. **Work Experience**: Does having job experience influence visa approval?
4. **Wage Unit**: Which wage unit (Hourly, Weekly, Monthly, Yearly) is most likely to lead to visa certification?
5. **Prevailing Wage**: How does visa status change with different levels of prevailing wage?

## Project Structure

- `data/`: Contains the raw dataset for visa applications.
- `notebooks/`: Jupyter notebooks used for data exploration, analysis, and modeling.
- `scripts/`: Python scripts for data preprocessing, feature engineering, and model training.
- `models/`: Directory to store trained models.
- `README.md`: Project documentation (this file).

## Machine Learning Approach

The classification model is designed to predict whether a visa application will be **certified** or **denied**. The following steps are taken:

1. **Data Preprocessing**: Cleaning the data, handling missing values, encoding categorical variables, and scaling numerical features.
2. **Feature Engineering**: Creating new features based on domain knowledge, such as grouping wage units or calculating the company's age.
3. **Model Selection**: Evaluating different classification models like Logistic Regression, Decision Trees, Random Forests, and Gradient Boosting Machines.
4. **Model Evaluation**: Using metrics such as accuracy, precision, recall, F1-score, and ROC-AUC to assess model performance.