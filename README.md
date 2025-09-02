# 🩺 Disease Prediction Using Patient Data (Diabetes Dataset)

## 📌 Project Overview  
This project demonstrates how **Machine Learning** can be applied to predict diabetes using patient medical data.  
We cover the complete ML workflow — **data preprocessing, exploratory data analysis (EDA), model training, and evaluation** — to build a baseline predictive system.  

---

## 📊 Dataset  
- **Source:** [Pima Indians Diabetes Dataset (Kaggle)](https://www.kaggle.com/datasets/uciml/pima-indians-diabetes-database)  
- **Shape:** 768 rows × 9 columns  
- **Features:**  
  - Pregnancies  
  - Glucose  
  - BloodPressure  
  - SkinThickness  
  - Insulin  
  - BMI  
  - DiabetesPedigreeFunction  
  - Age  
- **Target Variable:** `Outcome`  
  - 0 → No Diabetes  
  - 1 → Diabetes  

⚠️ Note: Some medical values like *0 Glucose, 0 BMI, 0 BloodPressure* are unrealistic → handled as missing values and replaced with median.

---

## 🔧 Steps Performed  

### 1. Data Preprocessing  
- Filled missing/zero values with **median**.  
- Normalized all features using **MinMaxScaler (0–1 scaling)**.  
- Split dataset into **80% training** and **20% testing**.  

### 2. Exploratory Data Analysis (EDA)  
- Checked **target balance** → ~65% non-diabetic, ~35% diabetic.  
- **Correlation heatmap** showed Glucose, BMI, and Age as most predictive.  
- **Random Forest feature importance** also confirmed these factors.  

### 3. Model Training  
- **Logistic Regression** (baseline linear model).  
- **Random Forest Classifier** (non-linear ensemble).  

### 4. Evaluation  
- Logistic Regression: ~73% accuracy.  
- Random Forest: ~78–80% accuracy.  
- ROC-AUC ≈ 0.80 (reasonably good, but not perfect).  
- Confusion Matrix showed some **false negatives** (diabetes cases missed).  

---

## 📌 Insights  
- Glucose, BMI, and Age strongly influence diabetes prediction.  
- Dataset imbalance + unrealistic values reduce accuracy.  
- With better preprocessing & advanced models (XGBoost, LightGBM), accuracy can reach ~85%.  
- ML models can support **early diabetes risk detection**, but not replace real diagnostics.  

---

## 🚀 How to Run  

1. Clone repo / open notebook.  
2. Install dependencies:  
   ```bash
   pip install pandas numpy scikit-learn seaborn matplotlib imbalanced-learn
   ```
3.Place your dataset (diabetes.csv or diabetes.txt) in the project folder.

4.Run the notebook step by step:

Preprocessing

EDA

Model Training

Evaluation

### 📂 Project Structure
```bash
📁 Diabetes-Prediction
│── diabetes.csv              # dataset (or .txt version)
│── notebook.ipynb            # Jupyter Notebook with code
│── README.md                 # project documentation
│── results/                  # charts, confusion matrices, ROC curves
```

### ✅ Conclusion

This project illustrates how a simple ML pipeline can predict diabetes with ~75–80% accuracy using patient data.
It highlights the importance of data cleaning, feature scaling, and model comparison in healthcare AI projects.
