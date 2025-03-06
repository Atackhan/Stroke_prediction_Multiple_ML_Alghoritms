# 🏡 Costa Rican Household Poverty Level Prediction

This project aims to develop machine learning models to **classify the socioeconomic status of households in Costa Rica**. It includes data analysis, data cleaning, feature engineering, and modeling.

---

## 📁 Dataset

The dataset was obtained from the [Kaggle Costa Rican Household Poverty Level Prediction](https://www.kaggle.com/c/costa-rican-household-poverty-prediction) competition.

**Files:**
- `train.csv` (Training dataset)
- `codebook.csv` (Codebook with descriptions of each variable)

---

## 🔍 Libraries Used
- `pandas`
- `numpy`
- `matplotlib`
- `scikit-learn`

Installation:
```
pip install pandas numpy matplotlib scikit-learn
```

---

## 🛠️ Project Workflow

### 1. Data Loading and Initial Analysis
- Loading and inspecting the dataset.

### 2. Data Cleaning and Preprocessing
- Identification and imputation of missing values using median values.
- Conversion of categorical variables into numerical format.

### 3. Feature Engineering
Creation of new meaningful features such as:
- Rent per adult and per person
- Number of electronic appliances
- People per room and bedroom
- Demographic ratios (children, adults, elderly, etc.)

### 4. Machine Learning Modeling
- Splitting data into training and testing sets.
- Models used:
  - **Support Vector Machine (SVM)**
  - **Stochastic Gradient Descent (SGDClassifier)**

### 5. Model Evaluation
Models were evaluated using the following metrics:
- Accuracy
- Precision
- Recall
- F1 Score

---

## 📊 Model Results

| Model             | Accuracy | Precision | Recall | F1 Score |
|-------------------|----------|-----------|--------|----------|
| **SVM**           | 0.63     | 0.40      | 0.63   | 0.49     |
| **SGD Classifier**| 0.61     | 0.49      | 0.61   | 0.52     |

> ⚠️ **Note:** The performance of these models can be improved using advanced methods such as XGBoost, LightGBM, or hyperparameter tuning.

---

## 🚀 Future Improvements
- Implement advanced algorithms like XGBoost and LightGBM.
- Address class imbalance using SMOTE.
- Conduct hyperparameter optimization (GridSearchCV, RandomizedSearchCV).

---

## 📌 How to Use
1. Clone this repository:
```
git clone https://github.com/your-username/your-repo-name.git
```

2. Install required libraries:
```
pip install -r requirements.txt
```

3. Run the notebook:
```
jupyter notebook costa-rican.ipynb
```

---
