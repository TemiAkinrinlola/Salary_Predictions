# Salary_Predictions

Accoding to Wikipedia,a salary is a form of payment from an employer to an employee, which may be specified in an employment contract. It is contrasted with piece wages, where each job, hour, or other unit is paid separately, rather than on a periodic basis. From the point of view of running a business, salary can also be viewed as the cost of acquiring and retaining human resources for running operations, and is then termed personnel expense or salary expense.

The current salary of an employee is determined by so many factors.Salary is determined by leveling the pay rates and salary ranges established by an individual employerand often, salary is affected by the number of people available to perform the specific job in the employer's employment locale.Typically,salary is determined by comparing market pay rates for people performing similar work in similar industries in the same region.

Most times,when job advertisements are posted online,the employer neglects to mention the salary but salary information is often an important factor in deciding whether a certain job position at a certain company is a good fit.

This projects evaluates the perfomance of certain machine learning models in predicting salary based on some obtained salary historical data.


## The Data
The training data used here contains past information about salary for different employees across different job types,location,industries and degree majors.
It basically contains variables such as jobId(unique description of the jobtype expressed as a categorical information),the salary (the amount paid to the end of the usual contract),the jobtype(this include Vice president,CFO,CTO,Manager,Junior Associate,etc),degree(the highest degree held by the employee),years of experience,the distance from the metropolis,the major of the employee,the industry where the employee seeks to be employed and the companyID(which represents a unique description of every company in the data).


## Exploratory Analysis
Exploratory analysis shows other important signicant information about the historical data including that the data has 10000 rows and 9 columns as well as that the distribution is relatively symmetrical and the outliers are relatively small.There is the presence of some missing data needing some form of rectification.Other notable information is that :

1.CEOs earn the highest salary,followed by CTOs and CFOs.

2.Employees with doctoral degrees earn more than others.

3.The finance and oil industries are the highest paying industries.

4.Business and Engineering major holders earn the most.

5.The categories seem to be evenly distributed,we can say we have a balanced dataset.

6.MilesfromMetroplolis and YearofExperience are linearly related to salary.

## Data Preprocessing 
This requires one -hot encoding to convert categorical variables to dummy variables as most machine learning models cannot accept data with categorical data.Other data processing techniques involved dealing with missing values,identifying the target variable amongs others.

## Model Development
Here,we explore several models with multiple linear regression as the baseline model since data exploration indicates the presence of some linear relationships with the target data (salary).Other machine learning models include DecisionTreeRegressor and GradientBoostingRregressor where the GradientBoostingRregresor outperformed other to produce the least root-mean-squared error.

## Deployment
The choice model(GradientBoostingRegressor) is selected to produce the target variables(salaries) for the test dataset(features) and stored as a csv file.

## Feature Importance 
An investigation into the feature importance shows that the top three variables that contributed to the prediction of the salary of the employee include jobType,milesFromMetroplois and YearsOfExperience.
