                                                               ASSIGNMENT 1
Introduction:
I undertook an analysis of data from a Portuguese banking institution's direct marketing campaigns. This multivariate dataset covers 45,211 clients across 17 attributes, detailing their personal characteristics and their interactions with the bank's marketing efforts. My objective is twofold:
Segmentation using K-means Analysis: To identify distinctive customer groups based on their shared characteristics.
Prediction with Logistic Regression: To determine the likelihood of a client subscribing to a term deposit.
Through this study, I aim to offer the bank actionable insights on customer behaviors and recommendations on optimizing their marketing expenditures.
Methodology: 
In this analysis, I employed a structured methodology to understand the engagement of clients with the Portuguese banking institution's marketing campaigns, especially focusing on their likelihood to subscribe to a term deposit.
1.Data Preparation & Exploration:
Tool & Libraries: I used Python as our primary tool and employed libraries such as numpy, pandas, seaborn, and matplotlib for data manipulation and visualization.
Data Loading: The dataset was loaded into a pandas DataFrame, considering ';' as the delimiter.
Data Quality Check: Initial data inspection using df.info() provided a quick overview of columns and their data types. I identified missing values with df.isna().sum() to ensure completeness. Also, to ensure the uniqueness of the data, I searched for duplicate entries using df.duplicated(). After identifying them, these duplicates were promptly dropped from the dataset.
2. Exploratory Data Analysis (EDA):

A) Job-wise Distribution: This dataset represents the number of individuals contacted during direct marketing phone campaigns by a Portuguese banking institution, segmented by their job roles and whether they accepted a term deposit. The "admin." category had the most contacts, with 10,419 individuals, followed by "blue-collar" and "technician" roles. The least contacted category was labeled "unknown", with only 330 individuals. Across all categories, only a small fraction of the contacted individuals subscribed to the term deposit. Students alone have shown up in good numbers in the subscription policy with repect to no of students conatacted.
 

B)Education-wise Distribution: This dataset represents the number of individuals contacted during direct marketing phone campaigns by a Portuguese banking institution, segmented by their educational level and whether they accepted a term deposit. The category "university.degree" had the most contacts, with 12,164 individuals, followed by "high.school" with 9,512, and then "basic.9y" with 6,045 individuals. The least contacted education level was "illiterate", with only 18 individuals. Across all educational levels, only a small fraction of the contacted individuals subscribed to the term deposit.
 
C)Martial-wise Distribution: This dataset represents the number of individuals contacted during direct marketing phone campaigns by a Portuguese banking institution, segmented by their marital status and whether they accepted a term deposit. The "married" category had the most contacts, with 24,921 individuals, followed by "single" with 11,564, and then "divorced" with 4,611 individuals. The least contacted category was labeled "unknown", with only 80 individuals. Across all marital statuses, only a small fraction of the contacted individuals subscribed to the term deposit.
 
D)Contingency Table:
 
 
1)Ceontact
•	Cellular Contact:
No (0.852611): Approximately 85.26% of the clients who were contacted via a cellular phone declined the offer for a term deposit.
Yes (0.147389): Approximately 14.74% of the clients who were contacted via a cellular phone agreed to subscribe to a term deposit.
•	Telephone Contact:
No (0.947676): Approximately 94.77% of the clients who were contacted via a landline telephone declined the offer for a term deposit.
Yes (0.052324): Only about 5.23% of the clients contacted through a landline telephone agreed to subscribe to a term deposit.
From this data, we can draw several conclusions:Higher Success with Cellular Contact: There's a higher rate of positive responses (subscriptions) from clients when they are contacted via cellular phones compared to landline telephones. Nearly 15% of cellular contacts led to subscriptions, while only around 5% of telephone contacts did.
2)Personal loan :This data shows the customer taking a personal loan  or not doesnt affect the chance of him/her subscribing for term deposit
3)Housing loan:This data shows the customer taking a hosuing loan  or not doesnt affect the chance of him/her subscribing for term deposit
4)Default:people with no default credit seem to subscribe for term deposit.
5)Month:
High Success in December and March: Notably, December and March have the closest ratios of acceptance to rejection,with almost half of the clients agreeing to the term deposit. This could be due to year-end financial planning in December and financial year-end considerations in March.
Lowest Conversion in May,june,jul,aug,april,nov: these months have the lowest success rate with only about 6.44% of clients agreeing for the deposit. The bank might need to re-evaluate their strategy for these month
Moderate Success in october and september:The bank can target these months apart from december and march to get customers sign the subscriptions
6)dayofweek:This data shows the customers last contact day of the week doesnt affect the chance of him/her subscribing for term deposit

E)Correlation matrix:
 ![my image](image2.webp)
High Positive Correlation:
•	emp.var.rate and euribor3m: 0.972244. This indicates that the employee variation rate and the euribor 3 month rate move almost in unison. As one increases, the other is also likely to increase.
•	emp.var.rate and nr.employed: 0.906949. The employee variation rate and the number of employees are also positively correlated.
•	euribor3m and nr.employed: 0.945146. The euribor 3 month rate and the number of employees are strongly positively correlated.
•	emp.var.rate and cons.price.idx: 0.775293. The employee variation rate and the consumer price index have a positive correlation.
•	cons.price.idx and euribor3m: 0.688180. The consumer price index and the euribor 3 month rate are positively correlated.
High Negative Correlation:
•	pdays and previous: -0.587508. The number of days since the last contact and the number of times a client was contacted before this campaign have a negative correlation.
•	previous and emp.var.rate: -0.420587. The number of times a client was contacted before this campaign and the employee variation rate are inversely correlated.
•	previous and euribor3m: -0.454571. The number of times a client was contacted before this campaign and the euribor 3 month rate also have a negative correlation.
•	previous and nr.employed: -0.501411. The number of times a client was contacted before this campaign and the number of employees are inversely related.
Columns to Consider for Combination or Elimination:
•	euribor3m and nr.employed (correlation: 0.945146) and emp.var.rate and nr.employed (correlation: 0.906949) are  pairs that are highly correlated. When two or more variables are highly correlated, they might convey similar information, and hence, retaining all of them might not add much value.

