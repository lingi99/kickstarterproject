# kickstarterproject
Objective: Predict whether a kick-starter project will be successful before it is released :)

Open-source Library Used:
- pandas #for converting csv to dataframe, data analysis
- sklearn #for logistic regression and metrics

Dataset:
- obtained from https://www.kaggle.com/datasets/kemical/kickstarter-projects
- consisting of 15 variables (ID,name,category,main_category,currency,deadline,goal,launched,pledged,state,backers,country,usd pledged, usd_pledged_real,usd_goal_real)
- created new variables named 'usd_difference', difference between usd_pledged_real and usd_goal_real, to see whether goals are met
- consisting of 378661 records
- records with states of 'successful' and 'failed' are used in the prediction model
- records with N.A entries are removed using #.dropna() from pandas
- states of 'successful' and 'failed' are converted to binary values 1 (successful) and 0 (failed) for prediction purposes

Prediction Model:
- Logistics Regression
- 70% of data used for training, 30% of data used for testing
- accuracy of 99.8%, recall of 100%, precision of 99.7%
