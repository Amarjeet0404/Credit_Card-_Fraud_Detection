# 💳 Credit Card Fraud Detection

---

## 📌 Problem Statement

Credit card fraud detection is a **major challenge** for financial institutions because:  

- **⚠ Highly Imbalanced Data:** Fraudulent transactions are extremely rare compared to legitimate ones.  
- **🔍 Feature Complexity:** Dataset contains both **numerical** and **categorical** features requiring careful preprocessing.  
- **⚡ Real-time Detection Requirements:** Must be **accurate, efficient, and scalable** for real-world usage.  

### 🎯 Objective  
Develop a **robust machine learning model** that:  
✔ Accurately identifies fraudulent transactions  
✔ Minimizes **false positives**  
✔ Handles **class imbalance** effectively  

---

## ✅ Proposed Solution

The system follows a **supervised machine learning pipeline** with these key stages:

---

### **1️⃣ Data Acquisition & Exploration**
- Loaded the credit card transaction dataset: **`train.csv`**  
- Performed **EDA**:  
  ✔ Data shape & summary statistics  
  ✔ Missing value checks  

---

### **2️⃣ Data Preprocessing & Feature Engineering**
- Converted **transaction timestamps** → datetime format and extracted **day of the week**  
- Calculated **customer age** from **DOB**  
- Removed **irrelevant columns** (IDs, non-informative fields)  
- Applied:  
  ✔ **Label Encoding** for categorical variables  
  ✔ **StandardScaler** for numerical feature scaling  

---

### **3️⃣ Handling Imbalanced Data**
Due to extreme class imbalance, multiple strategies were applied:  
✔ **Class Weight Balancing** in Logistic Regression  
✔ **Undersampling** (reduce majority class)  
✔ **Oversampling** using **Random Oversampling**  

---

### **4️⃣ Model Development & Training**
Implemented and compared **multiple classification models**:  
- **Logistic Regression (Vanilla)**  
- **Logistic Regression with Class Weights**  
- **Logistic Regression on Undersampled Data**  
- **Logistic Regression on Oversampled Data**  
- **Random Forest Classifier** (on resampled data)  

**Data Splitting:**  
- **Training**, **Validation**, and **Test sets** for unbiased evaluation  

---

### **5️⃣ Model Evaluation**
Models were evaluated using:  
✔ **Accuracy Score**  
✔ **Classification Report** (Precision, Recall, F1-score)  
✔ **Confusion Matrix**  

**Key Metric:**  
- Special focus on **Recall for fraud class** (detecting fraud is critical ✅)  

---

### **6️⃣ Insights & Observations**
📌 Models using **class balancing techniques** performed better.  
📌 **Random Forest** and **Balanced Logistic Regression** gave **most reliable results**.  
📌 Vanilla models struggled with detecting rare fraud cases.  

---

## 📊 Results Snapshot
| Model                                  | Precision | Recall | F1-Score |
|---------------------------------------|-----------|--------|----------|
| Logistic Regression (Vanilla)        | Low       | Very Low | Poor     |
| Logistic Regression (Balanced)       | Medium    | High   | Good     |
| Random Forest (Resampled Data)       | High      | High   | Excellent |

---

## 🛠 Tech Stack
- **Language:** Python 🐍  
- **Libraries:** pandas, numpy, scikit-learn, matplotlib, seaborn  

---

## 🚀 Future Improvements
✔ Implement **SMOTE** for better oversampling  
✔ Try **Gradient Boosting** & **XGBoost** for higher accuracy  
✔ Deploy as **Flask/FastAPI API** for real-time fraud detection  

---

⭐ **If you found this project useful, don't forget to give it a STAR!** ⭐
