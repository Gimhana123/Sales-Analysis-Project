## Sales Insights Data Analysis Project

<div style="text-align: center;">
  <img src="https://github.com/Gimhana123/Sales-Analysis-Project/blob/main/Screenshot%20(1064).png?raw=true">
</div>


This repository contains the code and resources for a comprehensive sales dashboard project using Power BI. The dashboard visualizes key sales metrics, providing insights into revenue, quantity sold, profit margins, and top products and customers across different markets.

### Data Analysis Using SQL

1. Show all customer records

    `SELECT * FROM customers;`

2. Show total number of customers

    `SELECT count(*) FROM customers;`

3. Show transactions for Chennai market (market code for chennai is Mark001

    `SELECT * FROM transactions where market_code='Mark001';`

4. Show distrinct product codes that were sold in chennai

    `SELECT distinct product_code FROM transactions where market_code='Mark001';`

5. Show transactions where currency is US dollars

    `SELECT * from transactions where currency="USD"`

6. Show transactions in 2020 join by date table

    `SELECT transactions.*, date.* FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020;`

7. Show total revenue in year 2020,

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.currency="INR\r" or transactions.currency="USD\r";`
	
8. Show total revenue in year 2020, January Month,

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and and date.month_name="January" and (transactions.currency="INR\r" or transactions.currency="USD\r");`

9. Show total revenue in year 2020 in Chennai

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020
and transactions.market_code="Mark001";`


## Features

- **Revenue Analysis**: Visualize total revenue and revenue distribution across various markets.
- **Quantity Analysis**: Track the quantity of products sold in different markets.
- **Profit Margin**: Calculate and display profit margins and contributions by market.
- **Top Products and Customers**: Identify top-performing products and key customers driving sales.
- **Temporal Analysis**: Analyze sales performance over different time periods (years and months).

## Measures and Calculations

The following measures were used in the dashboard:
- **Total Revenue**: Sum of revenue from all sales transactions.
- **Total Quantity**: Sum of the quantity of products sold.
- **Profit Margin**: (Total Revenue - Total Cost) / Total Revenue.
- **Revenue by Market**: Sum of revenue for each market.
- **Quantity by Market**: Sum of the quantity sold for each market.
- **Top Products**: Products with the highest sales revenue.
- **Top Customers**: Customers with the highest sales revenue.



## Conclusion

The Sales Dashboard project offers a robust solution for visualizing and analyzing key sales metrics. By leveraging Power BI, users can gain valuable insights into revenue distribution, sales quantities, and profit margins across different markets. The detailed analysis of top products and customers further aids in strategic decision-making. This project demonstrates the power of data visualization in driving business insights and optimizing sales performance.
