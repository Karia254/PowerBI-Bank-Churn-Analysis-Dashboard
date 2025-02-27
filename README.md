# Bank Customer Churn Analysis Dashboard

## **Project Overview**
This project analyzes customer churn data for a bank using Power BI to identify patterns and trends that contribute to customers leaving. The dashboard provides actionable insights to improve customer retention and inform marketing strategies. Key performance indicators (KPIs) include:
- **Total Customers**: Total count of customers.
- **Active Customers**: Number of currently active customers.
- **Inactive Customers**: Number of inactive customers.
- **Credit Card Holders**: Number of customers with a credit card.
- **Retained Customers**: Number of customers who stayed.
- **Exited Customers**: Number of customers who left.

![RBC Bank Customer Churn Analysis](https://github.com/user-attachments/assets/916a7134-6b4e-4f0f-8faf-21e7ba1daece)

---

## **Data Overview**
The dataset includes customer attributes such as **Credit Score**, **Geography**, **Age**, **Tenure**, **Balance**, **Number of Products**, **Credit Card Status**, **Active Membership**, and **Estimated Salary**. Key fields like **Exited** indicate whether a customer left the bank (1 = Exit, 0 = Retained), while **Bank DOJ** tracks the date of joining.

---

## **Data Gathering**
The analysis uses datasets like **ActiveCustomer**, **Bank_Churn**, **CreditCard**, **CustomerInfo**, **ExitCustomer**, **Gender**, and **Geography** to provide a comprehensive view of customer behavior.

---

## **Data Modeling**
The data model follows a **Star Schema** design:
- **Fact Table**: `Bank_Churn` (central table for churn data).
- **Dimension Tables**: `Customer`, `Geography`, `CreditCard`, and `ActiveStatus` (provide descriptive attributes).

Relationships were established using keys like **CustomerId**, **GeographyId**, and **CreditCardId** to enable dynamic analysis across customer demographics, location, and product holdings.

![Data Model](https://github.com/user-attachments/assets/88de061b-fdf1-4244-a2dd-c0595af716eb)

---

## **DAX Measures & Calculated Columns**
- **Measures**: Calculated metrics like **total churn rate**, **average customer age**, and **average balance**.
- **Calculated Columns**: 
  - **Credit Status**: Classifies customers based on credit scores (e.g., Excellent, Very Good, Good, Fair, Poor).
  - **Date Master Table**: Facilitates time-based analysis with fields like **Year**, **Month**, and **Day** extracted from **Bank DOJ**.

---

## **Churn Analysis & Insights**
1. **Credit Score**: Customers with higher credit scores (Excellent/Very Good) are less likely to churn. Those with lower scores (Fair/Poor) are at higher risk.
   - *Action*: Target low-credit-score customers with retention programs.

2. **Tenure**: Longer-tenured customers exhibit lower churn rates, while newer customers are more likely to leave.
   - *Action*: Improve the onboarding experience and offer loyalty programs for new customers.

3. **Balance**: Customers with higher balances are less likely to churn, while those with lower balances are at higher risk.
   - *Action*: Incentivize low-balance customers to increase deposits through tailored offers.

4. **Active Membership**: Active customers have significantly lower churn rates compared to inactive ones.
   - *Action*: Increase engagement among inactive customers through personalized offers.

---

## **How to Use**
1. Download the `.pbix` file and open it in Power BI Desktop.
2. Use filters and slicers to explore specific customer segments, time periods, or geographic regions.
3. Refer to the KPIs and visualizations for actionable insights.

---

## **Contributing**
Contributions are welcome! Fork the repository, create a new branch, and submit a pull request with your changes.

---

## **License**
This project is licensed under the [MIT License](LICENSE).
