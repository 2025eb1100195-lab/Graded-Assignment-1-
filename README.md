# Graded-Assignment-1-

##  Overview
This project focuses on predicting hotel booking cancellations using the Hotel Bookings dataset.  
The main objective is not just model building, but demonstrating how **feature engineering, preprocessing, and proper pipelines improve model performance, stability, and interpretability**.

---

##  Objective
- Predict **is_canceled (binary classification)**
- Show the impact of:
  - Feature engineering
  - Scaling and preprocessing
  - Feature selection
  - Distance-based learning (KNN)

---

## ⚙️ Tools & Libraries
- Python  
- pandas  
- numpy  
- scikit-learn  
- matplotlib / seaborn  

---

## 🚀 How to Run

### Option 1: Google Colab (Recommended)
- Open the notebook using the Colab link  
- Run all cells sequentially

---


---

## 🧠 Key Steps Implemented

### ✔ Task 1: Baseline Model
- Minimal preprocessing (imputation + encoding)
- KNN classifier used
- Established initial benchmark performance

---

### ✔ Task 2: Curse of Dimensionality
- Generated synthetic datasets with increasing features
- Observed that distance differences shrink in high dimensions
- Demonstrated why feature selection is important

---

### ✔ Task 3: Numeric Preprocessing
- Applied:
  - Binning
  - Binarization
  - Scaling (Standard, MinMax, Robust)
- Compared distributions and summary statistics

---

### ✔ Task 4: Distance Metrics & Scaling
- Used KNN with:
  - No scaling
  - StandardScaler
  - RobustScaler
- Compared Euclidean and Manhattan distance

**Key insight:** Scaling significantly improves performance in distance-based models

---

### ✔ Task 5: End-to-End Pipeline
- Built using:
  - ColumnTransformer
  - Pipeline
- Includes:
  - Imputation
  - Scaling
  - Model
- Evaluated using **5-fold cross-validation**

---

### ✔ Task 6: Feature Extraction
- Extracted meaningful features:
  - total_guests
  - total_nights
- Encoded categorical features using OneHotEncoder

---

### ✔ Task 7: Feature Construction

Constructed features include:

- **Ratio features**
  - price_per_person  
  - requests_per_night  

- **Interaction features**
  - adr_lead_interaction  
  - guests_nights_interaction  

- **Aggregated features**
  - avg_adr_by_country  
  - avg_lead_by_hotel  

- **Polynomial features**
  - adr_squared  
  - adr_lead_poly  

---

### ⚠️ Avoiding Data Leakage
- Aggregated features initially computed on full dataset (risk)
- Proper approach: compute using training data only
- Pipeline ensures safe preprocessing (no leakage in scaling/encoding)

---

### ✔ Task 8: Feature Importance & Selection

**Feature Importance Methods:**
- Random Forest
- Mutual Information
- Permutation Importance

**Feature Selection Techniques:**
- Correlation filtering (>0.85 removed)
- Chi-square test
- Mutual Information ranking

**Final Feature Set:** Top 20 features selected based on consistency across methods

---

## 📊 Results Summary

| Stage | Performance |
|------|------------|
| Baseline | Moderate |
| After preprocessing | Improved |
| After feature engineering | Significant improvement |
| After feature selection | Optimized |

---

## 💡 Key Insights
- Feature engineering had the **largest impact on performance**
- Scaling is essential for KNN and distance-based models
- Important features include:
  - lead_time  
  - adr  
  - total_nights  
- Feature selection improves efficiency without reducing accuracy

---

## 📎 Submission Links
- 📘 **Colab Notebook:** [PASTE YOUR LINK HERE]  
- 📂 **GitHub Repository:** [PASTE YOUR LINK HERE]  

---

## 🏁 Conclusion
This project demonstrates that **well-engineered features and proper preprocessing are more impactful than complex models**, especially in real-world business problems like cancellation prediction.

---

## 👩‍💻 Author
**Anya Sharma**
