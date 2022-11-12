# (Loan Data From Prosper)
## by (Oyindamola Jimoh)


## Dataset

> This data set contains 113,937 loans with 81 variables on each loan, including loan amount, borrower rate (or interest rate), current loan status, borrower income, and many others.


## Preliminary Wrangling

> out of the 81 columns i choosed the data set i would focus on into a data fram which includes

> ListingNumber: The number that uniquely identifies the listing to the public as displayed on the website.
> Term: The length of the loan expressed in months.
> LoanStatus: The current status of the loan: Cancelled, Chargedoff, Completed, Current, Defaulted, FinalPaymentInProgress, PastDue. The PastDue status will be accompanied by a delinquency bucket.
> BorrowerAPR: The Borrower's Annual Percentage Rate (APR) for the loan.
> BorrowerRate: The Borrower's interest rate for this loan.
> ProsperRating: The Prosper Rating assigned at the time the listing was created between AA - HR. Applicable for loans originated after July 2009.
> ProsperScore: A custom risk score built using historical Prosper data. The score ranges from 1-10, with 10 being the best, or lowest risk score. Applicable for loans originated after July 2009.
> BorrowerState:The two letter abbreviation of the state of the address of the borrower at the time the Listing was created.
> Occupation: The Occupation selected by the Borrower at the time they created the listing.
> EmploymentStatus:The employment status of the borrower at the time they posted the listing.
> IsBorrowerHomeowner: A Borrower will be classified as a homowner if they have a mortgage on their credit profile or provide documentation confirming they are a homeowner.
> IncomeRange: The income range of the borrower at the time the listing was created.
> LoanOriginalAmount: The origination amount of the loan.
> LoanOriginationDate: The date the loan was originated.
> Listing_category: The category of the listing that the borrower selected when posting their listing

### Wrangling
> changed the Loan Origination Date into a date time category created a better representation of the Listing category
> renaming the coulmn names
## Summary of Findings
#### Univariate Exploration
> In the exploration, I found that there was a strong relationship between the betweem borrowers APR and borrowers rate.they had the same plot pattern. which is normal because Borrower Rate pluse other charges make up the Borrower APR. The loan amount collected was widely distributed, between 1000 and slight above 30000 dollars. the prosper Score distrbution showed that it is multimodal, with score 4,6,8 dominaing the population. The employment status distribution depict majority of individuals that applied for the loans are employed and the least being retired individuals. The homeowners distribution was evenly distributed in the population. Large numbers of the borrowers are of the high income range earners. using the log scale, the borrowers who are currently on the loan plan are the highest, followed by those who have completed the loan  and also Majority of the loan was collected for debt consolidation.

#### Bivariate Exploration
> using clusterd bar chart to show the Loan amount been distributed by the Term, The plot shows that 36 term which is 3 years was the highest distribution for all the amount collected except for the 30k upward, which had the 60 term that 5 years slightly higher.Only a few borrowers collected loan for 12 months Term which is for one year,from 25k - 35k amount borrowers didnt opt for the 12 months Loan Term.Generally we can say maybe because of the convenience of payment,most borrowers will prefer not to take the 12 months Loan Term.

> Using a heatmap to show how the LoanAmount affect Borrowers API,The distribution show that a negative correlation exists between the BorrowersAPR and the Loan Amount.So we can conclude that there is higher tendency that borrowers with less than 20,000 USD will have higher APR,while borrowers with more than 20,000 USD have tendency of getting a lower APR. 

> Using the violin plot to show the relationship between loan amount Borrowed and IncomeRange/EmployementStatus,shows that High income earners of between 25,000k-100,000k+ obviously got access to largest sizes of loans,and  employement status is quite related with the income range as well because  employed borrowers accessed higher sizes of loans while part-time and not employed borrowers accessed the smallest sizes of loans.This is a major finding which will be documented in my Explanatory Analysis.

#### Multivariate Exploration
> From the heat map Showing how lower credit ratings, and lower incomes equate to higher returns. It's interesting to see that the income range does not play a big influence on the estimated returns by credit rating category.Across the credit ratings 'AA', 'A', and 'B', we observe no difference in the rate of return for income ranges 1-100k However, there is a definite jump in returns for the 0k income range across all credit rating categories.So we can generally  say that borrowers with higher credit ratings have the lowest estimated return.

> Looking further into the clusterd bar chart in the bivariate while adding Term to the distribution, the plot shows that the longer term(5 years(60Months)) had higher borrower APR. which means the longer the term the individual collect the loan the higher their API gets.

> This two multivariate insight are significant for my explainatory analysis.

### Key Insights for Presentation
> The first multivariate showed that the longer term(5 years(60Months)) had higher borrower APR. which means the longer the term the individual collect the loan the higher their API gets.However,using the credit rating we can say that borrowers with higher credit ratings have the lowest estimated return.
