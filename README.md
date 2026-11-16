# CreditWise – Loan Approval Prediction

A Machine Learning project that predicts loan approval outcomes based on applicant financial, demographic, and loan-related information.

## About the Project

CreditWise is a supervised Machine Learning classification project developed as part of an academic assignment.

The goal is to analyze loan applicant information and predict whether a loan application will be approved or rejected. The project covers the complete basic ML workflow, from data preprocessing and exploratory data analysis to model training, feature engineering, and performance evaluation.

## Project Objectives

- Analyze applicant information and loan-related factors.
- Handle missing values and prepare data for model training.
- Explore relationships between different features using visualizations.
- Apply encoding and feature scaling techniques.
- Train and compare multiple classification algorithms.
- Evaluate model performance using standard classification metrics.
- Experiment with feature engineering to improve prediction performance.

## Technologies & Libraries

- **Language:** Python
- **Data Manipulation:** Pandas, NumPy
- **Data Visualization:** Matplotlib, Seaborn
- **Machine Learning:** Scikit-learn
- **Environment:** Jupyter Notebook

## Dataset Overview

The project uses a loan approval dataset containing 1,000 records and 20 original columns.

The dataset includes information related to:

- Applicant income and co-applicant income
- Employment status and employer category
- Age and marital status
- Credit score and existing loans
- Debt-to-Income (DTI) ratio
- Savings and collateral value
- Loan amount, loan term, and loan purpose
- Property area and education level
- Loan approval status (target variable)

**Note:** The dataset is not included in this repository. The notebook expects a file named `loan_approval_data.csv` in the project directory. Place the dataset there before running the notebook.

## Project Workflow

### 1. Data Loading and Inspection
- Load the dataset using Pandas.
- Examine the dataset structure, data types, and statistical summaries.
- Identify missing values in numerical and categorical columns.

### 2. Data Preprocessing
- Handle missing numerical values using mean imputation.
- Handle missing categorical values using most-frequent imputation.
- Remove the `Applicant_ID` column.
- Prepare the target variable for classification.

### 3. Exploratory Data Analysis (EDA)
- Explore numerical and categorical feature distributions.
- Analyze relationships between applicant attributes.
- Use visualizations to understand patterns in the dataset.
- Examine feature correlations using a heatmap.

### 4. Feature Encoding
- Apply Label Encoding to `Education_Level` and `Loan_Approved`.
- Apply One-Hot Encoding to selected categorical features.
- Convert categorical information into numerical representations.

### 5. Feature Scaling
- Split the dataset into training and testing sets using an 80:20 ratio.
- Apply StandardScaler to standardize numerical features.
- Use the training data to fit the scaler and transform the test data.

### 6. Model Training and Evaluation

Train and evaluate three classification algorithms:

- Logistic Regression
- K-Nearest Neighbors (KNN)
- Gaussian Naive Bayes

Evaluate each model using:
- Accuracy
- Precision
- Recall
- F1-score
- Confusion Matrix

### 7. Feature Engineering

Experiment with additional features to improve model performance:

- Square transformation of Credit Score.
- Square transformation of DTI Ratio.
- Log transformation of Applicant Income using `log1p()`.

Retrain the classification models and compare their performance with the initial results.

## Model Performance

The following results were obtained from the notebook using an 80:20 train-test split.

### Initial Model Results

| Algorithm | Accuracy | Precision | Recall | F1-Score |
|---|---:|---:|---:|---:|
| Logistic Regression | 86.5% | 78.33% | 77.05% | 77.69% |
| KNN | 76.5% | 62.96% | 55.74% | 59.13% |
| Gaussian Naive Bayes | 86.5% | 80.36% | 73.77% | 76.92% |

### Results After Feature Engineering

| Algorithm | Accuracy | Precision | Recall | F1-Score |
|---|---:|---:|---:|---:|
| Logistic Regression | 87% | 77.78% | 80.33% | 79.03% |
| KNN | 76.5% | 62.96% | 55.74% | 59.13% |
| Gaussian Naive Bayes | 86.5% | 80.36% | 73.77% | 76.92% |

### Key Observations

- Logistic Regression achieved the highest accuracy of 87% after feature engineering.
- Logistic Regression also achieved the highest F1-score of 79.03%.
- Gaussian Naive Bayes achieved the highest precision of 80.36%.
- KNN achieved an accuracy of 76.5% and showed no improvement after feature engineering.
- Feature engineering improved Logistic Regression's accuracy, recall, and F1-score.

## Project Structure

```text
CreditWise-Loan-System/
│
├── loan_approval_prediction.ipynb
├── README.md
├── requirements.txt
└── .gitignore
```

## How to Run the Project

### 1. Clone the Repository

```bash
git clone https://github.com/Mohith-Bitra09/CreditWise-Loan-System.git
```

### 2. Navigate to the Project Directory

```bash
cd CreditWise-Loan-System
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Add the Dataset

Obtain the original `loan_approval_data.csv` dataset separately and place it in the project directory.

### 5. Launch Jupyter Notebook

```bash
jupyter notebook
```

Open `loan_approval_prediction.ipynb` and execute the cells to explore the analysis and model results.

## Key Learnings

Through this project, I gained practical experience in:

- Data cleaning and missing-value handling.
- Exploratory Data Analysis and data visualization.
- Label Encoding and One-Hot Encoding.
- Feature scaling using StandardScaler.
- Implementing classification algorithms using Scikit-learn.
- Evaluating models using classification metrics.
- Feature engineering and model performance comparison.

## Limitations

- The project uses a single train-test split for model evaluation.
- Preprocessing steps such as imputation and encoding are fitted before the train-test split in the current notebook, which can introduce data leakage.
- The models have not been evaluated through cross-validation or hyperparameter tuning.

## Disclaimer

This project is developed for academic and learning purposes. The predictions are experimental and should not be used as the sole basis for real-world loan approval decisions.

---

**Project:** CreditWise – Loan Approval Prediction  
**Category:** Supervised Machine Learning | Binary Classification  
**Developed using:** Python and Scikit-learn