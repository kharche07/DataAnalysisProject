# Sales Insights using MY-SQL and Tableau

# Data Analysis using SQL

1. Show all tables present in the database.
   ``` 
   select * from customers;
   select * from markets;
   select * from transactions;
   select * from products;
   select * from date; 
       
2. Show total count of transactions,customers,market,product.
   ```
   select count(*) from transactions;
   select count(*) from customers;
   select count(*) from markets;
   select count(*) from products;
   
3. Check transactions for Mumbai market (market code for Mumbai is Mark002). 
   ```
   select * from transactions where market_code = 'Mark002';
   
4. Show transactions in the year 2018.
   ```
   SELECT transactions.*, date.* FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2018;
   
 5. Show total revenue in 2018.
    ```
    SELECT SUM(sales_amount) FROM transactions as t INNER JOIN date as d ON
    t.order_date=d.date where d.year=2018 and t.currency="INR\r" or t.currency="USD\r";
    
6. Show transactions where currency is in "USD".
    ```
    select * from transactions where currency = "USD";
    
7. Show total revenue in the year 2020 in Mumbai(i.e Mark002 is Mumbai).
   ```
   select sum(sales_amount) from transactions t1 inner join date d on
   t1.order_date = d.date where d.year = 2018 and t1.market_code ="mark002"; 
   
   
