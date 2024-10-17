# BAN6420-Mod5_Ass_PrincipalComponentAnalysis-SodiqOtunba
This is my submission for Assignment Module 5 PrincipalComponentAnalysis (PCA) - Sodiq Otunba Learner ID 154046

## Breast Cancer Data Analysis Using PCA and Logistic Regression
This project demonstrates the use of Principal Component Analysis (PCA) for dimensionality reduction on the Breast Cancer dataset from sklearn.datasets, followed by Logistic Regression for prediction.
## Introduction
The primary goal of this project is to identify essential variables for securing donor funding for Anderson Cancer Center. PCA has been applied to reduce the dimensionality of the dataset, making it easier to identify these key variables. Logistic Regression is then used for classification, predicting if a tumor is malignant or benign.

### Prerequisites
- Python 3.7+
- Required libraries:
- pandas
- numpy
- scikit-learn
- matplotlib
- seaborn

### Install Packages
```bash
pip install pandas numpy scikit-learn matplotlib seaborn
```
### Usage
Clone this repository to your local machine.
```bash
git clone https://github.com/Taryorh/BAN6420-Mod5_Ass_PrincipalComponentAnalysis-SodiqOtunba.git
```
## Feature Engineering
Feature Engineering includes:

 - Adding polynomial features using PolynomialFeatures from sklearn.preprocessing.
 - Selection of important features based on RandomForestClassifier using SelectFromModel.
## Dimensionality Reduction
- **PCA (Principal Component Analysis):** PCA reduces the number of dimensions while preserving 85% of the variance in the dataset. Two principal components were extracted from the dataset, which captures around 85.4% of the variance.

```python
pca = PCA(n_components=2)
pca_components = pca.fit_transform(scaled_data)
```
## Logistic Regression
Logistic Regression was implemented using the reduced PCA components as input features. 
```python
logistic = LogisticRegression()
logistic.fit(pca_components, target)
```
### Results
 - Before feature engineering, the Logistic Regression model achieved an accuracy of 97%.
 - After applying feature engineering and feature selection, the model's accuracy dropped to 83%, suggesting that further tuning is needed to improve feature selection and engineering.
