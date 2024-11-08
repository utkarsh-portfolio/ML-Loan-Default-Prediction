# ML-Loan-Default-Prediction

## Loan Default Prediction Model
### 1. Introduction
This project focuses on predicting loan defaults based on various features from a loan dataset. A loan default refers to the failure of a borrower to make required payments on a loan, which can result in financial loss for lending institutions. By accurately predicting which borrowers are likely to default on their loans, financial institutions can make better lending decisions and mitigate risks.

In this notebook, we build a machine learning pipeline to predict loan defaults using features such as personal information (e.g., age, income, and employment details), loan information (e.g., loan amount, interest rate, and loan term), and other behavioral and financial characteristics.

### 2. Dataset Overview
The dataset used for this project contains several columns, including both numerical and categorical features related to the borrower and the loan. The target variable, Default, indicates whether the loan defaulted or not (binary classification).

#### Key features in the dataset include:
##### Numerical features:
Age, Income, Loan Amount, Credit Score, Months Employed, Number of Credit Lines, Interest Rate, Loan Term, Debt-to-Income Ratio (DTIRatio).

##### Categorical features:
Education, Employment Type, Marital Status, Has Mortgage, Has Dependents, Loan Purpose, Has Co-Signer.

### 3. Problem Statement
The goal of this project is to develop a predictive model that can:

Accurately predict whether a loan will default or not (classification problem). Identify the most important features that influence the likelihood of loan default.

### 4. Data Preprocessing
Data preprocessing is a crucial step in building any machine learning model. In this step, we handled the following tasks:

#### Loading and Exploring Data:

The dataset was loaded and the first few records were reviewed to understand its structure and the types of features available. Descriptive statistics and data types were examined using .describe() and .info(). Handling Missing Values:

We checked for missing values and outliers to ensure the dataset was clean and ready for analysis. Feature Selection and Engineering:

We split the dataset into numerical and categorical features. For categorical variables, One-Hot Encoding was used to convert them into numerical format. Correlations between numerical features were visualized using a heatmap to detect multicollinearity, and less important features were removed based on their correlation and feature importance analysis. Feature Importance:

We used a Random Forest Regressor to evaluate the feature importance of all variables. Features with an importance score lower than 0.02 were excluded from the model, leaving only the most relevant features.

### 5. Data Transformation
#### Scaling:

Numerical features were standardized using StandardScaler to bring them to the same scale and prevent any one feature from disproportionately affecting the model due to its higher magnitude (e.g., Income or Loan Amount). One-Hot Encoding:

Categorical features were encoded into binary format using pd.get_dummies(), ensuring that all data used in the model is numerical and suitable for machine learning algorithms. Data Splitting:

The dataset was split into a training set (70%) and a test set (30%) using train_test_split to allow the model to learn from one portion of the data and be evaluated on another.

### 6. Model Building
In the next steps, machine learning models will be built using the preprocessed data. The key objectives at this stage are:

Model Training: We will train various machine learning algorithms (e.g., Random Forest, Logistic Regression) to predict loan defaults. Evaluation: The model’s performance will be evaluated using metrics such as accuracy, precision, recall, and the F1-score. We will also use cross-validation to assess model robustness. Feature Significance: We will analyze which features are most impactful for the loan default prediction.

### 7. Conclusion
By the end of this project, we aim to:

Build an accurate loan default prediction model. Identify the most influential features in predicting loan defaults. Provide insights that can help financial institutions make better lending decisions and minimize risks.
