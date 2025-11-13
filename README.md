# NFHS Data Analysis and Predictive Modelling

This project presents a complete exploratory, statistical, and machine-learning analysis of the National Family Health Survey (NFHS) dataset for the years 2014–15 and 2019–20. The study explores behavioural health factors, women’s health indicators, chronic disease patterns, demographic characteristics, and their inter-relationships across districts in India.

## 1. Project Overview

This project aims to:

- Analyze major NFHS indicators across two survey cycles  
- Examine behavioural factors like tobacco and alcohol usage  
- Study women’s health indicators such as education, early marriage, anaemia, and teenage pregnancy  
- Investigate chronic diseases such as blood pressure and cancer  
- Perform correlation analysis and temporal comparison  
- Identify sign flips and major changes in relationships across years  
- Build regression, classification, and clustering models  
- Visualize state-wise and district-wise patterns  

## 2. Dataset Description

The dataset includes:

- Tobacco and alcohol consumption  
- Oral, cervical, and breast cancer rates  
- Blood pressure categories  
- Female schooling  
- Family planning indicators  
- Early marriage  
- Teenage pregnancy  
- Anaemia among women  
- Child population and malnutrition  
- State and district identifiers  
- NFHS Year (2014–15 or 2019–20)

Dataset used:
national-family-health-survey.csv

## 3. Data Preprocessing

Steps performed:

- Checked missing values (dataset is mostly complete)  
- Split dataset by NFHS year  
- Dropped district names  
- Encoded state names  
- Converted year into numeric  
- Selected numeric columns for analysis  

## 4. Exploratory Data Analysis

### 4.1 Correlation Analysis  
Correlation heatmaps were created for both NFHS years to compare:

- Tobacco and alcohol usage  
- Cancer prevalence  
- Blood pressure categories  
- Education indicators  
- Population structure  
- Sex ratio  

A separate correlation heatmap was created for Northeast India.

### 4.2 Strongest Correlations  
Top 15 strongest correlations were extracted, flattened, and interpreted.

### 4.3 State-Level Aggregation  
Computed state-wise averages for key indicators and created visual analyses such as:

- Tobacco vs oral cancer  
- Alcohol vs severe blood pressure  
- Female schooling vs oral cancer  

## 5. Temporal Comparison (2014–15 vs 2019–20)

- Correlations were compared year-wise  
- Delta correlation values were calculated  
- Sign flips were detected (cases where relationships reversed direction)  
- Identified indicators whose relationships changed significantly over time  

## 6. Regression Modelling

### 6.1 Simple Linear Regression  
Target: teenage pregnancy  
Predictor: early marriage  
The model shows early marriage explains ~45% of variation in teenage pregnancy.

### 6.2 Multiple Linear Regression  
Predictors include:

- Early marriage  
- Family planning  
- Child population  
- Anaemia  
- Child underweight  

R² improved from 0.447 to 0.587.

## 7. Cluster Analysis

### 7.1 Behavioural and Health Risk Clusters  
Clustering using:

- Tobacco  
- Alcohol  
- Cancer  
- Blood pressure  

Used KMeans and PCA for visualization.

### 7.2 Women Empowerment Clusters  
Clustered districts using:

- Female schooling  
- Early marriage  
- Teenage pregnancy  
- Anaemia  
- Contraceptive usage  

### 7.3 State-Level Clustering  
State-wise averaged indicators were used to form clusters.

## 8. Decision Tree Models

Two decision tree regressors were built:

1. Predict teenage pregnancy  
2. Predict child malnutrition  

Feature importance and full tree visualizations were generated.

## 9. Logistic Regression

A binary classifier was developed to predict high blood pressure risk among men, using behavioural and cancer-related features.

Evaluation included accuracy, confusion matrix, and classification report.

## 10. Random Forest Analysis

A Random Forest model was used to identify non-linear feature importance for predicting teenage pregnancy. Cross-validation was performed.

## 11. Visualizations

The project includes:

- Correlation heatmaps  
- Scatterplots  
- Bar charts  
- PCA plots  
- Cluster heatmaps  
- Decision tree diagrams  
- Feature importance graphs  

## 12. Summary of Findings

- Behavioural factors show strong clustering with disease outcomes  
- Early marriage is a major driver of teenage pregnancy  
- Education variables correlate with improved health outcomes  
- Several correlations changed significantly across NFHS cycles  
- ML models help understand and predict key health indicators  
