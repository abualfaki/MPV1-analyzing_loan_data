# **Customer Segmentation Analysis for LendingClub.com**

![image](https://github.com/user-attachments/assets/8121eb1c-f966-43d8-b445-3b059b4c738b)


Analyzing the customer segments of **LendingClub.com**, a peer-to-peer lending platform, to understand borrower demographics, loan charge-off rates, and underwriting inefficiencies.

## **Table of Contents**
- [Overview](#overview)
- [Recommendations](#recommendations)
- [Aim](#aim)
- [Technologies](#technologies)
- [Data](#data)
- [Cleaning & Processing](#cleaning--processing)
- [Analysis & Insights](#analysis--insights)
- [Challenges](#challenges)


---

## **Overview**
This project focuses on analyzing **LendingClub.com**'s loan data to identify key customer segments, assess risk levels, and uncover underwriting inefficiencies. The analysis highlights income-based default rates, debt-to-income (DTI) ratio considerations, and geographic distributions of borrowers. 

### **Key Insights**
- **31%** of LendingClub’s borrowers earn **$50,000 - $75,000** annually, while **26%** earn **$25,000 - $50,000**.
- Borrowers earning **$50,000 - $75,000** have an **18.5% charge-off rate**, whereas those earning **$200,000 - $500,000** have a lower **14.1% charge-off rate**.
- Debt-to-Income (DTI) ratio was not considered in underwriting, potentially leading to riskier loan issuances.
- The majority of LendingClub’s borrowers reside in **California (13.9%)**, **New York (8.2%)**, **Texas (8.2%)**, and **Florida (7.2%)**, presenting key areas for marketing efforts.

---
## **Recommendations**
1. **Enhance Underwriting by Incorporating DTI**  
   - Including **Debt-to-Income ratio** in the credit decision-making process can help prevent issuing loans to borrowers who may struggle with repayments.
   
2. **Target High-Quality Borrowers for Lower Default Risk**  
   - Focus on borrowers earning **$200,000 - $500,000**, as they have a lower **14.1% charge-off rate** compared to middle-income earners.

3. **Refine Marketing Strategies Based on Geography**  
   - Prioritize **California, New York, Texas, and Florida**, where most borrowers are located, to improve customer acquisition efficiency.

4. **Improve Data Input Standardization**  
   - Implement **dropdown selections** instead of free-text input for job titles and loan purposes to reduce data inconsistencies.
## **Aim**
To help LendingClub **identify high-ROI customer segments** and refine the loan application process by analyzing borrower demographics, income levels, and underwriting policies.

---

## **Technologies**
- **Python 3.10.11**
    - `pandas`, `NumPy`, `Matplotlib`, `Seaborn`
    - `FuzzyWuzzy` for text-based data correction
- **PostgreSQL**
- **ipython-sql**
- **Jupyter Notebook**

---

## **Data**
### **Collection**
The dataset was sourced from Kaggle and includes loan records from **2007 to Q2 2018**.  
[View dataset on Kaggle](https://www.kaggle.com/code/faressayah/lending-club-loan-defaulters-prediction)

### **Cleaning & Processing**
- Cleaned a **2 million-row dataset with 151 features**, handling missing values, outliers, and datatype conversions.
- Used **Fuzzy Matching Algorithm** to automatically correct misspelled job titles, reducing data cleaning time from **weeks to 7 minutes**.
- Identified borrowers' **loan purposes** and corrected inconsistencies in user-inputted categories.

---

## **Analysis & Insights**
### **Income-Based Charge-Off Rates**
- Borrowers in the **$50,000 - $75,000** income range faced an **18.5% loan charge-off rate**.
- Borrowers in the **$200,000 - $500,000** range had a **14.1% charge-off rate**, suggesting lower risk at higher income levels.

### **Debt-to-Income (DTI) Ratio Considerations**
- **DTI was not factored into LendingClub's underwriting process**, possibly leading to loans issued to **highly indebted borrowers** who struggled with repayments.

### **Geographic Distribution**
- **Top borrower states**:
  - **California (13.9%)**
  - **New York (8.2%)**
  - **Texas (8.2%)**
  - **Florida (7.2%)**
- These states represent key **marketing and risk management** opportunities.

---

## **Challenges**
- **Text-based data inconsistencies**: Borrowers manually entered job titles, leading to spelling errors and inconsistencies.
  - Used **Fuzzy Matching Algorithm** to detect and correct errors efficiently.
- **Data size**: The dataset contained **2 million rows**, requiring optimized processing and cleaning strategies.
- **Loan purpose inconsistencies**: Borrowers entered varying descriptions for similar loan purposes, requiring **categorization standardization**.

---


