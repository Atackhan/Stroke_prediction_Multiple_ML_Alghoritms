---

# **Stroke Prediction using Machine Learning**

## **Overview**
This project aims to predict stroke occurrences using machine learning models based on patient health records. The dataset contains information such as age, hypertension, heart disease, average glucose level, BMI, and smoking status. Several classification models are implemented, including **Naive Bayes, Decision Tree, Random Forest, and Multi-Layer Perceptron (MLP)**.

---

## **Dataset**
The dataset consists of two CSV files:

- **train_2v.csv**: Contains labeled data used for training models.
- **test_2v.csv**: Contains unlabeled data for predictions.

### **Features**
| Column Name         | Description |
|---------------------|-------------|
| `id`               | Unique identifier for each patient |
| `gender`           | Patient's gender (Male/Female) |
| `age`              | Patient's age |
| `hypertension`     | 0 = No, 1 = Yes |
| `heart_disease`    | 0 = No, 1 = Yes |
| `ever_married`     | Marital status (Yes/No) |
| `work_type`        | Type of employment (Private, Self-employed, Govt_job, children, Never_worked) |
| `Residence_type`   | Urban or Rural |
| `avg_glucose_level`| Average glucose level |
| `bmi`              | Body Mass Index (BMI) |
| `smoking_status`   | Smoking history (never smoked, formerly smoked, smokes, NaN) |
| `stroke`           | Target variable (0 = No stroke, 1 = Stroke) |

---

## **Data Preprocessing**
1. **Handling Missing Data**:
   - `bmi` and `smoking_status` columns contain missing values.
   - Rows with missing values are dropped for simplicity.

2. **Exploratory Data Analysis (EDA)**:
   - **Distribution of stroke occurrences** is visualized using `sns.countplot()`.
   - **Gender vs Stroke** relationship is analyzed.

3. **Encoding Categorical Variables**:
   - `LabelEncoder()` is used to convert categorical features (`gender`, `ever_married`, `work_type`, `Residence_type`, `smoking_status`) into numerical values.

4. **Splitting the Data**:
   - `train_test_split()` is used to divide the data into training and validation sets.

---

## **Machine Learning Models**
### 1️⃣ **Naive Bayes**
- Uses **Gaussian Naive Bayes**.
- Accuracy: **97.45%**.
- However, **low recall and precision for stroke cases** due to imbalanced data.

### 2️⃣ **Decision Tree**
- Uses `DecisionTreeClassifier(max_depth=8)`.
- Accuracy: **97.9%**.
- Stroke detection performance is still poor.

### 3️⃣ **Random Forest**
- Uses `RandomForestClassifier(n_estimators=100)`.
- Accuracy: **98.2%**.
- However, it **fails to predict any stroke cases correctly**.

### 4️⃣ **Multi-Layer Perceptron (MLP)**
- Uses `MLPClassifier()`.
- Accuracy: **98.2%**.
- Similar issues with stroke detection.

---

## **Cross-Validation Results**
| Model | Accuracy (%) |
|--------|-------------|
| **Random Forest** | 98.1 |
| **Decision Tree** | 97.8 |
| **Naive Bayes** | 97.5 |
| **MLP** | 96.9 |

Even though the accuracy is high, the model struggles to predict stroke cases due to **data imbalance**.

---

## **Principal Component Analysis (PCA)**
- PCA is applied to reduce the number of features to **3 components**.
- Models are retrained using PCA-transformed data.
- Results:
  - **PCA Naive Bayes Accuracy**: 97.56%
  - **PCA Decision Tree Accuracy**: 96.31%
  - **PCA Random Forest Accuracy**: 98.14%
  - **PCA MLP Accuracy**: 98.14%

---

## **Challenges & Improvements**
✅ **Challenges:**
- **Severe class imbalance**: Only **1.26%** of patients in the dataset had a stroke.
- High accuracy **but poor performance in predicting strokes** (many false negatives).

💡 **Possible Improvements:**
- **SMOTE (Synthetic Minority Over-sampling Technique)** to balance the dataset.
- **Feature Engineering**: Creating new features from existing data.
- **Hyperparameter Tuning** to improve model generalization.
- **Ensemble Methods** to combine multiple models.

---

## **How to Run**
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/stroke-prediction.git
   cd stroke-prediction
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Run the Python script:
   ```bash
   python stroke_prediction.py
   ```

---

## **Author**
📌 **Atakan AKIN**  
