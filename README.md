# Investment-Study-
This Analysis report shows Online Loan study, where multiple derivations based on Return of Investment,Loan Defaulted, Number of loans issued
based on employment, state, loan_puprose and other metrics have been depicted.
Data shape - **39717 columns and 111 rows**

| Code |
| ----------- | ----------- |
| Header | Title |
| Paragraph | Text |

---

## Code and Resources used
**Python** - 3.0
**Packages** : pandas, numpy, matplotlib, seaborn.

---

## Data Cleaning
After reading the data, following changes were done 
- Fixing Rows and Columns: DataType changes and column values fixing
- Convert string object to date object for below columns: *issue_d, last_pymt_date,int_rate*
- Removal of extra space in column value : *term*
---
## Missing values
Dropping unnecessary columns and columns with more 70% of missing values and filling missing values.
- Let's drop the columns with more than 30% missing values(since the data is already huge).
- Since there is no much spread of data and the difference between mean and median is very small, let's impute the missing  values with mean for column: *revol_util*.
 
---
##  Analysis for number of loan issued
![](/images/SC1.png)
1) From above plots, it shows that more number of loans were from *B,A and C grade's and least from G grade*.
2) From Sub grades A4, B3 have more number of loans.
3) From 3rd plot, it shows that **A,B,C** grade loans have **less interest rate** and **E,F,G** have **high interest rate**. From 1st, 2nd plots there are more number of loans from A,B,C grade(granularity check from sub-grades). It might be the reason that the loan applicant's from A,B,C grades have better credit score and lower risk.
4) From 4th plot, it shows that there are *high funded amount in A,B,C and D grades as the applicant's from these grades have better credit score and lower risk*.
![](/images/download%20(1).png)
We see that the majority of borrowers have been employed for at least 10 years.

---

## Analysis on the loan defaulters
![](/images/download%20(2).png)
 It shows there are more defaulters in RENT and MORTGAGE.

![](/images/download%20(3).png)
 There are more defaulters from 'debt_consolidation','other', 'credit_card' and 'small_business'
 
---
## Conclusion:
1) Number of loans issued increased steadily by every year with a slight decrease in 2008.
2) Of settled loans, 83% were Fully Paid and 14% were Charged Off.
3) Borrowers with own house and the purpose of loan with consolidate debt, 'credit_card' and 'small_business' are not at much risk, but borrower with rent,mortgage are high risk applicants.
4) Majority of loans were from A, B, and C grade.
5) There is an inverse relationship between interest rate and loan grade - lower grades(E,F,G) have higher interest rate.
6) Overall, there are more defaulters from 'debt_consolidation', 'others', 'credit_card' and 'small_business' purpose loans from all grades.
