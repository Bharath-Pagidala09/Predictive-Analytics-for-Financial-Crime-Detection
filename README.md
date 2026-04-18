# Predictive Analytics for Financial Crime Detection

## Overview
This project investigates financial crime and money laundering using 
a data-driven approach. Using the Black Money Transaction dataset 
(4,509 transactions), multiple machine learning models were built and 
evaluated to detect suspicious financial behaviour, classify risk levels, 
and predict relationships between transaction features.

---

## What Was Done

### 1. Data Preprocessing
The original dataset had 10,000 rows and 14 columns. It was cleaned down 
to 4,509 rows and 9 columns by removing irrelevant columns like 
Transaction ID and Destination Country. Missing values were handled, 
formats were standardised, and the Money Laundering Risk Score was 
converted into categories (High/Low) to make it suitable for analysis.

---

### 2. Exploratory Data Analysis
Descriptive statistics revealed that the average transaction amount was 
$2.5 million USD, with an average of 4.5 shell companies involved per 
transaction. Histograms showed near-normal distributions across all 
numerical variables, and boxplots confirmed no significant outliers 
between high and low risk groups.

---

### 3. Clustering
Two clustering methods were used to find hidden patterns in the data:

- **K-Means:** Cluster values from K=2 to K=11 were tested and the best 
  K was selected using the Davies-Bouldin Score and Silhouette Score. 
  The optimal K was 8 for high-risk and 8 for low-risk transactions. 
  Results showed clear groupings where high-risk clusters had large 
  transaction amounts and many shell companies involved.

- **Hierarchical Clustering:** Using agglomerative clustering and 
  dendrograms, a 2-cluster solution was found for high-risk and a 
  3-cluster solution for low-risk data, which better matched the 
  High/Medium/Low risk classification.

---

### 4. Classification
Two models were trained to classify transactions as High or Low risk:

- **Logistic Regression:** Accuracy 50.78%, F1 Score 50.43%, AUC 0.5269
- **Random Forest:** Accuracy 52.55%, F1 Score 52.36%, AUC 0.5269

Both models performed only slightly better than random guessing. 
This suggests the dataset needs further feature engineering, 
balancing using techniques like SMOTE, and hyperparameter tuning 
to improve performance.

---

### 5. Regression
The relationship between transaction amount (USD) and the number of 
shell companies involved was investigated:

- **Linear Regression:** R-Squared = 0.0009 — very weak fit
- **Polynomial Regression (Degree 2):** R-Squared = 0.0014 — 
  slightly better but still poor

These results show that transaction amount alone is not a strong 
predictor of shell company involvement, and more variables or 
data transformation are needed.

---

## Key Takeaway
Clustering was the most effective technique in this project, 
successfully identifying high-risk transaction patterns. 
Classification and regression models struggled due to the 
nature of the dataset, highlighting the need for richer 
features and better data quality in future work.

---

## Tools Used
- **Python** — clustering, classification, regression modelling
- **Excel / Power Pivot** — data cleaning and preprocessing
