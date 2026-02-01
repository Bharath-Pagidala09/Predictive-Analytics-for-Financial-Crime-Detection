# Predictive Analytics for Financial Crime Detection

## Project Overview
This project focuses on applying predictive analytics techniques to detect and analyse financial crime and money laundering risks. The objective is to identify suspicious transaction patterns, classify transactions into risk categories, and analyse the relationship between transaction amounts and shell company involvement. The project supports Anti-Money Laundering (AML) efforts by providing data-driven insights for financial institutions and regulators.

---

## Objectives of the Study
The key objectives of this project are:
- To identify distinct patterns in financial transactions based on transaction amount, risk score, and involvement of shell companies and persons.
- To classify transactions into High Risk and Low Risk money laundering categories.
- To analyse the relationship between transaction amount and the number of shell companies involved using regression techniques.

---

## Dataset Description
The analysis uses the **Black Money Transaction dataset**, which contains:
- 4,509 transaction records
- Numerical, categorical, and binary variables

Key features include:
- Amount (USD)
- Money Laundering Risk Score (High / Low)
- Shell Companies Involved
- Persons Involved
- Transaction Type, Industry, Country, and Source of Money

---

## Data Preprocessing
Data preprocessing was carried out to ensure quality and usability:
- Removal of irrelevant columns such as Transaction ID, Destination Country, and Financial Institution
- Cleaning and standardisation of data formats
- Reduction of dataset size to essential variables
- Conversion of risk scores into categorical labels
- Ensuring consistency and readiness for analysis

---

## Exploratory Data Analysis
An exploratory analysis was performed using:
- Descriptive statistics
- Histograms and boxplots
- Correlation analysis

Key observations:
- Transaction amounts showed high variability but near-normal distribution
- No major outliers were detected
- Weak correlations were observed between numerical variables
- The dataset was suitable for further modelling without major transformations

---

## Clustering Analysis
Unsupervised learning techniques were applied to uncover hidden transaction patterns.

### K-Means Clustering
- Transactions were clustered based on Amount (USD), Shell Companies Involved, and Persons Involved
- Separate clustering was performed for High-Risk and Low-Risk transactions
- Optimal cluster selection was done using Silhouette Score and Davies-Bouldin Index
- Optimal clusters identified:
  - High Risk: k = 8
  - Low Risk: k = 9

Results showed clear transaction groupings, with high-risk clusters characterised by large transaction amounts and multiple shell companies.

### Hierarchical Clustering
- Agglomerative hierarchical clustering was used to explore nested transaction patterns
- Dendrograms were created to visualise cluster relationships
- Two-cluster and three-cluster solutions were identified
- The three-cluster solution aligned well with predefined risk categories

Hierarchical clustering provided deeper insights into transaction behaviour and supported the clustering results obtained from K-Means.

---

## Classification Analysis
Supervised learning models were developed to classify transactions into High Risk and Low Risk categories.

Models used:
- Logistic Regression
- Random Forest

Evaluation metrics:
- Accuracy
- Precision
- Recall
- F1 Score
- ROC-AUC

Results indicated that:
- Both models performed slightly better than random guessing
- Random Forest showed marginally better performance than Logistic Regression
- Overall classification performance was limited, indicating the need for further feature engineering, data balancing, and hyperparameter tuning

---

## Predictive Modelling (Regression)
Regression analysis was conducted to study the relationship between:
- Independent Variable: Amount (USD)
- Dependent Variable: Shell Companies Involved

Models applied:
- Linear Regression
- Polynomial Regression (Degree 2)

Findings:
- Both models showed very low R-squared values
- Polynomial regression did not significantly improve predictive performance
- The relationship between transaction amount and shell company involvement was weak

These results indicate the need for additional preprocessing and feature transformation for improved prediction.

---

## Conclusion
The study demonstrates that clustering techniques effectively identify suspicious transaction patterns associated with money laundering risk. Classification models showed limited predictive power, while regression models failed to capture meaningful relationships between transaction amount and shell company involvement. Despite these limitations, the analysis highlights the importance of transaction complexity in AML detection and provides valuable insights for improving financial crime monitoring systems.

---

## Note
The project report focuses on the key results relevant to the study objectives.

---

## Author
Bharath Pagidala

MSc Business Analytics

