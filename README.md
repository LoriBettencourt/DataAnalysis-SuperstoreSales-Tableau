# IN PROGRESS
# Data Analysis-Superstore Sales Tableau

# Currently working on this at my [Tableau Public](https://public.tableau.com/app/profile/lori.bettencourt) projects site.

## Data Prep
Working with previously cleaned and formatted data 

## Metadata Observations/Assumptions
* 'Quantity' is accounted for in 'Sales' column
* 'Discount' is a perenctage taken already reflected in 'Sales' column.
* Discount taken = Discount * Sales/(1-Discount)

## Sales Dashboard
Sales
1) Avg days to ship = Avg(Ship Date - Order Date)
2) Avg order value =  Sum(sales)/countd(order id)
3) Avg basket size = qty/orders = Sum(quantity)/countd(order id)
4)Avg profit/order = Avg(order profit) = sum(profit)/countd(order id)
5) Avg discount = Avg(order discount) = sum(discount amt)/countd(order id)
6) Avg discount %
Commission per Sales Rep
* Options to Group by segment
* Filter by date

## Resources
[Luke Barosse's: My Tableau tutorial playlist](https://www.youtube.com/playlist?list=PL_CkpxkuPiT_sRLeU_5JSArjc0P1lGU2_)  (options/formatting)  
[Tableau Superstore Data Set](https://docs.google.com/spreadsheets/d/1rAZkrxrtO1LQd7Lw61jXta0A7Bj5lFtn3LPRzcVxqhI/edit#gid=1824808968)  (data)  
[How to Create a Single Column Hierarchy Drill Down Drill Up with Parameter Actions](https://www.youtube.com/watch?v=L140GRsQ-mY&list=PLdeA_5rmA1Ecl1MnWUsyuV3IjiPSOqbU7&index=12) (for category/sub-category drill down)  
[Method 1: Insert a Hyperlink onto your Tableau Dashboard using textual/sheet with Actions](https://www.youtube.com/watch?v=-Mtb3WPBPSM) (for links)  
[Tableau KPI dashboard Design for Business Dashboards](https://www.youtube.com/watch?v=WT-8TLEXpF4&list=PLdeA_5rmA1Ecl1MnWUsyuV3IjiPSOqbU7&index=13&t=469s) formatting  
[Coursera](https://www.coursera.org/)\
[Google Data Analytics Certificate Course](https://www.coursera.org/professional-certificates/google-data-analytics?utm_source=gg&utm_medium=sem&utm_campaign=15-GoogleDataAnalytics-US&utm_content=B2C&campaignid=12504215975&adgroupid=122709142687&device=c&keyword=coursera%20data%20analytics%20course&matchtype=b&network=g&devicemodel=&adpostion=&creativeid=504570191916&hide_mobile_promo&gclid=Cj0KCQjw94WZBhDtARIsAKxWG--aGc_mpu7WTeU8sHtAVT4D9k79qOSJOCdgcl3hVUqPH2zR1B2j8acaAovsEALw_wcB)  

