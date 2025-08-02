# AI Breast Cancer Diagnosis Project

This project leverages the **Breast Cancer Wisconsin (Diagnostic) Dataset** to develop a machine learning model capable of distinguishing between **malignant** and **benign** tumors based on features extracted from cell nuclei in fine needle aspirate (FNA) images.

---

## 📊 Dataset Overview

- **Source**: [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/Breast+Cancer+Wisconsin+%28Diagnostic%29)  
- **Total Samples**: 569  
- **Total Features**: 30 numerical features (+ ID and diagnosis)  
- **Target Variable**: `diagnosis`  
  - `M`: Malignant  
  - `B`: Benign  

---

## 🧬 Feature Description

Each record contains measurements computed from FNA images, organized into 10 primary categories — each with **mean**, **standard error (`_se`)**, and **worst-case (`_worst`)** variants:

| Feature     | Description |
|-------------|-------------|
| Radius      | Distance from center to edge |
| Texture     | Variation in gray-scale intensity |
| Perimeter   | Total length around the cell |
| Area        | Size of the cell |
| Smoothness  | Local variation in radius |
| Compactness          | `(perimeter² / area - 1.0)` |
| Concavity         | Depth of concave portions |
| Concave Points    | Count of concave portions |
| Symmetry    | Symmetry of the cell shape |
| Fractal Dimension    | "Roughness" of the boundary |

> Example features: `radius_mean`, `texture_worst`, `concavity_se`, etc.

---

## 🧠 Project Workflow

1. **Data Preprocessing**  
   - Removed outliers using IQR  
   - Label encoded target classes  
   - Scaled features (if necessary)

2. **Modeling**  
   - Trained various classifiers (e.g., Random Forest, Logistic Regression)
   - Feature importance visualized using tree-based models

3. **Evaluation Metrics**  
   - Confusion Matrix  
   - Accuracy, Precision, Recall, F1-Score  
   - Mean Squared Error (for regression testing)

---

## 📈 Example Results

| Metric     | Value |
|------------|-------|
| Accuracy   | 0.91  |
| Precision  | 0.00  |
| Recall     | 0.00  |
| F1 Score   | 0.00 |

> Note: Results may vary based on model choice and feature selection.

---

## 📌 Key Findings

- `concave_points_worst`, `area_worst`, and `concavity_mean` were among the **most predictive features**
- Models achieved **high accuracy** using even a subset of features
- DecisionTree performed well despite dataset imbalance

---

## 🚀 Future Improvements

- Add cross-validation and hyperparameter tuning  
- Try ensemble methods like XGBoost  
- Apply SMOTE or other techniques to balance the dataset  
- Deploy as an interactive web app (e.g., with Streamlit)

---

## 📂 File Structure

```
├── data.csv              # Cleaned dataset
├── python_code.ipynb     # Jupyter notebook with full analysis
├── README.md             # Project documentation
```

---

## 🔗 References

- [UCI Dataset Page](https://archive.ics.uci.edu/ml/datasets/Breast+Cancer+Wisconsin+%28Diagnostic%29)
- [scikit-learn Documentation](https://scikit-learn.org/)
