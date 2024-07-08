# Loan Tap Customer Profiling

![LoanTap](https://github.com/hardeek24/LoanTapLogisticResgression_SMOTE/assets/162917115/6219f732-fc7e-48d0-bd7f-5cc8e13bed50)



## Overview

When applying for a bank loan, there is a lengthy process involving the submission of various documents and details such as a good credit score, a no dues certificate, and sometimes even a no crime certificate. However, not everyone is eligible for these loans and able to meet all the documentation requirements and profile evaluations. Loan Tap, as a company, aims to provide loans to individuals and small-sized firms (MSMEs) who may not be able to fulfill all the necessary requirements. They specifically target high-risk profiles as their potential customers, but within this category, there are three sub-profiles that loan applicants can fall into.

The first category is the "White Collar" customers, who are considered high risk but are expected to repay their loans. The second category is the "Grey Collar" customers, who have a mixed likelihood of repaying the loan. Lastly, the "Black Collar" customers are those who are unlikely to be able to repay the loan. Loan Tap focuses on the White Collar and Grey Collar customers only. However, they cannot approve loans for all Grey Collar customers.

This is where data scientists come in. They are needed to properly profile the Grey Collar customers so that Loan Tap can have a balanced mix of high-risk and low-risk customers, allowing them to potentially make a profit even if a few customers default on their loans.

## Data Description

This dataset includes the following features:

- **loan_amnt**: The listed amount of the loan applied for by the borrower. If at some point in time, the credit department reduces the loan amount, then it will be reflected in this value.
- **term**: The number of payments on the loan. Values are in months and can be either 36 or 60.
- **int_rate**: Interest Rate on the loan.
- **installment**: The monthly payment owed by the borrower if the loan originates.
- **grade**: LC assigned loan grade.
- **sub_grade**: LC assigned loan subgrade.
- **emp_title**: The job title supplied by the borrower when applying for the loan.
- **emp_length**: Employment length in years. Possible values are between 0 and 10 where 0 means less than one year and 10 means ten or more years.
- **home_ownership**: The home ownership status provided by the borrower during registration or obtained from the credit report. Values are: RENT, OWN, MORTGAGE, OTHER.
- **annual_inc**: The self-reported annual income provided by the borrower during registration.
- **verification_status**: Indicates if income was verified by LC, not verified, or if the income source was verified.
- **issue_d**: The month which the loan was funded.
- **loan_status**: Current status of the loan.
- **purpose**: A category provided by the borrower for the loan request.
- **title**: The loan title provided by the borrower.
- **zip_code**: The first 3 numbers of the zip code provided by the borrower in the loan application.
- **addr_state**: The state provided by the borrower in the loan application.
- **dti**: A ratio calculated using the borrower’s total monthly debt payments on the total debt obligations, excluding mortgage and the requested LC loan, divided by the borrower’s self-reported monthly income.
- **earliest_cr_line**: The month the borrower's earliest reported credit line was opened.
- **open_acc**: The number of open credit lines in the borrower's credit file.
- **pub_rec**: Number of derogatory public records.
- **revol_bal**: Total credit revolving balance.
- **revol_util**: Revolving line utilization rate, or the amount of credit the borrower is using relative to all available revolving credit.
- **total_acc**: The total number of credit lines currently in the borrower's credit file.
- **initial_list_status**: The initial listing status of the loan. Possible values are W, F.
- **application_type**: Indicates whether the loan is an individual application or a joint application with two co-borrowers.
- **mort_acc**: Number of mortgage accounts.
- **pub_rec_bankruptcies**: Number of public record bankruptcies.

## Analysis Goals

- **Identify Defaulters**: Determine which customers are likely to default on their loans.
- **Risk Mitigation**: Focus on specific customers to minimize risk.
- **Targeted Marketing**: Use data insights to conduct targeted marketing campaigns.

## Getting Started

### Prerequisites

- Python 3.6+
- Required libraries are listed in `requirements.txt`.

### Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/your-username/loan-tap-customer-profiling.git
    cd loan-tap-customer-profiling
    ```

2. Create a virtual environment and activate it:
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows use `venv\Scripts\activate`
    ```

3. Install the dependencies:
    ```bash
    pip install -r requirements.txt
    ```

### Running the Application

To run the Streamlit application, use the following command:
```bash
streamlit run app.py


