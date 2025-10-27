# US Visa Approval Prediction

## Project Overview
This project aims to predict the outcomes of US visa applications (Certified or Denied) using machine learning. With the growing number of applications handled by the Office of Foreign Labor Certification (OFLC), automating the classification process can help reduce manual effort, speed up decision-making, and maintain accuracy in approvals.

The solution leverages structured data on applicants and employers to identify key factors influencing visa approval decisions.

---

## Dataset
The dataset contains 25,480 visa applications with features describing both the **employee** and the **employer**:

- `case_id`: Unique ID for each application  
- `continent`: Continent of the employee  
- `education_of_employee`: Employee's education level  
- `has_job_experience`: Whether the employee has prior experience (`Y`/`N`)  
- `requires_job_training`: Whether job training is required (`Y`/`N`)  
- `no_of_employees`: Number of employees in the employer's company  
- `yr_of_estab`: Year the company was established  
- `region_of_employment`: Intended US region of employment  
- `prevailing_wage`: Average wage for the position  
- `unit_of_wage`: Hourly, Weekly, Monthly, or Yearly  
- `full_time_position`: Full-time (`Y`) or part-time (`N`)  
- `case_status`: Target variable (`Certified`/`Denied`)  

---

## Models Used
The following machine learning models were implemented and tuned:

1. **Decision Tree Classifier**  
2. **Bagging Classifier** (with Decision Tree base estimator)  
3. **Random Forest Classifier**  
4. **AdaBoost Classifier**  
5. **Gradient Boosting Classifier**  
6. **Stacking Classifier** (with AdaBoost, Gradient Boosting, and Random Forest as base estimators)  

All models were evaluated using **F1-score**, **accuracy**, and **confusion matrices** to ensure balanced performance for both certified and denied applications.

---

## Key Steps
1. **Data Preprocessing:**  
   - Handled negative and missing values  
   - Encoded categorical variables using one-hot encoding  
   - Split data into training (70%) and test (30%) sets  

2. **Exploratory Data Analysis (EDA):**  
   - Univariate and bivariate analysis  
   - Identified patterns in visa approvals by region, education, experience, and wage  

3. **Model Training & Hyperparameter Tuning:**  
   - Trained Decision Tree, Bagging, Random Forest, AdaBoost, Gradient Boosting, and Stacking classifiers  
   - Used GridSearchCV for hyperparameter tuning  

4. **Model Evaluation:**  
   - Evaluated performance on training and test sets  
   - Stacking classifier achieved the best overall performance  

---

## Key Findings
- **Top Features Influencing Visa Approval:**  
  - Education level of the employee  
  - Job experience  
  - Prevailing wage  
  - Region of employment  
  - Full-time vs part-time position  

- **Impact:**  
  - Automates visa classification, reducing manual review workload  
  - Helps OFLC make faster, data-driven decisions  
