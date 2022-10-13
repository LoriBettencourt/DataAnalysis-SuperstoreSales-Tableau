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
1) Avg order value = Sum(sales)/countd(order id)
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