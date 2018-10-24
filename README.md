### Machine Learning

Course code : CMPE-257 Group name : Seekers
Members :
* Anuradha Rajashekar(012409956)
* Ashwini Shankar Narayan(012506910)
* Nidhi Jamar(010070593)
* Sindhu Goudru Shivanandappa Patil(010823683)

### 1. Data Story
The data in the dataset is from a real Czech bank from 1999. The data is about clients and their
accounts and has relation account, client, disposiiton,permanent order, transaction, loan, credit card
and demographic data. Relations 'loans' and 'credit card' describe some services which bank offers
to its clients. More credit cards can be issued to an account but atmost one loan can be granted for
an account. The business objective is to analyze the transactional behavior of the customers and
predict the loan approval status for the same customers.This is useful in cases where credit card
companies provide pre approved loans for customers based on their payment and other factors.

### 2 . Dataset Selection
Dataset Link : https://data.world/lpetrocelli/czech-financial-dataset-real-anonymized-transactions
(https://data.world/lpetrocelli/czech-financial-dataset-real-anonymized-transactions)

### 3. Data Preparation
In data preparation step, we read and preprocess the data to identify and remove invlaid values such
as ? or NA. Here, we read and parse all the csv files in the dataset using the pandas
dataframe.Pandas provide a unique advantage over other libraries in preprocessing the data by
providing inbuilt APIs for all the math operations on selected row/column or full dataset. If there are
any invalid values, fill it with the median value of the column.

### 4. Identifying a categorical value form one of the columns in our dataset
Here, we are getting to know the possible unique values for status feature in loan dataset and login
frequency in account dataset. The only two features with String values from all the datasets is
'status' from loan and 'account_loginfrequency'. Therefore, we need to convert them to integer
values. From the output, we understand 'status' feature has 4 unique values: 'A', 'B', 'C' and 'D',
where A stands for contract finished, no problem, B stands for contract finished, loan not payed, C
stands for running contract, OK so far and D stands for running contract, client in debt
'account_loginfrequency' - frequency of issuance of statements, has 3 unique values 'POPLATEK
TYDNE', 'POPLATEK MESICNE', 'POPLATEK PO OBRATU' where "POPLATEK TYDNE" stands for
monthly issuance "POPLATEK TYDNE" stands for weekly issuance "POPLATEK PO OBRATU"
stands for issuance after transaction Here, we are using index values of these feature tuples to set an integer value. For example, in 'status' feature class B willbe assigned integer value 0.

### 6. Conclusion
To reiterate, our business use case was to profile customers and understand their ability to payback current loans and their credit card balances to target them for future loan and credit promotions. It is very important to identify defaulters, as it is to identify good customers. Another key requirement for this dataset is to identify defaulters pattern to judge new customers.

We were able to perform clustering to understand multiple groups of similar pattern in our dataset using clustering techniques. We also worked on regression to predict contineous numeric values(loan amount) and classification to understand if the person defaulted a loan that was offered to him.

Key conclusions about our dataset - the dataset has many independent features related to a customer, from other datasets, which could be used inorder to gain more information, but some references(feature explaination) to these information are missing. For example, the date when the assesment was done is missing, which is a vital in describing the reference point for all date related information.

The dataset has more linear features, than nonlinear features.(For example, age is a non linear feature, as it has no mathamatical relation to the loan amount deing differed). Hence our logistic regression method works better than other classificaiton algorithms.

Running all these algorithms on the loan dataset from Czech bank,

we could predict the loan amount using linear regression
we could predict what is the probabality that the customer would default or not using classification.
Based on the above techniques we could identify payment reliability of the prospective customers.
Also, we can target specific customers for various promotions based on these predictions.
