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

## Insights on Sales

### Top 5 Products by Sales
  <img width="600" alt="Screenshot 2024-11-24 at 2 04 44 PM" src="https://github.com/user-attachments/assets/927fc96e-e00d-45db-99db-1a3e366b4a93">
  
  - The aforementioned bar chart indicates that Apple products were experiencing exceptionally high sales, exceeding 19 million units.
   
### Top 5 Products By Profit 
 <img width="588" alt="Screenshot 2024-11-24 at 2 07 23 PM" src="https://github.com/user-attachments/assets/ee4aa101-0032-4f1d-a1af-98251e5a5670">
 
 - The bar chart indicates that the Apple iPhone 14 and Raymond Suit were the most profitable products, with profits of 2.41 million and 0.41 million, respectively. 

### Botton 5 Products by Sales and Profit 
 <img width="623" alt="Screenshot 2024-11-24 at 2 11 01 PM" src="https://github.com/user-attachments/assets/266fb142-b291-478c-84d1-4d5dd4cd7f7d">
 
 - The bar chart presents the five products with the lowest sales figures.
 
 <img width="623" alt="Screenshot 2024-11-24 at 2 12 08 PM" src="https://github.com/user-attachments/assets/993047e2-4f31-4b7d-abf5-d7c9b28b6021">
 
 - The bar chart persents the five products with the lowest profits
 



  

  
