# Bank Operation Analysis
## Table of Content
- [Business Integrity](#business-integrity)
- [Tools Used](#tools-used)
- [﻿Data Cleaning or Preparation](﻿#data-cleaning-or-preparation)
- [Explanatory Data Analysis](#explanatory-data-analysis)
- [Result or Findings](#result-or-findings)
- [Recommendations](#recommendations)
- [Limitations](#limitations)
- [References](#references)

### Business Integrity
1.	Bank offers 5 kinds of products. Like Fixed Deposit (FD), Loan Account (LA), Savings Bank (SB), Current Account (CA), Recurring Deposit (RD). Product table has Product ID, Product Name columns.
2.	Bank operates in North, East, South, West region. Region table has Region ID, Region Name columns.
3.	Bank staff designations are Branch Manager (BM), Assistant Manager (AM), Officer (OF), Head Cashier (HC), Clerk (C). Staff table has Staff ID, Staff Name, Designation columns.
4.	Bank has 4 branches (BR1, BR3, BR4, BR6) in North region, 3 branches in East (BR2, BR7, BR8), South (BR5, BR9, BR11) and West (BR10, BR12, BR13) region respectively. Branch table has Branch ID, Branch Name, Branch Address, Brach State, Branch Zip code, regarding Region ID columns. Branch names are according to their city name.
5.	Bank maintains customer table. Table has Account ID starts from 1001 and incremented by 1, Customer Name, Customer Address, Customer State, Customer Zip code, regarding Branch ID, regarding Product ID, Date of Opening of Account ID, regarding Clear Balance (balance in account), regarding Unclear Balance (balance to be clear after few hours of received or withdrawal of money, may contain 0), Status of Account (‘O’ for Operative, ‘I’ for Inoperative, ‘C’ for Closed) columns.
6.	Bank maintains transaction table. Table has Transaction ID, Date of Transactions, regarding Account ID, regarding Branch ID, regarding Transaction Type (‘CW’ for Cash Withdrawal, ‘CD’ for ‘Cash Deposit’, ‘CQD’ for Cheque Deposit), Cheque Number if cheque deposited, Cheque Date if cheque deposited, Transaction Amount, regarding Staff ID.
7.	The account, branch, product, region, and staff IDs all have unique values.
8.	The current date should be used as the Date of Transaction (DOT) and Date of Opening (DOO).
9.	A cheque that is over six months old is not acceptable.
10.	Accounts marked as "Inoperative" should not be used for transactions.
11.	The clerk's alteration of a transaction can results in a difference between the old and new amounts of the transaction, not exceeding 10%.
12.	The policy prohibits more than three cash withdrawal transactions in a single account on the same day.
13.	The transaction type 'Cheque Deposit' should not have 'NULL' in the 'Cheque Number' and 'Cheque Date' columns.
14.	A product should not be removed if it has attached accounts, and similar checks are required where appropriate.
15.	The transaction Amount should not be negative.
16.	The transaction type should be either 'CW', 'CD', or 'CQD'.
17.	The minimum balance for a Savings Bank should be Rs. 1,000/=.
18.	The 'Account Table' should be updated implicitly when an account transaction amount is inserted or updated.
19.	If the account does not have a minimum balance, withdrawals should be prohibited and an appropriate message should be displayed.
20.	The cash deposit transaction amount exceeding Rs. 50,000/= should be inserted into the 'High Value Transaction' table.
21.	The monthly transaction limit should be less than 5, and if it exceeds Rs. 50/= will be debited.
22.	The daily maximum cash withdrawal limit is Rs.50,000/-, and any excess will result in a 1% debit charge.

### Tools Used
- SQL Server - Data Analysis, Data Cleaning -- [Download Here](https://www.microsoft.com/en-in/sql-server/sql-server-downloads)
- T-SQL - Data Analysis, Reports -- [Download Here](https://www.microsoft.com/en-in/sql-server/sql-server-downloads)
- Power BI - Reports, Visualization -- [Download Here](https://powerbi.microsoft.com/en-us/downloads/)
- Excel - Data Loadings -- [Download Here](https://www.microsoft.com/en-us/microsoft-365/download-office)

### ﻿Data Cleaning or Preparation
1. In the initial data preparation phase, we performed the following tasks:
2. Data loading and inspection.
3. Handling missing values.
4. Data cleaning and formatting.

### Explanatory Data Analysis
Include some interesting code/features worked with
1. question 1
   ```sql
   select * from table1
   ```
3. question 2

### Result or Findings
1. The analysis results are summarized as follows:
2. The company's sales have been steadily increasing over the past year, with a noticeable peak during the holiday season.
3. Product Category A is the best-performing category in terms of sales and revenue. Customer segments with high lifetime value (LTV) should be targeted for marketing efforts.

### Recommendations
1. Based on the analysis, we recommend the following actions:
2. Invest in marketing and promotions during peak sales seasons to maximize revenue. Focus on expanding and promoting products in Category A.
3. Implement a customer segmentation strategy to target high-LTV customers effectively.

### Limitations
I had to remove all zero values from budget and revenue columns because they would have affected the accuracy of my conclusions from the analysis. There are still a few outliers even after the omissions but even then we can still see that there is a positive correlation between both budget and number of votes with revenue

### References
---
1. [any link](www.google.com) or name of someone or anything

🛕

|heading1|heading|
|--------|-------|
|pythonn|sql|

`comment1`

**bold**

*italic*
