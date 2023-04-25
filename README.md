# EDA Bank Project

understanding of risk analytics in banking and financial services and understand how data is used to minimise the risk of losing money while lending to customers

Business Understanding

The loan providing companies find it hard to give loans to the people due to their insufficient or non-existent credit history. Because of that, some consumers use it to their advantage by becoming a defaulter. Suppose you work for a consumer finance company which specialises in lending various types of loans to urban customers. You have to use EDA to analyse the patterns present in the data. This will ensure that the applicants capable of repaying the loan are not rejected.

When the company receives a loan application, the company has to decide for loan approval based on the applicant’s profile. Two types of risks are associated with the bank’s decision:

If the applicant is likely to repay the loan, then not approving the loan results in a loss of business to the company

If the applicant is not likely to repay the loan, i.e. he/she is likely to default, then approving the loan may lead to a financial loss for the company. The data given below contains the information about the loan application at the time of applying for the loan. It contains two types of scenarios:

The client with payment difficulties: he/she had late payment more than X days on at least one of the first Y instalments of the loan in our sample,

All other cases: All other cases when the payment is paid on time. When a client applies for a loan, there are four types of decisions that could be taken by the client/company):

Approved: The Company has approved loan Application

Cancelled: The client cancelled the application sometime during approval. Either the client changed her/his mind about the loan or in some cases due to a higher risk of the client, he received worse pricing which he did not want.

Refused: The company had rejected the loan (because the client does not meet their requirements etc.).

Unused offer: Loan has been cancelled by the client but at different stages of the process.

We will use EDA to understand how consumer attributes and loan attributes influence the tendency to default.

Business Objectives

To identify patterns which indicate if a client has difficulty paying their instalments which may be used for taking actions such as denying the loan, reducing the amount of loan, lending (to risky applicants) at a higher interest rate, etc. This will ensure that the consumers capable of repaying the loan are not rejected. Identification of such applicants using EDA is the aim of this case study.

In other words, the company wants to understand the driving factors (or driver variables) behind loan default, i.e. the variables which are strong indicators of default. The company can utilise this knowledge for its portfolio and risk assessment.

Approach:

Initial data inspection (null value, shape, and summary check)
Inspecting the existing variables for consistency, data types, etc
Univariate analysis (includes histograms, boxplots, finding statistical metrics like mean, mean median, etc.)
Bivariate analysis (includes scatterplots, pairplots, correlation matrix, heatmaps, etc.)
Deriving new variables
Data quality issues have been taken care of. Variables like 'DAYS_BIRTH', 'DAYS_REGISTRATION','DAYS_ID_PUBLISH' are converted into the correct format
divided the data into 2 categories with target = 0 and 1, This was important as there was a huge data imbalance in the dataset, hence you should analyze both of them separately and try to find any relationship
compared the target variable across categories of categorical and continuous variables, Good work, However, you can also generate these additional insights from the variables and their plots
CODE_GENDER: Less number of males(hist plot) take loans but the defaulters are higher in the case of males(dist plot).
NAME_INCOME_TYPE: Pensioner defaulter is lower than non-defaulter.
NAME_EDUCATION_TYPE: Most clients take loans for secondary education followed by higher education. But the default rate in secondary education is much higher and for higher education is much lower.
NAME_FAMILY_STATUS: Most married people apply for loans, and mostly they are not defaulters. Single and civil marriage turns out to be more defaulter.
OCCUPATION_TYPE: Laborers and different categories of staff mostly take the loan, but the managers and the highly skilled tech staffs are the most reliable.
compared the correlation and found the top-10 correlated pairs of variables for each target
joined the previous application dataframe to the current dataframe using 'SK_ID_CURR' as the primary key.
Insights

Bivariate analysis has been done. These are some of the additional inferences that you can generate from the plots
People tend to make more loans for 'Secondary special' and their loan is also approved.
You can see, there is a clear difference between the categories for "Approved, Refused, Unused, and Cancelled" for the category: Married. Married people tend to pay loans on time than Singles.
You can see, there is a clear difference between the categories for "Approved, Refused, Unused, and Cancelled" for the category: House/apartment.
Business Entity Type 3 and Self-employed tends to be the maximum defaulter
