# IN PROGRESS
# Data Analysis-Superstore Sales Tableau

## Dashboard 
Can be found at my [Tableau Public](https://public.tableau.com/app/profile/lori.bettencourt) site.

## Data Prep
Working with previously cleaned and formatted data 

## Metadata Observations/Assumptions
* 'Quantity' is accounted for in 'Sales' column
* 'Discount' is a perenctage taken already reflected in 'Sales' column.
* Discount taken = Discount * Sales/(1-Discount) or computed Orig_Price - Sales

## Sales Dashboard
### Overview of Calculations
1) Avg order value =  Sum(sales)/countd(order id)
2) Avg basket size = qty/orders = Sum(quantity)/countd(order id)
3) Fulfillment days
    Min(Ship Date - Order Date)
    Avg(Ship Date - Order Date)
    Max(Ship Date - Order Date)
4) Avg order discount (%) = Avg(discount) = AVG(disc_amt/orig_price)
5) Avg profit/order = Avg(order profit) = sum(profit)/countd(order id)
6) Avg discount/order ($) = Avg(order disc_amt) = sum(disc_amt)/countd(order id)

* Filter by Date, Category, and Sub-Category where appropriate.

## SQL Checks  
Queries against the dashboard reports can be reviewed at [SQLChecks.txt](/SQLChecks.txt)

## Resources
[Luke Barosse's: My Tableau tutorial playlist](https://www.youtube.com/playlist?list=PL_CkpxkuPiT_sRLeU_5JSArjc0P1lGU2_)  (options/formatting)  
[Tableau Superstore Data Set](https://docs.google.com/spreadsheets/d/1rAZkrxrtO1LQd7Lw61jXta0A7Bj5lFtn3LPRzcVxqhI/edit#gid=1824808968)  (data)  
[How to Create a Single Column Hierarchy Drill Down Drill Up with Parameter Actions](https://www.youtube.com/watch?v=L140GRsQ-mY&list=PLdeA_5rmA1Ecl1MnWUsyuV3IjiPSOqbU7&index=12) (for category/sub-category drill down)  
[Method 1: Insert a Hyperlink onto your Tableau Dashboard using textual/sheet with Actions](https://www.youtube.com/watch?v=-Mtb3WPBPSM) (for links)  
[Tableau KPI dashboard Design for Business Dashboards](https://www.youtube.com/watch?v=WT-8TLEXpF4&list=PLdeA_5rmA1Ecl1MnWUsyuV3IjiPSOqbU7&index=13&t=469s) formatting  
[](https://btprovider.com/how-to-disable-default-highlighting-in-tableau/)  
[How To Create a Filter for Start and End Dates Using Parameters in Tableau](https://www.youtube.com/watch?v=hMsQ8TvVjo4) (date filters - applied to all sheets)  
[Coursera](https://www.coursera.org/)  
[Google Data Analytics Certificate Course](https://www.coursera.org/professional-certificates/google-data-analytics?utm_source=gg&utm_medium=sem&utm_campaign=15-GoogleDataAnalytics-US&utm_content=B2C&campaignid=12504215975&adgroupid=122709142687&device=c&keyword=coursera%20data%20analytics%20course&matchtype=b&network=g&devicemodel=&adpostion=&creativeid=504570191916&hide_mobile_promo&gclid=Cj0KCQjw94WZBhDtARIsAKxWG--aGc_mpu7WTeU8sHtAVT4D9k79qOSJOCdgcl3hVUqPH2zR1B2j8acaAovsEALw_wcB)  

