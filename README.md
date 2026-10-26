[Data-Analysis-on-Breast-Cancer-Prediction_README.md](https://github.com/user-attachments/files/33942062/Data-Analysis-on-Breast-Cancer-Prediction_README.md)
# Data Analysis on Breast Cancer Prediction

A Python machine learning project that classifies breast tumors as **malignant (M)** or **benign (B)** with a K-Nearest Neighbors (KNN) classifier. The best model reached about **97.9% accuracy** on the test set at **k = 11**.

Completed as the final project for a computing course at the University of Colorado Denver (May 2023).

## Dataset

- **File:** [`cancerdata.csv`](cancerdata.csv), 569 records (Breast Cancer Wisconsin Diagnostic dataset)
- **Target:** `diagnosis` (M = malignant, B = benign)
- **Features:** 30 real-valued features computed from digitized images of a fine needle aspirate (FNA) of a breast mass. Ten cell-nucleus measurements are each recorded as a mean, a standard error and a "worst" (largest) value:
  - Radius, texture, perimeter, area, smoothness
  - Compactness, concavity, concave points, symmetry, fractal dimension

## Workflow

1. **Load and inspect** the data: dimensions, data types and missing values
2. **Clean** by removing unneeded columns such as `id`
3. **Explore** with summary statistics and visualizations (Matplotlib and Seaborn)
4. **Encode** the diagnosis as numbers (M = 1, B = 0)
5. **Scale** features with `MinMaxScaler`
6. **Split** the data into training and test sets
7. **Train and tune KNN**, testing several values of K with distance weighting
8. **Evaluate** with accuracy, a confusion matrix, a classification report and an ROC curve

## Results

| Model | Best K | Test accuracy |
|---|---|---|
| KNN (distance-weighted) | 11 | ~97.9% |

## Tech stack

Python, Jupyter Notebook, pandas, NumPy, Matplotlib, Seaborn, scikit-learn

## How to run

```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
jupyter notebook "Breast Cancer Dataset.ipynb"
```

Keep `cancerdata.csv` in the same folder as the notebook.

## Repository contents

| File | Description |
|---|---|
| `Breast Cancer Dataset.ipynb` | Full analysis and KNN model |
| `cancerdata.csv` | Breast cancer dataset |
| `Detailed Executive Report.pdf` | Written report of the methodology and findings |

## Author

Sravan Tallam
