# Bank Customer Churn Analysis Dashboard

# **Project Overview**

This project aims to analyze and visualize customer churn data for a bank using Power BI. The goal is to identify patterns and trends that contribute to customers leaving the bank. By examining various customer attributes, we can offer insights that may help improve customer retention and inform marketing or loyalty campaigns.

---
**Data Dictionary**

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

---
**Data Gathering**
To conduct this analysis, the following datasets were used:

ActiveCustomer
Bank_Churn
CreditCard
CustomerInfo
ExitCustomer
Gender
Geography

**Data Modelling**
The data model for this analysis follows a Star Schema design. The key features of the model are as follows:

**Fact Table**: The Bank_Churn table acts as the central fact table, storing information about customer churn (whether a customer exited or retained).
**Dimension Tables**: Several dimension tables were created to provide descriptive attributes related to the fact data. These include:

1. **Customer**: Details about the customer such as ID, gender, age, balance, and salary.
2. **Geography**: Information related to customer location.
3. **CreditCard**: Data regarding whether the customer holds a credit card.
4. **ActiveStatus**: A table indicating if the customer is an active member of the bank.

The tables were combined and relationships were created using PowerBI’s relationship feature, linking the fact table to the dimension tables through keys such as CustomerId, GeographyId, and CreditCardId. This enables effective querying and reporting on various dimensions of the customer data (e.g., customer demographics, geographic location, and product holdings).

Below is a screenshot of the Data Model in PowerBI:
![Data model](https://github.com/user-attachments/assets/88de061b-fdf1-4244-a2dd-c0595af716eb)


