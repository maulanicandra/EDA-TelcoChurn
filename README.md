# EDA-TelcoChurn
Making Comprehensive EDA for https://www.kaggle.com/blastchar/telco-customer-churn

Target variable is called Churn - it represents customers who left.
Predictor variables include all the remaining variables.

Data Observation:
1. Many column are categorical, except tenure, MonthlyCharges, TotalCharges
2. Variable gender, Partner, Dependents, PaperlessBilling, Churn seems to contain two distincts values (Male of Female, Yes or No), but we will confirm later.
3. PhoneService, MultipleLines, InternetService, OnlineSecurity, OnlineBackup, DeviceProtection, TechSupport, StreamingTV, Contract seems to contain three distincts values, PaymentMethod seems to contain four distinct value, but we will confirm later. 
4. SeniorCitizen seems to contaion binary values (0,1).
5. TotalCharges data type is object.
6. No obvious defect on the data (column name vs its entries), all looks good.

Result:
1. No outlier found.
2. Total Charge is skewed right.
3. tenure can be split into two distribution.
4. MonhtlyCharge distribution graph can not be described (at least by me :D) 
5. SeniorCitizen has boolean value, 0 and 1.
6. TotalCharges, MonthlyCharges, and tenure are highly correlated each other.

Deep Dive Observation Result:
1.  Mostly customers do not churn, only 26.6% (1869) of Customers churn.
2.  Gender: There is barely any difference in churn percentage between men and women;
3.  Senior Citizen: The number of customer churn for senior customers are high (476 of 1142), indicating a high likelihood of churn from that group;
4.  Partner: Single customers are more likely to churn than customers with partners;
5.  Dependents: Customers with dependents are less likely to churn than customers without any dependents.
6.  The group of people with partners and dependents and the group with neither of those are on the extremes in terms of likelihood of churn.
7.  The difference of churn between clients with (1699/4653) and without phone services (170/510) is quite small, been negligible if we take those with multiple lines out of equation.
8.  In the feature ‘InternetServices’, the percentage of churn in each category is highly different one from another. Those who don’t subscribe to the company’s internet (presumably, they only use their phone service), are the most likely to endure as their customers. The likelihood of churn from customers with DSL service is also smaller than the overall probability.
9.  The highest number of customer churn (1297/1799), is from customers with fiber optic internet. Fiber optic tends to be faster than DSL internet.
10.  Tech Support and OnlineSecurity don’t seem to affect the subscription charges by much.
11.  The highest churn rate is from the ‘month-to-month’ type, which is also the most dominant contract.
12.  The high chance of churn from customers who choose electronic check as payment method and opts for paperless billing.
13.  That most customers in the month-to-month contract also fall into those categories. Need further check.
14.  PaperlessBilling is highest at monthly payment regardless the payment methods.
15.  The likelihood of churn is highest in montly payment regardless of type of contract.
16.  Mostly, customers who do not have internet connection prefer to use mailed check (conservative).
17.  Customers who have Fiber Optic connection prefer to use Electronic check or automatic check.
18.  Customers who have DSL connection tend to use all check methods.
19.  Tenure: High concentration of the customers churn in the first months
20.  Monthly Charges: High concentration of the customers churn in higher values (around 60 and beyond)
21.  Total Charges: has similar distribution
