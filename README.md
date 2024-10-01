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

The dataset had no **churn** column. 

I was able to predict the **churn** column using some Python syntax importing Pandas and Numpy.

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

- Which customer demographics are most likely to churn
- What are the key factors contributing to customer churn
- How does product engagement affect churn
- Are there common patterns among customers who churn across multiple products
- What are the geographical trends of churn
- What is the lifetime value of customers who churn compared to those who stay
- What retention strategies can reduce churn for each financial product
- How does product ownership impact the likelihood of churn
- What is the effect of customer engagement with digital channels
