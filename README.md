# Bank Customer Churn Analysis Dashboard

# **Project Overview**

This project aims to analyze and visualize customer churn data for a bank using Power BI. The goal is to identify patterns and trends that contribute to customers leaving the bank. By examining various customer attributes, we can offer insights that may help improve customer retention and inform marketing or loyalty campaigns.

#**Data Dictionary**

The following table provides an explanation of the data fields used in the analysis:
| **Column Name**   | **Description**                                                                 |
|-------------------|---------------------------------------------------------------------------------|
| **RowNumber**     | Corresponds to the record (row) number; has no effect on output.               |
| **CustomerId**    | Contains random values; has no impact on customer churn.                        |
| **Surname**       | Customer’s surname; has no impact on their decision to leave the bank.          |
| **CreditScore**   | Credit score can influence churn. Higher credit scores are associated with lower churn risk. |
| **Geography**     | Customer’s location, potentially affecting churn likelihood.                     |
| **Gender**        | Gender of the customer, examined for any correlation with churn.                 |
| **Age**           | Age is relevant as older customers are generally less likely to leave.          |
| **Tenure**        | The number of years the customer has been with the bank. Longer tenure correlates with lower churn. |
| **Balance**       | Account balance can indicate churn risk. Higher balances are associated with lower churn. |
| **NumOfProducts** | Number of products the customer holds. Customers with more products are less likely to churn. |
| **HasCrCard**     | Indicates whether the customer holds a credit card. Credit card holders are less likely to churn. |
| **IsActiveMember**| Denotes whether the customer is an active member. Active members are less likely to leave. |
| **EstimatedSalary**| Salary is linked to churn; lower salaries are associated with higher churn risk. |
| **Exited**        | Whether the customer exited the bank (1 = Exit, 0 = Retained).                  |
| **Bank DOJ**      | Date of joining the bank.                                                      |



