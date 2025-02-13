# Bank Customer Churn Analysis Dashboard

# **Project Overview**

This project aims to analyze and visualize customer churn data for a bank using Power BI. The goal is to identify patterns and trends that contribute to customers leaving the bank. By examining various customer attributes, I can offer insights that may help improve customer retention and inform marketing or loyalty campaigns.The dashboard also shows key performance indicators (KPIs) such as:
- **Total Number of Customers**: The total count of customers in the bank.
- **Active Customers**: The number of customers who are currently active with the bank.
- **Inactive Customers**: The number of customers who have become inactive.
- **Credit Card Holders**: The number of customers who have a credit card with the bank.
- **Retained Customers**: The number of customers who have stayed with the bank.
- **Exited Customers**: The number of customers who have left the bank.
  ![RBC Bank Customer Churn Analysis](https://github.com/user-attachments/assets/916a7134-6b4e-4f0f-8faf-21e7ba1daece)


---
## Data Dictionary

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
## Data Gathering
To conduct this analysis, the following datasets were used:

1. ActiveCustomer
2. Bank_Churn
3. CreditCard
4. CustomerInfo
5. ExitCustomer
6. Gender
7. Geography

---
## Data Modelling

The data model for this analysis follows a Star Schema design. The key features of the model are as follows:

**Fact Table**: The Bank_Churn table acts as the central fact table, storing information about customer churn (whether a customer exited or retained).

**Dimension Tables**: Several dimension tables were created to provide descriptive attributes related to the fact data. These include:

   1. **Customer**: Details about the customer such as ID, gender, age, balance, and salary.
   2. **Geography**: Information related to customer location.
   3. **CreditCard**: Data regarding whether the customer holds a credit card.
   4. **ActiveStatus**: A table indicating if the customer is an active member of the bank.

The tables were combined and relationships were created using PowerBI’s relationship feature, linking the fact table to the dimension tables through keys such as **CustomerId**, **GeographyId**, and **CreditCardId**. This enables effective querying and reporting on various dimensions of the customer data (e.g., customer demographics, geographic location, and product holdings).

Below is a screenshot of the Data Model in PowerBI:
![Data model](https://github.com/user-attachments/assets/88de061b-fdf1-4244-a2dd-c0595af716eb)



---
**DAX Measures:**
Measures were created to calculate key metrics, such as **total churn rate**, **average customer age***, **average balance**, and more. These measures allowed for dynamic calculations based on slicers on the dashboard.

**Calculated Columns:** 

Additional calculated columns were created to derive new insights from existing data. These include:

Credit Status: A calculated column that classifies customers according to their Credit Score based on the business requirements:
**Excellent**: 800–850

**Very Good**: 740–799

**Good: 670–739**

**Fair: 580–669**

**Poor: 300–579**

**Date Master Table:**

A Date Master Table was created to facilitate time-based analysis. This table contains:

**Year**: Extracted from the customer’s Bank DOJ to allow for year-over-year comparisons.

**Month**: Extracted from Bank DOJ for monthly trend analysis.

**Day**: For finer date-level insights, such as tracking churn on specific days or trends over specific periods.

---
## Churn Analysis & Insights

The goal of this analysis was to identify key factors that contribute to customer churn in the bank. Based on the data and DAX measures applied, the following insights were discovered:

1.**Credit Score:**

**Insight**: Higher credit scores are correlated with lower churn rates. Customers who have Excellent or Very Good credit scores tend to stay longer with the bank and are less likely to churn. Conversely, customers with Fair or Poor credit scores are more likely to leave.

**Actionable Insight**: The bank can target customers with lower credit scores with retention programs or financial products aimed at improving their credit standing.

2.**Tenure**:

**Insight**: Customers who have been with the bank for a longer period (higher tenure) tend to have lower churn rates. These customers exhibit a higher level of loyalty. In contrast, newer customers, especially those with low tenure, have a significantly higher churn rate.
**Actionable Insight**: The bank could focus on improving the early customer experience to reduce churn among new customers, such as offering loyalty programs or personalized services.

3.**Balance:**

**Insight**: Customers with higher account balances exhibit lower churn, while those with lower balances are more likely to exit the bank. High balance customers likely perceive more value in maintaining a relationship with the bank.
**Actionable Insight**: Offering premium banking services or incentives to customers with low balances might help reduce churn in this group, encouraging them to increase their balance and stay with the bank.

4.**Active Membership:**

**Insight**: Active customers have significantly lower churn rates than inactive ones. Customers who are engaged with the bank and use its services regularly (e.g., through frequent transactions or interactions) are more likely to stay.

**Actionable Insight**: The bank should prioritize increasing engagement among inactive customers by introducing personalized offers or incentives to encourage regular use of banking services.
