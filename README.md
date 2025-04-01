# Sales Data

https://1drv.ms/x/c/88e6a26ec908b351/EWMU6H5GjTRPubjpIyl6QrEBg_NpK4KwywVDT6cVMl-XUA?e=7kCclh

Overview

This project involves cleaning and visualizing sales data in Excel. The final dashboard provides insights into sales, profit, and product details, aiming to improve decision-making processes.

Data Cleaning:

1. Order Date Formatting:

  The 'Order Date' was originally stored as text.

  Used "Text-to-Columns" to split the date, month, and year into separate columns.

  Recombined them using the DATE() function to create a properly formatted date column.

2. Price Formatting:

Prices were adjusted to display in currency format using the format tab.

3. Extracting Product Color:

Extracted product color from the 'Product Name' column using the formula: 
         
          =TEXTAFTER(L2, " ", -1).

New column:

Profit Calculation:

Added a new column for profit calculated as:
             
             Sales - Cost of Sales.


Improving Readability:

1. Created separate sheets to hold product category and sub-category details.

2. Removed duplicate values and hidden unnecessary columns from the clean sheet.

3. City-Country and Country-Region Relationship:
   Applied similar cleaning methods to the city-country and country-region relationships.

4. Segment Column update
   Added a new "Segment" column based on product sub-categories.

5. Regional Managers' Data Update:
   Region - Regional Manager
   Integrated regional managers' table data using the INDEX MATCH function. This allowed updating regional manager information in the main table based on the country.

       =INDEX('country-continent'!$E$1:$F$4,MATCH(Excel_project1!Q2,'country-continent'!$E$1:$E$4,0),2)
   
7. Product Segment Update:
   Added product segments (such as consumer, office) using VLOOKUP.This updated the segment information based on the product table.

       =VLOOKUP(Excel_project1!$O2,product!$A$2:$F$23,6,FALSE)
   
9. Product Totals,Profit, Quantity Calculation:
    Calculated product totals (sum of sales) using SUMIFS. Similarly, product profit and quantity were calculated for each product using corresponding criteria.

       =SUMIFS(Excel_project1!H:H,Excel_project1!O:O,product!$A2,Excel_project1!P:P,product!$B2)

Excel Dashboard
The dashboard presents the following:

Key Performance Indicators (KPIs) such as total sales, total profit, total Quantity

Slicers : Order Date, Channel, Region and Segment

Visualizations like bar charts, column chart, pie charts, area chart are created from pivot tables ( pivot charts).


