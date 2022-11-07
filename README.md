# ProsperLoan
# (Dataset Exploration Title)
## by (Joy Ikogho)


## Dataset
This data set contains 113,912 loan lists from 2005Q4 till 2014Q1 with 81 variables on each loan, including loan original amount, borrower rate (or interest rate), current loan status, borrowerAPR, listing category, employment status, loan term, income range, current loan status and many other features. You can view the complete dataset[here](https://s3.amazonaws.com/udacity-hosted-downloads/ud651/prosperLoanData.csv)


## Summary of Findings

During my exploration, I found the following:
  
  Looking at the relation between Loan original amount, borrowerAPR and monthly loan payment: Loan original amount has a negative relationship with borrowerAPR and Rate. At different size of the loan amount, the APR has a large range, but the range of APR decrease with the increase of loan amount. Overall, the borrower APR is negatively correlated with loan amount. The Loan original amount also has a strong positive relationship with the monthly loan payment, As the loan amount increases the monthly payment increases positively also.
  
  Looking at relationship between Borrower APR and Prosper Score: Borrowers with the best Prosper scores have the lowest interest rates. This is a strongly negative relationship between Borrower APR and Prosper Score. It means that the Prosper score has a strong effect on borrower APR. So it seems the scores with higher risk tends to have a higher percentage rate(BorrowerAPR).  
 
  Looking at Loan original amount and Prosper score: Loan original amount increases with an increase in Prosper score, which means there's a positive relationship.This also means that borrowers of large amount of loan tends to be at lower risk with prosper.This generally indicates that people who borrows large amount of loan have lower interest rates and also have a lower risk(high score) with prosper. 
  
  Looking at borrower APR and employment status: I found that the borrower APR for employment status 'Full-time' and 'Not-available' had a cancelled borrower APR, this may be due to the fact that they are both very low.looking at the Employment Status plot People who are employed don't necessarily have lower interest rate. But unemployed does have a higher median rate and higher concentrate of frequency are above the median. 
  
  Looking at Term and CreditGrade: I found that there is an interaction between term and CreditGrade and there are only 36 month loans populating on all CreditGrades from AA to NC borrowers.But the C borrowers has the highest 36 months loan. And there is also an interaction between employment status and CreditGrade, Full-time workers has more of B, C, D, E and HR borrowers, But the C borrowers are the highest on Full-time workers.

  Looking at borrowers rate and loan status: There seems to be an increasing borrowers rate from the loan status "Past Due (1-15 days)" to "Past Due (>120 days)".This means the longers the loan is past due, the higher the interest rate prosper gets in return. Loan status- "Past Due (>120 days)" has the highest interest rate with a median of approx. 0.28 and "Past Due (91-120 days)" has second highest rate with a median of approx. 0.26. Loan status- "Completed" has the lowest interest rate with a median of approx. 0.18.

  Looking at the correlation between Loan original amount, Borrower APR and Credit Grade: The loan amount increases with better Credit Grades. The borrower APR decreases with better Grades. People who borrowed a large loan amount tend to have a lower borrower APR, compared to people who borrows less amount.Interestingly, the relationship between borrower APR and loan amount turns from negative to slightly positive when the Credit Grades are increased from HR to AA or better. This may because people with A or AA Grades tend to borrow more money. Increasing APR could prevent them from borrowing even more and maximize the profit. And decreasing APR for people with lower Grades who borrows less money, could encourage them to borrow more.
 
  Looking at the relationship between term, category and loan amount: The median of 12 months term for green loans category has the highest loan amount compared to the other two terms. But 60 months seems to have the highest median of loan amount in almost all the categories, while 12 months has the lowest median of loan amount in approximately all categories. Personal loan, student use, and Not Available categories takes loan for 36 months terms only and the amount seems to be low. This means that generally, all the categories who borrowed a larger amount of loan preferred 60 months term.
 
 Generally, the loan amount is increased with an increase in loan term. Loan amount of borrowers also tends to increase with a better CreditGrade. The borrower APR decreases with the better CreditGrade. Borrowers with the best CreditGrade have the lowest APR. It means that the CreditGrade has a strong effect on borrower APR. Borrowers with better CreditGrade also have larger monthly income and loan amount.Employed, self-employed and full time borrowers have higher monthly income and loan amount than part-time, retired and not employed borrowers.Borrowers with better high scores(i.e with low risk) have a shorter term of 12 months. Full-time and part-time workers have a higher prosper score. Now looking at occupation generally, all occupations prefer to take a loan for a duration of 36 months.
 


## Key Insights for Presentation

For the presentation, I focus on just the influences of BorrowerAPR and leave out most of the features. I started by introducing the
loan variable by selecting the columns of interest, followed by the pattern in BorrowerAPR and StatedMonthlyIncome distribution, then plotted the correlation between ProsperScore and Borrower rates.

Afterwards, I introduce each of the selected variables correlation with each other one by one. To start,
I use the violin plots to show the relationship between ProsperScore and Borrower rates. I'm only looking at
the relationship plot here since ProsperScore affects both the BorrowerRate and BorrowerAPR. The other selected
variables, are covered afterwards, using scatter plot, box plot, regplot and facetgrid.
