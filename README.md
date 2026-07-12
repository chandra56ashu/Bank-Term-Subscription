# Bank Term Deposit Subscription Prediction

A machine learning project that predicts whether a bank customer will subscribe to a term deposit using demographic, financial and campaign information from the Portuguese bank marketing dataset.

## Project objective

The analysis compares an interpretable Logistic Regression model with a Random Forest classifier. It focuses on identifying customers most likely to subscribe while addressing the strong class imbalance in the target variable.

## Dataset

The notebook analyses 45,211 customer records with 17 variables, including:

- Customer profile: age, job, marital status and education
- Financial position: balance, housing loan, personal loan and default status
- Campaign activity: contact type, month, call duration and number of contacts
- Previous campaign history: days since prior contact, previous contacts and outcome
- Target: whether the customer subscribed to a term deposit

The positive subscription class represents approximately 7.5% of the observations.

## Analytical workflow

1. Data quality and structural assessment
2. Exploratory data analysis
3. Feature engineering and transformation
4. Categorical encoding and numerical scaling
5. Class-imbalance handling with class weights
6. Logistic Regression and Random Forest modelling
7. Hyperparameter tuning with cross-validation
8. Model evaluation using ROC-AUC, precision, recall and confusion matrices
9. Interpretation of important predictors and business implications

## Results

- Logistic Regression provided strong interpretability and high recall for subscribers.
- Random Forest achieved the stronger overall ROC-AUC after tuning.
- A successful previous campaign outcome and longer call duration were among the strongest positive signals.
- The final discussion balances model discrimination with the need for actionable, explainable targeting decisions.

## Tools

- Python
- pandas and NumPy
- Matplotlib and Seaborn
- scikit-learn
- statsmodels
- Jupyter Notebook

## Repository contents

- `Bank Term Deposit Subscription .ipynb` — complete analysis and modelling workflow

## Running the notebook

1. Clone or download this repository.
2. Install the required libraries:

```bash
pip install pandas numpy openpyxl matplotlib seaborn statsmodels scikit-learn
```

3. Download the `bank-full.csv` dataset and update the file path in the data-loading cell.
4. Run the notebook from top to bottom.

## Limitations

- Call duration is only known after a call has taken place, so it should be excluded from any true pre-call targeting model.
- Model performance depends on the historical campaign and customer population represented in the dataset.
- Predictions indicate statistical likelihood, not certainty.

## Author

Ashutosh Chandra
