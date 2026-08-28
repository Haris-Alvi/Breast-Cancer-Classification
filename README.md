# Breast Cancer Classification Using Machine Learning

A machine learning classification project comparing three supervised learning algorithms for breast cancer detection: **Logistic Regression, K-Nearest Neighbors (KNN), and Support Vector Machine (SVM)**.

The models are trained and evaluated on the **Breast Cancer Wisconsin (Diagnostic) Dataset** to classify tumors as **malignant or benign**.

## Project Overview

Early and accurate classification of breast tumors is an important application of machine learning in healthcare.

This project investigates how different machine learning algorithms perform on the same medical dataset and compares their classification performance.

Three algorithms were implemented:

* Logistic Regression
* K-Nearest Neighbors (KNN)
* Support Vector Machine (SVM)

Each model was evaluated using classification metrics including accuracy, classification reports, and confusion matrices.

## Dataset

The project uses the **Breast Cancer Wisconsin (Diagnostic) Dataset**.

### Dataset Characteristics

| Property        | Value |
| --------------- | ----: |
| Total Samples   |   569 |
| Total Features  |    30 |
| Malignant Cases |   212 |
| Benign Cases    |   357 |

The features represent morphological characteristics of cell nuclei obtained from fine needle aspirate (FNA) cytology of breast masses.

The dataset contains groups of:

* Mean features
* Standard error features
* Worst-case features

## Data Preprocessing

The preprocessing workflow includes:

1. Loading the dataset
2. Removing unnecessary columns
3. Separating features and target
4. Handling missing values
5. Encoding the diagnosis labels
6. Feature scaling where required
7. Splitting the data into training and testing sets
8. Maintaining class balance through stratification where used

The diagnosis labels are converted into numerical classes representing malignant and benign tumors.

## Machine Learning Models

### 1. Logistic Regression

Logistic Regression is used as a linear binary classification model.

The model estimates the probability of a sample belonging to a particular class using the logistic (sigmoid) function.

The implementation uses:

```text
LogisticRegression
StandardScaler
train_test_split
```

### 2. K-Nearest Neighbors

KNN is an instance-based classification algorithm that predicts a sample based on the classes of its nearest neighbors.

The project uses:

```text
K = 5
```

The implementation evaluates the model using accuracy, classification reports, and a confusion matrix.

### 3. Support Vector Machine

SVM identifies a decision boundary that maximizes the margin between classes.

The project uses an:

```text
RBF (Radial Basis Function) kernel
```

Feature scaling is applied before training the SVM model.

## Model Comparison

According to the project report:

| Algorithm           | Model Type     | Typical Accuracy |
| ------------------- | -------------- | ---------------: |
| Logistic Regression | Linear         |             ~97% |
| KNN                 | Instance-based |             ~96% |
| SVM                 | Kernel-based   |           ~97.4% |

The report identifies **SVM with the RBF kernel** as achieving the highest accuracy among the three models in this comparison.

## Evaluation Metrics

The models are evaluated using:

* Accuracy
* Classification Report
* Confusion Matrix

These metrics provide information about classification performance beyond overall accuracy.

## Technologies Used

* Python
* Pandas
* NumPy
* Scikit-learn
* Matplotlib
* Seaborn

## How to Run

Install the required dependencies:

```bash
pip install pandas numpy scikit-learn matplotlib seaborn
```

Run the Python script or notebook containing the implementation:

```bash
python main.py
```

> Replace `main.py` with the actual filename in the repository if it is different.

## Project Workflow

```text
Breast Cancer Dataset
        ↓
Data Cleaning
        ↓
Missing Value Handling
        ↓
Feature / Target Separation
        ↓
Target Encoding
        ↓
Feature Scaling
        ↓
Train/Test Split
        ↓
┌───────────────┬───────────────┬───────────────┐
│ Logistic      │ KNN           │ SVM           │
│ Regression    │               │ RBF Kernel    │
└───────────────┴───────────────┴───────────────┘
        ↓
Model Predictions
        ↓
Performance Evaluation
        ↓
Algorithm Comparison
```

## Key Concepts Demonstrated

* Supervised learning
* Binary classification
* Logistic Regression
* K-Nearest Neighbors
* Support Vector Machines
* Feature preprocessing
* Standardization
* Missing-value imputation
* Train/test splitting
* Stratification
* Confusion matrices
* Classification reports
* Model comparison

## Limitations

This project is an academic comparison of machine learning algorithms using a publicly available dataset.

High accuracy on this dataset does not imply that the models are suitable for direct clinical diagnosis. Real-world medical applications require extensive validation, appropriate clinical datasets, and professional oversight.

## Future Improvements

Potential improvements include:

* Hyperparameter tuning
* Cross-validation
* ROC-AUC comparison
* Precision-recall analysis
* Feature selection
* Additional classification algorithms
* More comprehensive model evaluation
* Explainable machine learning techniques

## Dataset Reference

Wolberg, W. H., Street, W. N., & Mangasarian, O. L. (1995).
**Breast Cancer Wisconsin (Diagnostic) Database.**
UCI Machine Learning Repository.
