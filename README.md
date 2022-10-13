# Data Analysis-Superstore Sales-Tableau

## Dashboard for this analysis can be found at my [Tableau Public](https://public.tableau.com/app/profile/lori.bettencourt) site.

## Scenario
The Superstore company has tracked its sales order data from 1/1/2016 through 12/13/2019. They have asked for a dashboard that when Category, Sub-Category, and Date Range values are chosen will show: 
* Average in dollars of order value, order profit, and discount amounts
* Average order discount percentage
* Minimum, Average, and Maximum fulfillment days

And also show:
* Overall average basket size 

## Business Task
We have been asked specifically to look for the following and deliver suggestions based on our findings for the past sales year: 
1. Category / Sub-Category product combinations with  
   a) lowest order value average  
   b) lowest order profit average  
   c) highest order discount amount average  
   d) highest order discount percentage average  
2. Minimum, average, and maximum fulfillment days  
3. Average order size

# Response to Business Task
Note: Superstore has a total of 17 product sub-categories.  In 2019 . . .

1.  
    a) The three products with the lowest order average are all Office Supplies.  
    Labels: $30.03  
    Fasteners: $36.29  
    Envelopes: $71.65  
    
    b) The product with the lowest order profit average is Furniture/Tables. Superstore loses an average of $107.18 per order! This brings the order profit average of all furniture sales to just $32.22 despite Tables having the highest order value average of all other sub-categories of any category.  
    The Office Supplies category had the next two lowest order profit averages with  
    Fasteners at $4.67 and  
    Labels at $5.86.  
    
    c) Furniture/Tables have the highest average order discount amount by far at $391.03.  
    Next is Technology/Machines with an average order discount of $119.60 and then  
    Furniture/Bookcases at $107.21.  
    
    d) The average order discount percentaage when all products are considered is 14.33%.

    Again, we see Furniture/Tables costing Superstore money with the highest average order discount at 29.12%.  
    Office Supplies/Binders are discounted 18.21% and    
    Furniture/Chairs 16.24%.  

    Of note are other products above the average:  
    Technology/Machines 16.13%  
    Furniture/Bookcases 15.45%  
    Office Supplies/Fasteners 15.10% and   
    Furniture/Furnishings 14.72%.           

    **Note: All four of Superstore's Furniture items are discounted above the Average Order Discount percentage.**

2. Overall, and interestingly for each Category/Sub-Category product, fulfillment days have a minimum of 0, an average of 4, and a maximum of 7 days. 

3. The average order size is 7 items.   

Suggestions:

1. Evaluate discounts for Furniture products. Compare Superstore's prices and discounts with competitors to see if it would be lucrative to decrease the discounts or if they should remain so that we can retain our current customers and attract others. Conversely, are our prices too low? Should we raise them?  
We might also consider our furniture supplier. Are we being over-charged? Should we reconsider our supplier and/or the materials or quality of the items we carry?
2. While Furniture discounts and losses are addressed, Technology/Machine discounts should be re-evaluated as well. Their average order discount is $119.60 which is about 16.13% per order. Use the same strategies as for Furniture to decide on a course of action.
3. Some low sales order value items need to stay in inventory. Even though they do not themselves produce high profits, they draw customers in who want a one-stop shop for all office items. Office Supplies like Fasteners, Labels, Binders and Envelopes are common items that office supply customers expect to be on the shelf. We can take a look at these as well, but they may not be as high of a priority. Looking at yearly sales revenue for these items might help guide us.
 

## Suggestions For Future Analysis  
1. Next, take a look at our top performing products so that we can (continue to) market them effectively.
2. Continue and improve data collection. Include item cost, and price before discount.
3. Compare findings each month/quarter of the current year to these insights to perpetuate a cycle of improvement.
4. Improve on dashboard by showing Average Order Discount Percentage for more than one Category / Subcategory at a time.
5. Future dashboard to include year over year analysis of Category / Sub-Category combinations.
6. Re-evaluate before next dashboard to determine is stakeholders desire any additional KPIs.
7. Increase date selection flexibility.

## Data  
Data source, metadata and data calculations can be reviwed at [DataAndCalculations.md](/DataAndCalculations.md)

## SQL Checks  
Queries against the dashboard reports can be reviewed at [SQLChecks.txt](/SQLChecks.txt)

## Sales Dashboard Visualizations
Explainations of visualizations can be reviewed at [Visualizations.md](/Visualizations.md)

## Resources
[Luke Barosse's: My Tableau tutorial playlist](https://www.youtube.com/playlist?list=PL_CkpxkuPiT_sRLeU_5JSArjc0P1lGU2_)  (options/formatting)  
[Tableau Superstore Data Set](https://docs.google.com/spreadsheets/d/1rAZkrxrtO1LQd7Lw61jXta0A7Bj5lFtn3LPRzcVxqhI/edit#gid=1824808968)  (data)  
[How to Create a Single Column Hierarchy Drill Down Drill Up with Parameter Actions](https://www.youtube.com/watch?v=L140GRsQ-mY&list=PLdeA_5rmA1Ecl1MnWUsyuV3IjiPSOqbU7&index=12) (for category/sub-category drill down)  
[Method 1: Insert a Hyperlink onto your Tableau Dashboard using textual/sheet with Actions](https://www.youtube.com/watch?v=-Mtb3WPBPSM) (for links)  
[Tableau KPI dashboard Design for Business Dashboards](https://www.youtube.com/watch?v=WT-8TLEXpF4&list=PLdeA_5rmA1Ecl1MnWUsyuV3IjiPSOqbU7&index=13&t=469s) (formatting)    
[How To Create a Filter for Start and End Dates Using Parameters in Tableau](https://www.youtube.com/watch?v=hMsQ8TvVjo4) (date filters - applied to all sheets)  
[Coursera](https://www.coursera.org/)  
[Google Data Analytics Certificate Course](https://www.coursera.org/professional-certificates/google-data-analytics?utm_source=gg&utm_medium=sem&utm_campaign=15-GoogleDataAnalytics-US&utm_content=B2C&campaignid=12504215975&adgroupid=122709142687&device=c&keyword=coursera%20data%20analytics%20course&matchtype=b&network=g&devicemodel=&adpostion=&creativeid=504570191916&hide_mobile_promo&gclid=Cj0KCQjw94WZBhDtARIsAKxWG--aGc_mpu7WTeU8sHtAVT4D9k79qOSJOCdgcl3hVUqPH2zR1B2j8acaAovsEALw_wcB)  