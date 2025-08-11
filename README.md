# Decision Tree & Random Forest Models with Visualization

## Overview
This project demonstrates implementation of Decision Tree and Random Forest algorithms for both classification and regression tasks using Scikit-learn.  
It also includes visualization of decision trees using Matplotlib.

## Dataset
- Airline flight dataset containing features like price, days left to departure, duration, and class.

## Features
- Data loading and preprocessing
- Training and evaluation of:
  - Decision Tree Classifier
  - Decision Tree Regressor
  - Random Forest Classifier
  - Random Forest Regressor
- Visualization of:
  - Single Decision Tree using Matplotlib
  - Feature importances from Random Forest

## Tools Used
- Python 3
- pandas
- scikit-learn
- matplotlib

## How to Run
1. Clone the repo or download the notebook/script.
2. Make sure you have the required packages installed:
   ```bash
   pip install pandas scikit-learn matplotlib
   Sample Code Snippets
Decision Tree Visualization
from sklearn import tree
import matplotlib.pyplot as plt

plt.figure(figsize=(20,10))
tree.plot_tree(dtc, feature_names=X.columns, class_names=['Economy', 'Business'], filled=True)
plt.show()
Random Forest Feature Importance
import matplotlib.pyplot as plt
import pandas as pd

feature_importances = pd.Series(rfr.feature_importances_, index=X_train_reg.columns)
feature_importances.sort_values().plot(kind='barh', color='teal')
plt.title("Random Forest Feature Importances")
plt.show()
