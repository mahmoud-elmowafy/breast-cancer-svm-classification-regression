# Breast Cancer Classification & Regression using SVM

## 📌 Project Overview

This project applies Support Vector Machines (SVM) to the Breast Cancer Wisconsin dataset, covering two Machine Learning tasks:

- **Classification:** Predicting whether a tumor is Benign or Malignant using Support Vector Classification (SVC).
- **Regression:** Predicting the `radius_mean` feature using Support Vector Regression (SVR).

The project also includes hyperparameter optimization using GridSearchCV to improve classification performance.

## 📊 Dataset Information

- **Dataset:** Breast Cancer Dataset
- **Source:** [Kaggle - Breast Cancer Dataset](https://www.kaggle.com/datasets/wasiqaliyasir/breast-cancer-dataset)
- **Original Shape:** 569 rows × 33 columns
- **Cleaned Shape:** 569 rows × 31 columns
- **Benign Cases:** 357
- **Malignant Cases:** 212
- **Missing Values After Cleaning:** 0
- **Duplicate Rows:** 0

## 🛠️ Data Preprocessing

1. Loaded the dataset using Pandas.
2. Inspected dataset structure and statistical information.
3. Removed unnecessary columns (`id` and `Unnamed: 32`).
4. Checked missing values and duplicate records.
5. Encoded the target variable:
   - Benign (B) → 0
   - Malignant (M) → 1
6. Split the data into training and testing sets (80/20).
7. Applied StandardScaler to numerical features.

## 📈 Exploratory Data Analysis (EDA)

The project includes:
- Diagnosis distribution visualization.
- Radius Mean comparison using boxplots.
- Feature correlation heatmap.
- Statistical analysis of numerical features.

## 🤖 Machine Learning Models

### 1. Support Vector Classification (SVC)

- Kernel: RBF
- C: 1.0
- Gamma: Scale
- Train/Test Split: 80/20
- Random State: 42
- Stratified splitting.

### Classification Results

| Metric | Score |
|---|---:|
| Accuracy | 97.37% |
| Precision | 100% |
| Recall | 92.86% |
| F1 Score | 96.30% |

### 2. Support Vector Regression (SVR)

SVR was used to predict the `radius_mean` feature based on the remaining numerical features.

- Kernel: RBF
- C: 1.0
- Epsilon: 0.1
- Gamma: Scale

### Regression Results

| Metric | Score |
|---|---:|
| MAE | 0.5090 |
| MSE | 1.0730 |
| RMSE | 1.0358 |
| R² Score | 0.9112 |

## ⚙️ Hyperparameter Tuning

GridSearchCV was used to optimize the SVC model.

**Search Configuration:**
- Cross-Validation: 5-Fold
- Scoring Metric: Recall
- Kernels: RBF and Linear
- C: [0.1, 1, 10, 100]
- Gamma: ['scale', 0.01, 0.001, 0.0001]

**Best Parameters:**
- C: 10
- Kernel: RBF
- Gamma: Scale

**Best Cross-Validation Recall:** 95.88%

### Tuned Model Results

- Test Accuracy: 97.37%
- Malignant Recall: 92.86%

## 📚 Technologies & Libraries

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Google Colab

## 📁 Project Structure

```text
breast-cancer-svm-classification-regression/
│
├── breast_cancer_svm.ipynb
├── README.md
├── requirements.txt
└── .gitignore
```

## ▶️ How to Run

1. Clone the repository.
2. Open the notebook using Google Colab or Jupyter Notebook.
3. Install the required libraries.
4. Run the notebook cells sequentially.

## 👨‍💻 Author

**Mahmoud Elmowafy**

Machine Learning & Data Analysis Projects.

---

*Disclaimer: This project is for educational purposes only and is not intended for medical diagnosis.*
