# Kaggle-Project
# Predicting Horse's Health 

This repository contains an attempt to apply **Random Forest** to predicting horse health outcomes using data from the [Kaggle "Predict Health Outcome" Challenge](https://www.kaggle.com/competitions/playground-series-s3e22/data?select=train.csv).

---

##  Abstract

The objective of this project is to use medical data to predict health outcomes for horses — specifically, whether they **survived**, were **euthanized**, or **died**. The dataset was obtained via Kaggle and underwent extensive preprocessing and cleaning.

A **Random Forest** machine learning model was selected due to its robustness to noise and its ability to handle non-linear relationships. Model performance was evaluated using **accuracy**, **precision**, **recall**, and **F1 score** across training, validation, and testing datasets.

The Random Forest model achieved an **accuracy of 81%**, showing promising results in predicting equine health outcomes.

---

##  Methods

### Data

- train.csv: 1235 samples × 29 features  
- test.csv: 824 samples × 28 features (no outcome column)

### Feature Types

- **Numerical**: rectal_temp, pulse, respiratory_rate, etc.
- **Categorical**: surgery, age, outcome, etc.

### Data Split

- 70% Training  
- 15% Validation  
- 15% Testing

###  Data Preprocessing

- Dropped irrelevant columns: id, hospital_num
- Filled missing categorical data with "missing"  
- No missing values in numerical columns
- Dropped lesion_3 and abdomo_protein after multicollinearity analysis
- Encoded categorical features for model compatibility

---

##  Exploratory Data Analysis (EDA)

- Plotted **bar graphs** for categorical features and **histograms** for numerical features
- Used **correlation heatmaps** to detect multicollinearity
- Visualized class distributions and feature relationships

---

##  Machine Learning Model: Random Forest

1. Split data into train, validation, and test sets
2. Implemented Random Forest classifier
3. Tuned hyperparameters using **Grid Search**
4. Evaluated model using:
   - Accuracy
   - Precision
   - Recall
   - F1-Score
   - AUC (Area Under Curve)
5. Analyzed feature importances (Top contributing features)

---

##  Results

- **Test Accuracy:** 81%  
- The Random Forest model effectively balanced bias and variance without overfitting.

---

##  Conclusion

- Random Forest proved to be an effective model for this problem
- Hyperparameter tuning improved model performance by approximately **10%**
- The model successfully captured important patterns in the dataset

---

##  Future Work

- Further investigate moderate correlations among features
- Explore relationships between **hospital IDs** and health outcomes for deeper insights
- Consider ensemble methods or other models for comparison

---
