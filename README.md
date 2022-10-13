# BEGAN ANALYSIS - Will polish up and complete tomorrow (10/13).
# Data Analysis-Superstore Sales Tableau

## Dashboard for this analysis can be found at my [Tableau Public](https://public.tableau.com/app/profile/lori.bettencourt) site.

## Scenario
The Superstore company has tracked its sales order data from 1/1/2016 through 12/13/2019. They have asked for a dashboard that will show 
* Averages in dollars of order value, order profit, and discount amounts AND
* Averages order discount percentage AND
* Minimum, Average, and Maximum fulfillment days AND
  - when Category, Sub-Category, and Date Range values are chosen 
* Overall average Basket size 

## Business Task
We have been asked specifically to look for the following and deliver suggestions based on our findings for the past sales year: 
1) Category / Sub-Category combinations with  
   a) lowest average order value  
   b) lowest average order profit  
   c) highest average order discount amount  
   d) highest average order discount percentage  
2) Average order size  
3) Minimum, Average, and Maximum fulfillment days  

# Response to Business Task
Note: Superstore has a total of 17 product sub-categories.  
In 2019 . . .  
1a) The three products with the lowest order average are all Office Supplies. 
    Labels: $30.03; Fasteners: $36.29; Envelopes: $71.65  

1b) The product with the lowest average order profit is Furniture/Tables! We Superstore loses $107.18 per order. This brings the average order profit of all furniture sales to just $32.22 despite Tables having the highest Order Average Value of all other Sub-Categories of any Category. Office Supplies had the next two lowest Average Order Profits with Fasteners at $4.67 and Labels at $5.86.  

1c) Furniture/Tables have the highest average order discount amount by far at $391.03. Next is Technology/Machines with an average discount of $119.60. Next, Furniture/Bookcases come in at a $107.21 average order discount.  

1d) The Average Order Discount when all products are considered is 14.33% 
Again, we see Furniture/Tables costing Superstore money with the highest average order discount at 29.12%. 
Office/Supplies/Binders are discounted 18.21% and 
Furniture/Chairs 16.24%. 
Of note is other products above the average are: 
Technology/machines 16.13% 
Furniture/Bookcases 15.45%
Office Supplies/Fasteners 15.10% 
Furniture/Furnishings 14.72%.  
**All four of Superstore's Furniture items are discounted above the Average Order Discount percentage.**  

2) The average order size is 7 items.  

3) Overall, and interestingly for each Category/Sub-Category product, fulfillment days have a minimum of 0, an average of 4, and a maximum of 7 days.

Suggestions:

1) Evaluate discounts for Furniture products. Compare Superstore's discounts with competitors to see if it would be lucrative to lessen the discounts or if they should remain so that we can retain our current customers and attract others.
2) Some low sales order value items need to stay in inventory. Even though they do not themselves produce high profits, they draw customers in who want a one-stop shop for all office items. Office Supplies like Fasteners, Labels (and Envelopes)

## Suggestions For Future Analysis  
1) Next take a look at our top performing products so that we can (continue to) market them effectively.
2) Continue and improve data collection. Include item cost, and price before discount.
3) Compare findings each month/quarter of the current year to impact a cycle of improvement.
4) Improve by showing Average Order Discount Percentage for more than one Category/Subcategory at a time.
5) Future dashboard to include year over year analysis of Category / Sub-Category combinations.
6) Re-evaluate before updating dashboard to determine is stakeholders desire any additional KPIs.
7) Increase date selection flexibility.

## Data  
Data was sourced from the Orders table of the [Tableau Superstore Data Set](https://docs.google.com/spreadsheets/d/1rAZkrxrtO1LQd7Lw61jXta0A7Bj5lFtn3LPRzcVxqhI/edit#gid=1824808968)
 via Luke Barosse's: [My Tableau tutorial playlist](https://www.youtube.com/playlist?list=PL_CkpxkuPiT_sRLeU_5JSArjc0P1lGU2_).
This data set contains 51290 sales order data records for Tableau Superstore office items segmented by Consumer, Corporate, and Home Office segments. Items themselves are categorized by Furniture, Office Supplies, and Technology, and are further sub-categorized.

The data is stored in long format. We consider the data to be first-party data, with a complete sales order history and therefore reliable and comprehensive. The data is for sales from 1/1/2016 through 12/13/2019. For the purposes of this study, we will go back in time to 2020 and assume that this data is timely and adequate for data-driven analysis for the current year.

**Metadata**  
This sample file has food sales data, from an imaginary food company.

There are 23 original columns of data
There are 51290 rows of data in the sales table. Multiple rows can be observed for a single order, dependent on different items purchased in the same transaction.

Each row shows the following fields and my observations/assumptions(?) about each field:

Row ID: consecutive row number  
Order ID: sales order number  
Order Date: Date the order was placed  
Ship Date: Date item was shipped  
Ship Mode: First Class, Second Class, Standard Class, Same Day  
Customer ID: Id assigned to unique customers  
Customer Name: Name of customer associated with 'Customer ID'  
Segment: Type of purchase: Consumer, Corporate, Home Office  
City: (Shipping?) City of Customer  
State: (Shipping?) State of Customer  
Country: (Shipping?) Country of Customer  
Postal Code: (Shipping?) Postal Code of Customer (not required)  
Market: (Sales Market?) Africa, APAC, Canada, EMEA, EU, LATAM, US  
Region: (Geographic region where order will be shipped?)  Africa, Canada, Caribbean, Central, 
  Central Asia, East, EMEA, North, North Asia, Oceania, South, Southeast Asia, West  
Product ID: Unique to each item  
Category: Furniture, Office Supplies, Technology  
Sub-Category: Items that belong to the different Categories  
Product Name: Name associated with 'Product ID'  
Sales: Total price of the quantity of this Product ID for this Order ID after discount has been applied  
Quantity: number of units ordered of the Product ID for this Order ID  
Discount: Percentage deduction discounted from original Sales price and already reflected in the Sales column  
Shipping Cost: Cost to ship item to customer  
Order Priority: Critical, High, Medium Low  

## Data Prep
Working with previously cleaned and formatted data. 

## Overview of Calculations performed for visualizations
1) Avg order value =  Sum(sales)/countd(order id)
2) Avg basket size = qty/orders = Sum(quantity)/countd(order id)
3) Fulfillment days
    Min(Ship Date - Order Date)
    Avg(Ship Date - Order Date)
    Max(Ship Date - Order Date)
4) Avg order discount (%) = Avg(discount) = AVG(disc_amt/orig_price)
5) Avg profit/order = Avg(order profit) = sum(profit)/countd(order id)
6) Avg discount/order ($) = Avg(order disc_amt) = sum(disc_amt)/countd(order id)

* Disc_amt = Discount * Sales/(1-Discount) or computed Orig_Price - Sales
* Filter by Date, Category, and Sub-Category where appropriate.

## SQL Checks  
Queries against the dashboard reports can be reviewed at [SQLChecks.txt](/SQLChecks.txt)

# Sales Dashboard
## Visualizations
**Note: Date ranges are selected in full months**
### **Average Order Value Bar Chart**   
For orders with selected products, shows average sales value for those products in the selected time period.

### **Average Order Profit Highlight Table**   
Shows average sales profit for products in the selected time period.

### **Average Order Discount Amount Highlight Table**   
Shows average order discount in dollars for products in the selected time period. 

### Additional KPIs
### **Average Basket Size**   
Shows average items per order in the selected time period.

### **Fulfillment Days (min, max, avg)**   
Shows minimum, maximum, and average fulfillment days for selected products in the seleted time period.

### **Average Order Discount (%)**   
Shows average order discount percent selected products in the seleted time period. 

## Resources
[Luke Barosse's: My Tableau tutorial playlist](https://www.youtube.com/playlist?list=PL_CkpxkuPiT_sRLeU_5JSArjc0P1lGU2_)  (options/formatting)  
[Tableau Superstore Data Set](https://docs.google.com/spreadsheets/d/1rAZkrxrtO1LQd7Lw61jXta0A7Bj5lFtn3LPRzcVxqhI/edit#gid=1824808968)  (data)  
[How to Create a Single Column Hierarchy Drill Down Drill Up with Parameter Actions](https://www.youtube.com/watch?v=L140GRsQ-mY&list=PLdeA_5rmA1Ecl1MnWUsyuV3IjiPSOqbU7&index=12) (for category/sub-category drill down)  
[Method 1: Insert a Hyperlink onto your Tableau Dashboard using textual/sheet with Actions](https://www.youtube.com/watch?v=-Mtb3WPBPSM) (for links)  
[Tableau KPI dashboard Design for Business Dashboards](https://www.youtube.com/watch?v=WT-8TLEXpF4&list=PLdeA_5rmA1Ecl1MnWUsyuV3IjiPSOqbU7&index=13&t=469s) (formatting)    
[How To Create a Filter for Start and End Dates Using Parameters in Tableau](https://www.youtube.com/watch?v=hMsQ8TvVjo4) (date filters - applied to all sheets)  
[Coursera](https://www.coursera.org/)  
[Google Data Analytics Certificate Course](https://www.coursera.org/professional-certificates/google-data-analytics?utm_source=gg&utm_medium=sem&utm_campaign=15-GoogleDataAnalytics-US&utm_content=B2C&campaignid=12504215975&adgroupid=122709142687&device=c&keyword=coursera%20data%20analytics%20course&matchtype=b&network=g&devicemodel=&adpostion=&creativeid=504570191916&hide_mobile_promo&gclid=Cj0KCQjw94WZBhDtARIsAKxWG--aGc_mpu7WTeU8sHtAVT4D9k79qOSJOCdgcl3hVUqPH2zR1B2j8acaAovsEALw_wcB)  