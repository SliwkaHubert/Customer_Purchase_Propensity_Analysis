# Customer Purchase Propensity Analysis

## Project Overview

The goal of this project is to analyze user behavior data from an online store and build predictive models to determine the likelihood of a user making a purchase. The project covers the full pipeline—from exploratory data analysis (EDA), through data preprocessing, to model building and hyperparameter optimization.

## Exploratory Data Analysis (EDA)

- The dataset is clean—no duplicates or missing values.
- Key features strongly correlated with the target include: `sign_in`, `saw_checkout`, and `checked_delivery_detail`.
- Most features are imbalanced with respect to the target variable, except for `returning_user`, which is relatively balanced.
- Most users come from the UK and make purchases using mobile devices.
- Data was prepared using One Hot Encoding.

## Model Building and Evaluation

Several classification models were trained and evaluated:

- **Random Forest**
- **K-Nearest Neighbors (KNN)**
- **Naive Bayes**

### Key Findings:

- All models showed high Accuracy, Precision, and Recall scores.
- The Naive Bayes model produced more false positives (users who were classified as buying but did not).
- The KNN model produced more false negatives (users who were misclassified as not buying), with FN: 286.
- The Random Forest model was selected for further hyperparameter tuning.

## Model Optimization

The Random Forest model was optimized to:

- Reduce the number of false negatives.
- Improve the model’s ability to correctly identify users who will make a purchase.

## Requirements

To run the notebook, you’ll need Python 3 and the following libraries:

- pandas  
- numpy  
- scikit-learn  
- matplotlib / seaborn (optional, for visualization)

## How to Run

1. Clone the repository or download the `.ipynb` file.
2. Ensure all required libraries are installed.
3. Open and run `customer_propensity_final.ipynb` in Jupyter Notebook or JupyterLab.


This project analyzes customer behavior in the e-commerce domain and can serve as a foundation for building a scoring model to support marketing campaigns.
