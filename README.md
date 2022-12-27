 # AliSyedPortfolio


# [Project 1: Regional departmental sales store recommendations](https://github.com/HassenAliSyed/AliSyedPortfolio)

This is a project that I did during my internship

Data was given to me by infinite code

## Overview of the SQL queries I used in the project
 ![](images/Screenshot%202022-12-27%20at%2001.46.35.png)


![](/boat/1.png)

![](https://github.com/HassenAliSyed/AliSyedPortfolio/blob/main/boat/2.png)

![](https://github.com/HassenAliSyed/AliSyedPortfolio/blob/main/boat/3.png)

![](https://github.com/HassenAliSyed/AliSyedPortfolio/blob/main/boat/4.png)

![](https://github.com/HassenAliSyed/AliSyedPortfolio/blob/main/boat/5.png)

![](https://github.com/HassenAliSyed/AliSyedPortfolio/blob/main/boat/6.png)

![](https://github.com/HassenAliSyed/AliSyedPortfolio/blob/main/boat/7.png)

![](https://github.com/HassenAliSyed/AliSyedPortfolio/blob/main/boat/8.png)

![](https://github.com/HassenAliSyed/AliSyedPortfolio/blob/main/boat/9.png)

![](https://github.com/HassenAliSyed/AliSyedPortfolio/blob/main/boat/10.png)

Data Analysis Using SQL

Show all customer records

SELECT * FROM customers;

Show total number of customers

SELECT count(*) FROM customers;

Show transactions for Chennai market (market code for chennai is Mark001

SELECT * FROM transactions where market_code='Mark001';

Show distrinct product codes that were sold in chennai

SELECT distinct product_code FROM transactions where market_code='Mark001';

Show transactions where currency is US dollars

SELECT * from transactions where currency="USD"

Show transactions in 2020 join by date table

SELECT transactions.*, date.* FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020;

Show total revenue in year 2020,

SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.currency="INR\r" or transactions.currency="USD\r";

Show total revenue in year 2020, January Month,

SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and and date.month_name="January" and (transactions.currency="INR\r" or transactions.currency="USD\r");

Show total revenue in year 2020 in Chennai

SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.market_code="Mark001";
