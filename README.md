
# Olist Data Pipeline

I built this small data pipeline to practise SQL and Python on a real dataset: the Brazilian E-Commerce Public Dataset by Olist, from Kaggle. I wanted to go beyond analysing data in a dashboard and handle the full path from raw files to answers.

## How it works
1. **Load the data.** I read 7 CSV tables into pandas: orders, customers, items, payments, reviews, products and sellers.
2. **Clean and combine.** I turned the date columns into real dates and kept only delivered orders. I worked out how many days each delivery took and whether it arrived by the estimated date. Because one order can have several items, payments or reviews, I summarised each table to one row per order before joining them into a single table.
3. **Store it in a database.** I wrote the raw tables and my cleaned table into a SQLite database.
4. **Ask questions with SQL.** I used JOIN, GROUP BY and date functions to answer questions about delivery, reviews and sales.

## The data
There are 99,441 orders in total. After cleaning, 96,470 are delivered orders.

## What I found
- 91.9% of delivered orders arrived by the estimated date.
- Remote states wait much longer for delivery: RR takes 29.0 days on average, AP 26.7 and AM 26.0, compared with 8.3 days in SP.
- That wait is already built into the promise. Olist tells customers in RR, AP and AM to expect about 45 to 46 days, so most of those orders still arrive early.
- The weakest on-time rates are in AL (76.1%) and MA (80.3%). RJ stands out for volume: 12,350 orders, with 86.5% on time.
- Late orders get much lower reviews. They average 2.57, compared with 4.29 for on-time orders.
- One order from September 2016 has no payment record, so its revenue shows as empty.

## Tools
Python, pandas, SQLite, SQL and Kaggle Notebooks.

## What I'd do next
- Build a dashboard for these results in Power BI or Tableau.
- Look at why AL and MA have lower on-ti O
