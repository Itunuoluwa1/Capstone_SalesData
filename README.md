# Capstone Sales Data
## This is where I documented the Sales Performance Analysis for a Retail Store
### Project Title: Sales Performance Analysis for a Retail Store
**Summary:** In this project, you are tasked with analyzing the sales performance of a retail store. 
You will need to explore sales data to uncover key insights such as top-selling products, regional 
performance, and monthly sales trends. The goal is to produce an interactive Power BI 
dashboard that highlights these findings.

Parts In The Documentation\
[EXCEL](#excel)\
[SQL](#sql)\
[Power BI](#power-bi)


## EXCEL
- Perform an initial exploration of the sales data. Use pivot tables to summarize total sales by product, region, and month.
- Use Excel formulas to calculate metrics such as average sales per product and total revenue by region.
- Create any other interesting report.

[Remove Duplicate](#remove-duplicate)\
[Pivot Table](#pivot-table)\
[Excel Functions](#excel-functions)\
[My Personal Interesting Report](#my-personal-interesting-report)

#### Remove Duplicate
First and foremost, in my dataset I removed duplicate to impact the quality, accuracy and reliability of my data. After removing duplicates in my data, the data of 50,000 rows was reduced to 9,921 rows removing 40,079 rows, therefore, making the data more accurate.

#### Add Column
Knowing that I would be needing Revenue column and I don't have it in my table, I added a revenue column whose value was a result of the Qauntity and UnitPrice column.
```EXCEL
= F2*G2
```

#### Pivot table
I used pivot table and excel functions to uncover key insight from the sales data in the Capstone project.\
Pivot table is used for summarization of data in the project in order to uncover insights for reporting. 

1. **Total Sales By Product:**
Pivot table to summarize total sales by product with pivot chart included.\
![Capstone Total Sales By Product (2)](https://github.com/user-attachments/assets/5b221c8f-39ed-4d41-a276-4a72bd32f34b)

2. **Total Sales By Region:**
Pivot table to summarize total sales by region with pivot chart included.\
![Capstone Total Sales by Region (2)](https://github.com/user-attachments/assets/22bda19d-b5f8-4c5c-9530-988ecc489c90)

3. **Total Sales By Month:**
Pivot table to summarize total sales by month with pivot chart and slicer included. The slicer is used to filter the data in the pivot table and chart to only the selected data.\
![Capstone Total Sales By Month (2)](https://github.com/user-attachments/assets/b8e28762-7928-44ce-97ee-196c2e0f47df)\
I used yearly slicer to filter the pivot table and chart showing the total sales by month in each year.\
![Capstone 2023](https://github.com/user-attachments/assets/1bc2aa06-6910-4243-b834-bc78233475b5)
![Capstone 2024](https://github.com/user-attachments/assets/dc766e42-4406-43c8-8e27-6a2c029464f9)

#### Excel Functions
I used excel functions to make certain calculations and summarization in the dataset to attain insights from the project.
1. **Average Sales Per Product:**
I listed all the products and then used excel AVERAGEIF function to calculate the average sales per product of the sales data.
```EXCEL
=AVERAGEIF($C$2:$C$9922,J7,$H$2:$H$9922)
```
The table of the average sale per product:\
![Capstone Average Sales Per Product (2)](https://github.com/user-attachments/assets/16f1edbd-977b-4335-9f78-74f849326de1)

2. **Total Revenue By Region:**
I listed all the regions and then used excel SUMIF function to calculate the total revenue by region.
```EXCEL
=SUMIF($D$2:$D$9922,J17,$H$2:$H$9922)
```
The table of the total revenue by region:\
![Capstone Total Revenue By Region (2)](https://github.com/user-attachments/assets/ebfe8325-03e6-42db-ae81-8fd86f86fe9c)

#### My Personal Interesting Report
I made a report of Region and Product By Revenue. In this report, the table shows the total revenue of the products in each region. I made a pivot chart which was a muktiple bar chart and also a region slicer that can be used to see the total revenue by product report for specific regions selected.\
![Capstone Region and Product By Revenue (2)](https://github.com/user-attachments/assets/b50994d1-9223-4fa8-afc9-1e9ab584debc)

#### NOW THE REPORT USING THE SLICER IN SPECIFIC REGIONS
![Capstone East](https://github.com/user-attachments/assets/bc9eba55-830c-4f60-be31-5f732302e623)
![Capstone North](https://github.com/user-attachments/assets/a47b2f11-c6d4-4b4c-8abd-269b6a320103)
![Capstone South](https://github.com/user-attachments/assets/48a78229-d995-424d-9ff0-249634c2a75b)
![Capstone West](https://github.com/user-attachments/assets/5fecc155-bce7-4872-8dce-0d81454cc4f4)


## SQL
- Retrieve the total sales for each product category.
- Find the number of sales transactions in each region.
- Find the highest-selling product by total sales value.
- Calculate total revenue per product.
- Calculate monthly sales totals for the current year.
- Find the top 5 customers by total purchase amount.
- Calculate the percentage of total sales contributed by each region.
- Identify products with no sales in the last quarter.

[Data Import](#data-import)\
[Create Database](#create-database)\
[Select Statement](#select-statement)\
[Actual Tasks](#actual-tasks)

#### Data Import
The raw Capstone Data is an excel file that has two tables in two different worksheet and cannot be imported into sql ordinarily. Firstly, I opened the file in excel and removed duplicate from the data to impact quality and accuracy of my data. Then, I saved each of the worksheet as a CSV(Comma Delimited) file and was eventually having two files; one for Sales Data and the other for Customer Data. This way is would be possible to insert the data. Now I inserted the data by clicking import flat file and ensured to change the datatype where necessary and was able to insert the data successfully.

#### Create Database
A database is an organized collection of data that is stored and managed in a structured way to allow for easy access, retrieval and manipulation. I created a database for my capstone data. Also note that SQL is not case-sensitive so I didn't neccesarily use one casing.
``` SQL
create database CAPSTONE_DB
```

#### Select Statement
A select statement is a type of Data Query Language(DQL). A DQL is used to fetch the data from the database. I selected the Sales Data table in order to preview it.
```SQL
select * from [dbo].[SalesData]
```
![SQL Sales Data Table](https://github.com/user-attachments/assets/d35dc3d5-d62f-4e65-877b-3a24e627f94b)

#### Actual Tasks
I firstly altered the table and added the Revenue_Or_Sales column, updated the column to be the product of quantity and unitprice before doing the tasks. 
```SQL
alter table [dbo].[SalesData]
add Revenue_Or_Sales int 

update SalesData
set Revenue_Or_Sales = Quantity * UnitPrice
```

1. **Total sales for each product category:**
The Query:
```SQL
select SUM(Revenue_Or_Sales) as TOTAL_SALES, PRODUCT from SalesData
group by Product
```
The Table:\
![SQL Sales Data 1](https://github.com/user-attachments/assets/baeb48f8-0a2d-4df0-bcc9-f37da3583e60)

2. **Number of sales transactions in each region**\
The Query:
```SQL
select COUNT(*) as NUMBER_OF_SALES, REGION from SalesData
group by Region
```
The Table:\
![SQL Sales Data 2](https://github.com/user-attachments/assets/8e579ccc-bd8b-44a7-81e7-23eef099992e)

3. **Highest-selling product by total sales value**\
The Query:
```SQL
select top 1 SUM(Revenue_Or_Sales) as TOTAL_SALES, PRODUCT from SalesData
group by Product
order by TOTAL_SALES desc
```
The Table:\
![SQL Sales Data 3](https://github.com/user-attachments/assets/1f2a3fd7-a920-4a47-b927-372555cd3ec5)

4. **Total revenue per product**\
The Query:
```SQL
select SUM(Revenue_Or_Sales) as TotalRevenue, Product from SalesData
group by Product
```
The Table:\
![SQL Sales Data 4](https://github.com/user-attachments/assets/b8a64d8b-ef22-4593-b04c-bd5fb3a47db2)

5. **Monthly sales totals for the current year**\
The Query:
```SQL
select 
	MONTH(OrderDate) as SalesMonth,
	SUM(Revenue_Or_Sales) as MonthlySalesTotal2024 
from SalesData
where YEAR(OrderDate) = YEAR(GETDATE())
group by MONTH(OrderDate)
order by SalesMonth
```
The Table:\
![SQL Sales Data 5](https://github.com/user-attachments/assets/4b973a3c-9506-42fd-84fa-36531de7166a)

6. **Top 5 customers by total purchase amount**\
The Query:
```SQL
select top 5 SUM(Revenue_Or_Sales) as Total_Purchase_Amount, Customer_Id from SalesData
group by Customer_Id
order by Total_Purchase_Amount desc
```
The Table:\
![SQL Sales Data 6](https://github.com/user-attachments/assets/4afb6f68-b16b-4299-8b02-4b58ba14a305)

7. **Percentage of total sales contributed by each region**\
The Query:
```SQL
select Region, SUM(Revenue_Or_Sales) as Total_Sales,
	   SUM(Revenue_Or_Sales) * 100 / SUM(SUM(Revenue_Or_Sales)) OVER() AS Percentage_Of_Sales
	from SalesData
	group by Region
```
The Table:\
![SQL Sales Data 7](https://github.com/user-attachments/assets/ae626cb7-266b-489a-ba22-f601ee5ee977)

8. **Products with no sales in the last quarter**\
The Query:
```SQL
select Product, SUM(Quantity) as Product_With_No_Sale
from SalesData
where Product NOT IN (select Product from SalesData where 
					  OrderDate >= DATEADD(quarter, -1, GETDATE())
					  )
group by Product
```
The Table:\
![SQL Sales Data 8](https://github.com/user-attachments/assets/a735a07b-04c5-4d1e-8085-c70b774297ba)

## Power BI
Create a dashboard that visualizes the insights found in Excel and SQL. The 
dashboard should include a sales overview, top-performing products, and 
regional breakdowns.

Power BI is a data visualization tool that converts data from different sources to make an interactive dashboard and BI reports.

#### Data Import
I imported my capstone data into my Power BI desktop and clicked transform data. In the transform state I removed duplicates from my data to make it more accurate. \
I also added a custom column of Revenue because I know that I would be needing it in my report.
```
= [Quantity] * [UnitPrice]
```
 After doing this I loaded my data.

#### Measures
I created measures within my Sales Data.\
Total Sales Revenue
```
= SUM(SalesData[Revenue])
```
Average Order Value (AOV): Dividing total sales by number of order
```
= SUM(SalesData[Revenue]) / COUNT(SalesData[OrderID])
```





