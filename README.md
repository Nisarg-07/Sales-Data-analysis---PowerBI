# Sales Analysis - PowerBI : Overview
> Created by Nisarg Patel

* Developed a PowerBI Dashboard to assist **ElectroHub** in analyzing its Sales Data.
* Employed four tables (Customer Details, Product Details, Promotion Details, and Transaction Details) for the analysis.
* Identified the top and bottom five products based on sales and profit, sales by city, sales trend over time, the relationship between sales and profit, and the average discount for each discount category.
--
## Tool and System 
* **PowerBI :** Power Query Editor, DAX, Visualization
* **System :** MacOS(15.1.1) - Parallels


## Dataset 
The sales data was colleted from ElectroHub in form of 4 Xlsx Files.
* **Customers :** The table contains the information on customers
  * CustomerID
  * CustomerName
  * City
  * State
  * Pincode
  * EmailID
  * ContactNumber
  
* **Product :** Table Contains product Detail
  * ProductID
  * ProductName
  * ProductLine
  * PricePerUnit

* **Promotion :** The table contains Promotion Details
  * PromotionID
  * PromotionType
  * AdType
  * CouponCode
  * PriceReductionType

* **Fact Table :** This Table had all the transaction details
  * Date
  * CustomerID
  * PromotionID
  * ProductID
  * UnitsSold
  * PricePerUnit
  * Total Sales
  * DiscountPercentage
  * Discount Value
  * NetSale
  * Profit
 
## Data Transformation 
- I have utlized **Power Query Editor** for Data Tranformation

  ### Customers Table
  - The Table didn't had any missing entry
  - I have changed the data Types of the column according to business needs

  ### Product Table
  - No missing Value in the Table
  - Changed the Data types of the columnm accoring to busineess needs

  ### Promotion Table
  - No missing Value
  - Extracted whole number form Price reduction (Eg : 20% off, 10%off ..) column and created a numeric column percentage using custom column feature.

  ### Fact Table
    #### Price Per Unit
    - Null Column
    - Extracted Price per unit from **Product Table** using **Join** on **ProductID** Column
      
    #### Total Sales
    - Null Column
    - Filled the column using **price per unit** and **unitSold** Column

    #### Discount Percentage
    - Extracted discount percentage from **Promotion Table** using **Join** on **Promotion ID** column

    #### Discount Value
    - Calculated  and filled the Discount value from **Discount percentage** and **total sales** column using **Custom Column** Feature

    #### Net Sales
    - Calculated net sales using **discount value** and **total sales** column

    #### Profit
    -  Client was getting 10% of profit on totalSales 

  

  
