# Credit Risk Analyzer

## Project Description
A sophisticated credit risk model that categorizes loan applications into **Poor**, **Average**, **Good**, and **Excellent** categories based on criteria similar to the CIBIL scoring system.

```python
def get_rating(score):
    if 300 <= score < 500:
        return 'Poor'
    elif 500 <= score < 650:
        return 'Average'
    elif 650 <= score < 750:
        return 'Good'
    elif 750 <= score <= 900:
        return 'Excellent'
    else:
        return 'Undefined'
```

## Key Features
- Predict credit risk based on user inputs:
  - **Age**
  - **Income**
  - **Loan Amount**
  - **Loan Tenure (Months)**
  - **Average DPD per Delinquency**
  - **Delinquency Ratio**
  - **Credit Utilization Ratio**
  - **Number of Open Accounts**
  - **Residence Type**
  - **Loan Purpose**
  - **Loan Type**

## Technical Details
- **Programming Language**: Python
- **Libraries/Frameworks**: `scikit-learn`, `streamlit`, `pandas`, `numpy`, `joblib`, `xgboost`

## Installation
1. Clone the repository:
    ```bash
    git clone <repository-url>
    cd <repository-folder>
    ```
2. Install the dependencies:
    ```bash
    pip install -r requirements.txt
    ```
3. Run the Streamlit app:
    ```bash
    streamlit run app.py
    ```

## Usage
1. Open the deployed app on [Streamlit Cloud](https://credit-risk-analyzer-kesavadas.streamlit.app/).
2. Enter user details such as:
   - Age
   - Income
   - Loan Amount
   - Loan Tenure (Months)
   - Average DPD per Delinquency
   - Delinquency Ratio
   - Credit Utilization Ratio
   - Number of Open Accounts
   - Residence Type
   - Loan Purpose
   - Loan Type
3. The app predicts:
   - **Default Probability**: e.g., `63.25%`
   - **Credit Score**: e.g., `520`
   - **Rating**: e.g., `Average`

## Dataset Details
- Merged datasets:
  - **Customers Dataset**
  - **Loans Dataset**
  - **Bureau Dataset**
- Resulted in **50,000 rows** and **33 columns**.

## Machine Learning Pipeline
1. **Data Splitting**: Performed train-test split early to avoid data leakage.
2. **Data Cleaning**: Replaced invalid loan purpose values with mode.
3. **Feature Selection**: Utilized VIF, IF, and domain knowledge.
4. **Scaling**: Min-Max scaling for numeric features.
5. **Train-Test Split**: 75% train, 25% test.
6. **Model Training**:
   - Logistic Regression
   - XGBoost
   - Random Forest
7. **Fine Tuning**:
   - RandomizedSearchCV
   - Optuna
8. **Evaluation Metrics**:
   - AUC-ROC
   - KS
   - Gini Coefficient
   - Classification Report

## Deployment
- **Platform**: Streamlit Cloud

## Screenshots
![image](https://github.com/user-attachments/assets/f68243f6-916c-4f78-96dd-dc7f1f243425)

## License
This project is licensed under the Apache 2.0 License.

## Contributions
Contributions are welcome! Feel free to open issues or submit pull requests.
