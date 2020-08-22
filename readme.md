# Prosper Loan Data Exploration
------------------------------------------------------
## by Donnelly Miller
------------------------------------------------------

## Dataset
------------------------------------------------------
The Prosper loan dataset consists of 113,937 columns and 82 columns. The columns within this dataset consists of qualitative, quantitative and Boolean datatypes. For this data exploration project, I trimmed down the number of columns from 82 down to 25. The reduction in columns made it easier to work with dataset consisting of the variables I found relevant for the project. 

 Prior to doing any exploration, a couple of the columns were renamed to avoid potential type errors. Some of the datatypes were changed over to a categorical datatype. A new column was created that actually displayed the reason for a borrower took out a loan instead of an assigned number as is assigned on the original dataset. Null values for a couple of the numeric datatype columns were filled in with median values over the mean. The reasoning for this was due to some of the outliers as outliers do not tend to affect the median.
The main variables I were interested in were:
 * Upper and lower credit score ranges
 * Number of open credit lines
 * Current delinquencies
 * Employment status
 * Income ranges
 * Debt-to-income ratio
 * Term length of the loan
 * Original Loan amount
 * Scheduled monthly payments
 * Prosper score (1 to 11) with 11 being the lowest risk.
 * Interest rate


## Summary of Findings
-----------------------------------------------------------------------------------------


* Some general statistics were acquired for each of the variables during the univariate data exploration part of the project. Upper and lower credit score ranges showed a normal distribution with most credit scores falling between 650 and 750. Considering that credit scores of 670 or above are considered good based on some credit agencies, it looks like many of Prosper's borrowers have good or excellent credit. 
* Lower and middle-class incomes were the most represented income range in the dataset. There was a wide range of alpha credit ratings and Prosper scores. Debt-to-income ratios of 0.20 to 0.24 were the most frequent in the data set with some outliers having debt-to-income ratios of greater than 0.50. 
  
* Surprisingly, there were borrowers who had many open credit lines and other borrowers who had a high number of delinquencies. Loans in the dollar amount of 1,000 to 10,000 were most common. 
  
* There were still several loans at 15,000, 20,000, or 25,000 or more dollars. Monthly payments for the most part were below 500 dollars with an average at around 170 180 dollars.   
  
* During the bivariate exploration, some key relationships started to become apparent. I focused on using the upper credit score ranges only from this point on. There did appear to be some relationship with credit scores and the status of loans. Credit scores were on average lower for borrowers who defaulted or had charged off loans. Similar outcomes were also noted when comparing the Prosper score with the outcome of loan status. 

* The number of delinquency also appeared to have a small effect on the status of loans. Increased number of delinquencies were associated with loans that had negative outcomes. Debt-to-income ratio did not appear to have impact on loan status. Borrowers with income ranges falling in the ranges of 25,000 to 75,000 dollars made up the greatest count of loans with a current status. 
* One of the key findings in this part of the exploration was the moderate negative correlation between Prosper scores and interests' rate. Higher Prosper scores were associated with lower interests' rates. There was also a negative correlation between credit scores and interests' rates, albeit the correlation was lesser than that with Prosper scores. 
* Original loan amount and monthly payment information did not yield any useful information during this part of the exploration process, but when doing multivariate exploration, there were some indications to suggest high monthly payments increased the risk of a negative outcome for repaying the loan.    


## Key Insights for Presentation
-----------------------------------------------------------------------------------------------------------
* Multivariate exploration gave further indications that a combination of higher income, lower interests' rates, and higher Prosper scores indicated a reduced risk of borrowers not being able to repay the loan. It was also shown that there were some indications that as the monthly payment amount increases the there was an increased risk. This risk seemed to be elevated somewhat as original loan amounts approached 25,000 dollars. 
* The insights gathered from this dataset may help to reinforce that lenders may choose to have higher confidence in borrowers who have the income available to pay off the debt along with the ability to establish good credit and thus have reduced interests rate. Higher credit scores, reduced interests' rates, which can reduce the monthly payment, all seem to indicate borrowers with lower levels of risk. 

## Resources
----------------------------------------------------------------------------------------------------------------------------------------
* https://kanoki.org/2019/04/06/pandas-map-dictionary-values-with-dataframe-columns/
* https://stackoverflow.com/questions/49153253/pandas-rounding-when-converting-float-to-integer
* https://stackoverflow.com/questions/51417483/mean-median-mode-lines-showing-only-in-last-graph-in-seaborn
* https://www.prosper.com/blog/2020/01/16/what-is-a-good-credit-score/
* https://datascience.stackexchange.com/questions/45383/how-to-fill-in-missing-value-of-the-mean-of-the-other-columns
* https://www.w3resource.com/graphics/matplotlib/piechart/matplotlib-piechart-exercise-2.php
* https://stackoverflow.com/questions/28115637/how-to-better-fit-seaborn-violinplots/28119908#28119908
* https://stackoverflow.com/questions/28638158/seaborn-facetgrid-how-to-leave-proper-space-on-top-for-suptitle
* https://www.protechtraining.com/content/python_fundamentals_tutorial-
*https://www.protechtraining.com/content/python_fundamentals_tutorial-functions#:~:text=7.1.&text=A%20function%20without%20an%20explicit,%3E%3E%3E
     
 