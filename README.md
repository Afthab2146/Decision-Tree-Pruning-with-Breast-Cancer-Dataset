# Decision-Tree-Pruning-with-Breast-Cancer-Dataset
Implementation of Decision Tree classification on the Breast Cancer dataset, comparing performance before and after cost-complexity pruning. Includes train/test accuracy, GridSearchCV tuning, and visualization of tree structures.

# Decision Tree Pruning with Breast Cancer Dataset

This project demonstrates **Decision Tree classification** on the popular **Breast Cancer dataset** using scikit-learn. The main focus is on **overfitting vs. generalization**, showcasing how **cost-complexity pruning** improves model performance.

---

## 📌 Project Workflow

1. **Dataset**
   - Breast Cancer dataset from `sklearn.datasets`.
   - Features scaled using `StandardScaler`.
   - Train/test split with stratification.

2. **Initial Decision Tree (No Pruning)**
   - A full tree (`ccp_alpha=0.0`) is trained.
   - Train and test accuracy compared.
   - The first 3 levels of the tree are visualized.

3. **Pruning with Cost-Complexity**
   - `GridSearchCV` applied with a parameter grid over:
     - `ccp_alpha` (pruning strength)
     - `max_depth` (depth control)
   - Cross-validation ensures robust parameter selection.
   - Accuracy before and after pruning is compared.

4. **Visualization**
   - Plot of **train vs test accuracy** across `ccp_alpha` values.
   - Comparison of **Decision Tree structures before and after pruning** (first 3 levels shown for clarity).

---

## 🔑 Key Concepts Covered
- **Overfitting in Decision Trees**: deep trees perform well on training data but poorly on test data.
- **Cost-Complexity Pruning**: controlled by `ccp_alpha`, prunes branches with little contribution to accuracy.
- **Hyperparameter Tuning with GridSearchCV**: optimizes pruning strength (`ccp_alpha`) and depth (`max_depth`).
- **Model Comparison**: accuracy before vs. after pruning on both train and test sets.

---

## 🛠️ Tech Stack
- Python 3.9+
- Scikit-learn
- NumPy
- Matplotlib

---

## 📊 Results
- **Before Pruning**: Tree is complex, higher training accuracy, lower test accuracy (overfitting).  
- **After Pruning**: Tree is simpler, slightly lower training accuracy but improved generalization with higher test accuracy.  
- Accuracy curves confirm the **bias–variance tradeoff**.  

---

