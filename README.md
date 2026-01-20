# Credit Card Fraud Detection: Sampling Technique Analysis

## 📌 Objective

The objective of this assignment is to study the impact of **different sampling techniques** on the performance of **various machine learning models** using an imbalanced credit card fraud dataset.

---

## 📁 Dataset

Dataset Source (as provided in the assignment):  
https://github.com/AnjulaMehto/Sampling_Assignment/blob/main/Creditcard_data.csv  

- The dataset contains credit card transaction records.
- Target column: `Class`
  - `0` → Normal transaction  
  - `1` → Fraud transaction  
- The dataset is highly imbalanced.

## ⚙️ Methodology

The following steps were followed in this project:

1. The dataset was loaded and basic preprocessing was performed.
2. The data was split into training and testing sets using stratified sampling to preserve class distribution.
3. Feature scaling was applied using standard normalization.
4. The training data was balanced using five different sampling techniques.
5. Five different machine learning models were trained on each sampled dataset.
6. The models were evaluated using accuracy score.
7. The results were recorded in a comparison table and visualized using a graph.

---
## 🔁 Sampling Techniques Used

The following five sampling techniques were used:

1. Random Under Sampling  
2. Random Over Sampling  
3. SMOTE (Synthetic Minority Over-sampling Technique)  
4. NearMiss  
5. SMOTEENN (Combination of SMOTE and Edited Nearest Neighbors)  

These techniques are implemented using the imbalanced-learn library.

---
## 🤖 Machine Learning Models Used

The following five machine learning models were used:

1. Logistic Regression  
2. Decision Tree Classifier  
3. Random Forest Classifier  
4. K-Nearest Neighbors (KNN)  
5. Support Vector Machine (SVM)  

---
## 📋 Result Table (Accuracy %)

| Model ↓ / Sampling → | Random Under | Random Over | SMOTE | NearMiss | SMOTEENN |
|----------------------|--------------|-------------|--------|-----------|-----------|
| Logistic Regression | 66.67 | 91.70 | 92.58 | 50.00 | 96.24 |
| Decision Tree | 66.67 | 98.47 | 98.25 | 16.67 | 98.55 |
| Random Forest | 66.67 | 99.78 | 98.91 | 16.67 | 99.71 |
| K-Nearest Neighbors | 16.67 | 98.47 | 89.08 | 83.33 | 94.22 |
| Support Vector Machine | 16.67 | 68.56 | 72.93 | 16.67 | 69.65 |

---
## 🧠 Analysis and Discussion

From the result table, the following observations can be made:

- Sampling1 gives poor performance for most models, especially M4 and M5.
- Sampling4 performs very poorly for most models except M4.
- Sampling2, Sampling3, and Sampling5 give consistently high accuracy for almost all models.
- Model M3 achieves the highest accuracy of 99.78% with Sampling2 and 99.71% with Sampling5.
- Model M2 and M3 perform extremely well with Sampling2, Sampling3, and Sampling5.
- Model M5 is the weakest model overall but still performs better with Sampling3 and Sampling5.
---
## 🏆 Conclusion

From the experimental results, it is clear that different sampling techniques have a significant impact on model performance.

- Sampling2 and Sampling5 are the best performing sampling techniques overall.
- Sampling3 also gives consistently strong results across most models.
- Sampling1 and Sampling4 perform poorly and are not suitable for this dataset.
- Model M3 is the best performing model overall, achieving the highest accuracy.
- Model M2 also shows excellent and stable performance across good sampling techniques.

Therefore, this experiment proves that selecting the correct sampling technique is extremely important when working with highly imbalanced datasets, and Sampling2 and Sampling5 are the most effective choices for this problem.
---
