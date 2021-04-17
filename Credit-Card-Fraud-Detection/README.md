# Credit Card Fraud Detection
### BUSINESS PROBLEM
Payment card fraud is a growing concern around the world, not only for financial institutions, but also for individuals whose identities may be stolen to commit the fraud. Payment card fraud can be broadly classified into two categories:
1.	Application Fraud 
2.	Transaction Fraud

According to the Federal Trade Commission, there were more than 250,000 reports of credit card fraud in the year 2019. The graph below shows the yearly trend of credit card fraud in the United States for the past five years
 
### OBJECTIVE
In this project, our objective is to curtail credit card transaction fraud by assigning a real-time fraud score to each and every transaction using supervised classification models built using Logistic Regression, Neural Networks, Boosted Trees and Random Forest. The data we used in this project consists of credit card transaction data for all the days in the year 2010, with each record identified either as a fraudulent or genuine transaction.

### PROJECT OVERVIEW
Given below is a high-level outline of the steps we took to achieve the objective of the project:
1.	**Exploratory Data Analysis and Data Cleaning**: The data consists of 10 fields and 96753 records. We only retained the records with transaction type ‘P’(Payment) and imputed some missing values for the fields merchant number, merchant zip code and merchant state. 
2.	**Feature Engineering and Feature Selection**: We engineered features by combining fields such as card number and merchant number with the average/median amount spent in each transaction. We also created days since variables and velocity variables for the combination variables. Among the 343 variables that were engineered, the 30 most relevant features were selected using a random forest wrapper. 
3.	**Building Classification Models and Evaluating Performance**: We divided the data into training, testing and out of time (OOT) sets, and built four classification models using Logistic Regression, Neural Networks, Boosted Trees and Random Forest. The performance of each model was evaluated using the Fraud Detection Rate in the top 3% of the OOT data. 
4.	**Determine the optimal score cutoff to maximize savings**: We assumed a $2000 savings for every fraudulent transaction that was caught and a $50 loss for every false positive. For our best performing model, we calculated the fraud savings, lost sales and overall savings at each score cutoff, above which the transaction will be flagged. The most profitable score cutoff was determined.

The result of the project was that the best classifier was built using a Random Forest Model, which had an average FDR of 59.7% in the top 3% of the OOT data. We recommend a score cutoff at the top 3% of the OOT population, which will result in yearly savings of over $2.2 million.
