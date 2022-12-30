 # AliSyedPortfolio

![](https://github.com/HassenAliSyed/AliSyedPortfolio/blob/main/boat/Screenshot%202022-12-30%20at%2000.46.32.png)

# [Project 1: Regional departmental sales store recommendations](https://github.com/HassenAliSyed/AliSyedPortfolio)

This is a project that I did during my internship

Data was given to me by infinite code

## Overview of the SQL queries I used in the project

Show all customer records

![](/boat/1.png)

![](/boat/Screenshot%202022-12-30%20at%2000.46.10.png)

Show total number of customers

![](/boat/2.png)

![](/boat/Screenshot%202022-12-30%20at%2000.46.32.png)

Show transactions for Chennai market (market code for chennai is Mark001

![](/boat/3.png)

![](/boat/Screenshot%202022-12-30%20at%2000.46.45.png)

Show distrinct product codes that were sold in chennai

![](/boat/4.png)

![](/boat/Screenshot%202022-12-30%20at%2000.47.02.png)

Show transactions where currency is US dollars

![](/boat/5.png)

![](/boat/Screenshot%202022-12-30%20at%2000.47.10.png)

Show transactions in 2020 join by date table

![](/boat/6.png)

![](/boat/Screenshot%202022-12-30%20at%2000.47.18.png)

Show total revenue in year 2020,

![](/boat/7.png)

![](/boat/Screenshot%202022-12-30%20at%2000.47.25.png)

Show total revenue in year 2020, January Month,

![](/boat/8.png)

![](/boat/Screenshot%202022-12-30%20at%2000.47.31.png)

Show total revenue in year 2020 in Chennai

![](/boat/9.png)

![](/boat/Screenshot%202022-12-30%20at%2000.47.41.png)

![](/boat/10.png)

![](/boat/Screenshot%202022-12-30%20at%2001.43.47.png)

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
