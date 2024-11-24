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

## Sales Trend (Yearly, Quatrly, Monthly)
 - Utilizing the drill-down option within the Line chart, I was able to discern the sales trend over the specified timeframe.

   ## Sales Trend Yearly
    <img width="775" alt="Screenshot 2024-11-24 at 2 21 12 PM" src="https://github.com/user-attachments/assets/7aeb7b7d-f269-49b1-8e87-0de7f78971cc">
    
    - It is evident that sales value has been consistently increasing over time.
    - However, there was only one record for the year 2024, which resulted in a relatively low sales figure for that year.

   ## Sales Trend Quatrly
    <img width="775" alt="Screenshot 2024-11-24 at 2 23 59 PM" src="https://github.com/user-attachments/assets/15577435-e5e0-4d81-b0ad-25d5ad266bc5">

    -It is evident that across all years, the highest sales figures were recorded during the fourth quarter, which totaled **32.6 million**.

   ## Sales Trend Monthly
    <img width="775" alt="Screenshot 2024-11-24 at 2 26 04 PM" src="https://github.com/user-attachments/assets/f05e90e0-8d5b-49e5-8c0d-9f787a04b278">

   - The highest sales figures were recorded in **October and November**.

## Sales and Profit Relation 
 <img width="522" alt="Screenshot 2024-11-24 at 2 30 27 PM" src="https://github.com/user-attachments/assets/a0252569-ccdd-4a3f-a702-6c416f23299e">
 
 - A linear relationship can be observed between the sales and profit columns, as the client was earning a flat **10% profit** on each sale.

## Avrage Discount For each promotion Category 
 <img width="598" alt="Screenshot 2024-11-24 at 2 32 52 PM" src="https://github.com/user-attachments/assets/e1bc6456-c642-46cf-8ed8-2611d9d74afd">
 
 - The accompanying stacked bar chart presents the average promotion price for each promotion category. Notably, **Weekend Flash Sales** exhibit the highest average discount, averaging 22.6k INR.

## Sales By City 
    
<img width="548" alt="Screenshot 2024-11-24 at 2 38 37 PM" src="https://github.com/user-attachments/assets/98d6727c-11f7-484a-b8ee-657cd073499a">

- The enclosed map chart illustrates the sales figures for each city, with the size of the bubbles representing the sales volume. Notably, **Bhopal** recorded the highest sales, surpassing **1.5 million** units.

## Sales/Profit/quntity sold comparison for 2 periods by User
 <img width="814" alt="Screenshot 2024-11-24 at 2 42 21 PM" src="https://github.com/user-attachments/assets/e21b9d6b-6cfd-46b2-b15b-12c29a080d4f">

 - The aforementioned interactive graph would enable users to compare the sales, profit, and sold quantity across two distinct time periods.

## Filterd Transaction data 

 <img width="952" alt="Screenshot 2024-11-24 at 2 46 22 PM" src="https://github.com/user-attachments/assets/fc36591a-958a-463f-bf67-df1d8295003e">

- The interactive graph provided above would assist the client in identifying specific transaction details by filtering the data based on the criteria of Date, CustomerName, ProductName, and PromotionName.

## Promotion Filter 
<img width="475" alt="Screenshot 2024-11-24 at 2 53 59 PM" src="https://github.com/user-attachments/assets/612c67db-e96d-4813-afe1-b4b3afbcb1f3">

- This interactive graph enables clients to visualize the discounts utilized by specific customers and vice versa.

Nisarg Patel © 2024



  

  
