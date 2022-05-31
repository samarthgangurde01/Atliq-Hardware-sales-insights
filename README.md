# Project Title:- Atliq Hardware Sales Insights
![image](https://user-images.githubusercontent.com/93859458/171012616-096a1d46-fa86-4c17-be66-9cc8b63e43f1.png)

## Description
In this project, i used the database of AtliQ Hardware. It is a company which supplies computer hardware and peripherals to many clients across India. The company has a head office in Dehli and regional offices throughout India.

I tried to create a real world scenario in which the company's total revenue is declining every year. I used the database provided in the internet. Performed a data analysis and visualization in power BI with mysql database. It has all sales transactions, customers, products and markets information. Developed ETL mapping using SQL to extract the data from unstructured data and transfromed it to the staging area to conduct data cleaning and design star schema in Power BI. Created Dashboard to understand factors affecting on declining revenue. and we focused on Profit and Profit margin distribution in different markets, and different zones too.



## Table of Content
* Description
* Dataset Information
* Tools and Libraries Used
* Files
* Results
* Screenshots
* feedback

## Dataset Informatio
It contains 4 tables customers, date, markets, Products, trasactions.Lets look into features of tables


customers:
* customer_code:It contain code of customer ex.cus001
* Customer_name: It contain name of customer ex.Nomad Stores
* Customer_type: customer type is it E-commerce, Brick & Motar


date:
* date:It contain date of the order
* year:year
* Month_name: month
* date_yy_mm:date in yy mm formate


markets:
* market_code:code of the market ex.Mark001
* market_name:city name
* zone: Is it belongs south,North,Centrtal


Products:
* Product_code:code of the Product ex.Prod001
* product_type:Type of product own brand or distribution


trasactions:
* Product_code:code of the Product ex.Prod001
* customer_code:It contain code of customer ex.cus001
* market_code:code of the market ex.Mark001
* order_date:It contain date of the order
* sales_qty:Quantity of product saled
* sales_amount:amount received in sales
* currancy:is it in $ or RS
* profit_margin_percentage:percentage of the profit margin 
* Profit_margin:profit margin from the product
* cost Price:Price of the product



## Files
* This repository contains files as mentioned below
* db_dumb: It contaon SQL Database 
* Sales_bi: It contain Bi report(BI template)
* 
## Results
###Getting Data insingts from the sql database
* SQL query for viewing all rows from transactions table
```bash
  SELECT * FROM SALES.TRANSACTIONS
```
![image](https://user-images.githubusercontent.com/93859458/171045962-9d8cce32-8133-49ad-aa8a-d3c653d1b700.png)
Here you can see 10 columns like transactions details like product code,customer code, market code etc


* SQL query for viewing details of market places out of india
```bash
SELECT * FROM sales.markets where markets_name in ("New York","Paris")
```
![image](https://user-images.githubusercontent.com/93859458/171045407-a2a7a962-ac65-4efa-958e-2714ba8b13f6.png)



* SQL query for viewing unique currency from transactions table
```bash
SELECT distinct (currency) FROM sales.transactions;
```
 ![image](https://user-images.githubusercontent.com/93859458/171045725-dfbc0225-5756-4201-b87e-60c1745030e9.png)


* SQL query for inner join on date and transactions tables to show transactions table and year from date table
```bash
SELECT transactions.*, date.year FROM sales.transactions inner join date on transactions.order_date=date.date
```
 ![image](https://user-images.githubusercontent.com/93859458/171045584-345a882e-ee5d-40f6-9ac0-964d1ffdbdaf.png)

##We performed ETL steps (Extract,Transform,Load) in power BI
* we loaded the dataset from the sql data base
![image](https://user-images.githubusercontent.com/93859458/171046849-9f6c6fc0-fdcd-4999-ae17-fa513bf2d691.png)

* Designed Star schema for the tables in dataset
![image](https://user-images.githubusercontent.com/93859458/171047218-66a84f00-9da3-4482-b4d5-eac9f724ac25.png)

* Data cleaning(Converting USD amount into rupees)
![image](https://user-images.githubusercontent.com/93859458/171047773-36fc9f75-8ced-4af1-9bc5-235ee5ef243b.png)

* Finall powerBI Dashboard
Sales insights of year 2019
![image](https://user-images.githubusercontent.com/93859458/171049309-f00367d0-96cf-4ef3-958d-b83dce85ba98.png)



Sales insights of year 2020
![image](https://user-images.githubusercontent.com/93859458/171049506-c438fdb4-58c8-45da-bfa3-ce951c7a87c3.png)

## Feedback

If you have any feedback, please reach out to us at 
Gmail:- samarthgangurde01@gmail.com
Linkedin:-https://www.linkedin.com/in/samarth-gangurde-b07875212/


