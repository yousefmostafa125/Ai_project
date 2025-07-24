---

# Breast Cancer Wisconsin (Diagnostic) Dataset

This dataset contains features computed from a digitized image of a fine needle aspirate (FNA) of a breast mass. They describe characteristics of the cell nuclei present in the image and are used for diagnosing breast cancer.

## Dataset Overview

* **Rows:** 569 samples
* **Columns:** 32 attributes (including ID and diagnosis)
* **Target Variable:** `diagnosis`

  * `M` = Malignant
  * `B` = Benign

## Features

Each sample includes the following fields:

### Identification

* `id`: Unique identifier for each patient/sample
* `diagnosis`: Class label (M = malignant, B = benign)

### Feature Categories (Each with 3 versions: mean, SE, and worst)

1. **Radius**: Mean of distances from center to points on the perimeter
2. **Texture**: Standard deviation of gray-scale values
3. **Perimeter**
4. **Area**
5. **Smoothness**: Local variation in radius lengths
6. **Compactness**: (perimeter² / area - 1.0)
7. **Concavity**: Severity of concave portions of the contour
8. **Concave points**: Number of concave portions of the contour
9. **Symmetry**
10. **Fractal dimension**: "Coastline approximation" - 1

Each of these has:

* `*_mean`: Mean value
* `*_se`: Standard error
* `*_worst`: Worst (largest) value

### Example Feature Columns

* `radius_mean`, `radius_se`, `radius_worst`
* `texture_mean`, `texture_se`, `texture_worst`
* ...and so on for other feature types.

## Usage

This dataset is commonly used for:

* Binary classification tasks (malignant vs benign)
* Feature selection and dimensionality reduction
* Medical imaging model development and benchmarking

## Source

Original data source: UCI Machine Learning Repository
**Link**: [https://archive.ics.uci.edu/ml/datasets/Breast+Cancer+Wisconsin+(Diagnostic)](https://archive.ics.uci.edu/ml/datasets/Breast+Cancer+Wisconsin+%28Diagnostic%29)

---
