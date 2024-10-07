# Bank-Churn-Report
***
![](https://media.licdn.com/dms/image/D4D12AQFwIuqMsdB1JQ/article-cover_image-shrink_600_2000/0/1698802120424?e=2147483647&v=beta&t=fSS462PL0QMBLmY4YJONip6brMx9sf4a-Q1fv7Y8tBo)

## Introduction

This is a power BI project on bank churn analysis of a supposed bank located at **Southern California**.

The Project is to predict churn and drive data driven decisions for retention.

_**Disclaimer**_: _The dataset here does not represent any company or organization that I know of, this dataset was explored to showcase my knowledge in Data 
analysis._


## Problem Statement
- Predicting customer churn in financial products
- Identifying key factors influencing churn
- Improving retention strategies for financial products
- Evaluating the impact of customer demographics on churn

## Skills utilized

**1. Power BI**
- DAX
- Quick Measures
- Buttons
- Filters
- Modelling

**2. Python**
- Pandas
- Numpy


## Modelling

My dataset consisted of 1 table, I created new tables from the existing table to enhance the relationship.

![](https://github.com/oluwagbemiga01/Bank-Churn-Report/blob/main/model%20view.jpg)


## Visualization

**Overview of the Dashboard**

![](https://github.com/oluwagbemiga01/Bank-Churn-Report/blob/main/Bank%20churn%20snip.jpg)

_You can interact with the report [here](https://app.powerbi.com/links/JWdQwjmpO9?ctid=1bc1741c-5767-404b-b0f7-2402c36c6b5a&pbi_source=linkShare)_ 


## Data Exploration and Analysis


### Data Cleaning

The dataset was firstly imported to my jupyter notebook using [Visual Studio Code editor](https://code.visualstudio.com/Download).

Initially, the dataset had no **churn** column. 

But I was able to predict the **churn** column using some Python syntax by importing Pandas and Numpy.

![](https://github.com/oluwagbemiga01/Bank-Churn-Report/blob/main/churn%20prediction.jpg)


After that, I exported the dataset to csv format, _check below_

![](https://github.com/oluwagbemiga01/Bank-Churn-Report/blob/main/exported%20csv%20file.jpg)


This led me to exporting the csv file to Power Query in Power BI

**In Power Query, I made the following changes:**

1.  Checked for blank cells and missing values using the column quality check.
   
2.  Renamed the following column name:
   - Customer -> Customer ID
   - Online Presence -> Online Activity Status
   - Income Amount -> Annual Income
   - Personal Loan -> Personal Loan Status
   - Mortgage -> House Mortgage Value
   - Family -> Family Size

3. 	Renamed the following columns that contained binary values ( 0 and 1 )
   - Personal Loan Status ( 0 – rejected, 1 – accepted )
   - Securities Account ( 0 – NoSecurityAcc, 1 – Has a SecurityAcc )
   - Online Activity Status ( 0 – Inactive, 1 – Active )
   - Credit Card Status ( 0 – Not Owned, 1 – Owned )
   - Churn Status ( 0 – Not Churned, 1 – Churned )

4. 	Grouping of values using conditional column
   - Annual Income : ( < 20$, 20$ - 50$, 51$ - 100$, 101$ - 150$, 151$ - 200$, > 200$ )
   - Age Group : ( <25, 26 – 30, 31 – 35, 36 – 40, 41 – 50, 51 – 60, 61 – 70 )
   - Avg CC Spending : ( 0$, 0.1$ - 0.5$, 0.6$ - 1$, 1.1$ - 2$, 2.1$ - 5$, 5.1$ - 10$ )

![](https://github.com/oluwagbemiga01/Bank-Churn-Report/blob/main/renamed%20columns%20%26%20values.jpg)



### Questions For Analysis

1. Which customer demographics are most likely to churn (age, income, education level)
2. How does product engagement affect churn
3. Are there common patterns among customers who churn across multiple products
4. What are the geographical trends of churn
5. How does product ownership impact the likelihood of churn


---


**DATA INSIGHTS**


Following the exploratory data analysis of the customer churn data, the following insights were gotten:

1. **CUSTOMER DEMOGRAPHICS**


**Age**

Looking at the age range in respect to churn rate


![](https://github.com/oluwagbemiga01/Bank-Churn-Report/blob/main/churn%20rate%20by%20age%20groups.jpg) 


- Customers within the age range of 25 and below have the highest churn rate of 64.5%
- Customers within the age range of 26-30 have the least churn rate of 54.8%
- While other age range (31-35, 36-40, 41-50, 61-70) have a churn rate ranging between 57.0% to 58.9%


**Income**

Let us look at the annual income of the customers in relation to the churn rate


![](https://github.com/oluwagbemiga01/Bank-Churn-Report/blob/main/Churn%20rate%20to%20annual%20income.jpg)


- Customers who earn within 0$ to 100$ annually have the highest churn rate.
- While customers who earn above 100$ to 200$ and above have the lowest churn rate.


**Education Level**


Looking at the **education level** from the customer dataset


![](https://github.com/oluwagbemiga01/Bank-Churn-Report/blob/main/churn%20rate%20by%20education.jpg)


- This is showing us that **Graduates** and **Professionals** have less churn rate than **Undergraduates**
