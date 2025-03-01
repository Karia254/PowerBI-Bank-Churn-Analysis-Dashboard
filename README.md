# Bank Customer Churn Analysis Dashboard

## **Project Overview**
This project analyzes customer churn data for the Royal Bank of Canada(RBC) using Power BI to identify patterns and trends that contribute to customers leaving. The dashboard provides actionable insights to improve customer retention and inform marketing strategies. Key performance indicators (KPIs) include:
- **Total Customers**: Total count of customers.
- **Active Customers**: Number of currently active customers.
- **Inactive Customers**: Number of inactive customers.
- **Credit Card Holders**: Number of customers with a credit card.
- **Retained Customers**: Number of customers who stayed.
- **Exited Customers**: Number of customers who left.

![RBC Churn](https://github.com/user-attachments/assets/587a329a-e87f-415a-93ee-959f87212efa)

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

### 1. **Credit Score**
- Customers with higher credit scores (Excellent/Very Good) are less likely to churn, while those with lower credit scores (Fair/Poor) are more likely to leave.  
- **Key Findings:**
  - 685 customers with a **Fair** credit score exited, the highest among all categories.
  - 580 customers with a **Poor** credit score also left.
  - Only **128 customers** with an **Excellent** credit status churned.  

- **Action:**  
  - Implement targeted retention programs for customers with Fair/Poor credit scores.
  - Offer financial education, better loan terms, or personalized banking support to reduce churn.

### 2. **Tenure**
- Customers with longer tenure exhibit lower churn rates, whereas newer customers are more likely to leave.  
- **Key Findings:**
  - Customers with a **7-year tenure** had the lowest churn rate at **10.7%**.
  - Customers with a **4-year tenure** had the highest churn rate at **28.23%**.

- **Action:**  
  - Enhance the onboarding experience to engage new customers early.
  - Introduce loyalty programs and personalized banking solutions for customers in their early years.

### 3. **Balance**
- Customers with higher balances tend to stay, while those with lower balances are at higher risk of churn.  
- **Key Findings:**
  - Customers who **exited** had a total balance of **$185.59M**.
  - Customers who **remained** had a significantly higher total balance of **$579.27M**.

- **Action:**  
  - Encourage savings and investments among low-balance customers with tailored financial products.
  - Offer incentives such as better interest rates or exclusive benefits for customers maintaining higher balances.

### 4. **Location**
- Churn rates vary by location, with Germany having the highest churn rate.  
- **Key Findings:**
  - **Germany**: **32.44% churn rate**, the highest among the three countries.
  - **France**: **16.15% churn rate**.
  - **Spain**: **16.67% churn rate**.

- **Action:**  
  - Investigate the reasons behind the high churn in Germany (e.g., economic factors, competitor offerings, customer dissatisfaction).
  - Implement region-specific customer engagement strategies, such as localized services, better customer support, or competitive banking products.

---

## **Conclusion**
The **Bank Customer Churn Analysis Dashboard** provides valuable insights into the factors influencing customer churn at the **Royal Bank of Canada (RBC)**. By analyzing key metrics such as **credit score, tenure, balance, and geography**, the bank can implement targeted strategies to enhance customer retention.

### **Key Takeaways:**
- **Customers with low credit scores** (Fair/Poor) are more likely to leave, necessitating financial education and personalized retention programs.
- **Newer customers** have a significantly higher churn rate, highlighting the need for better onboarding and loyalty incentives.


