# Capstone Sales Data
## This is where I documented the Sales Performance Analysis for a Retail Store
### Project Title: Sales Performance Analysis for a Retail Store
**Summary:** In this project, you are tasked with analyzing the sales performance of a retail store. 
You will need to explore sales data to uncover key insights such as top-selling products, regional 
performance, and monthly sales trends. The goal is to produce an interactive Power BI 
dashboard that highlights these findings.

Parts In The Documentation\
[EXCEL](#excel)\
[PIVOT TABLE](#pivot-table)


## EXCEL
- Perform an initial exploration of the sales data. Use pivot tables to summarize total sales by product, region, and month.
- Use Excel formulas to calculate metrics such as average sales per product and total revenue by region.
- Create any other interesting report.

#### Remove Duplicate
First and foremost, in my dataset I removed duplicate to impact the quality, accuracy nad reliability of my data. After removing duplicates in my data, the data of 50,000 rows was reduced to 9,921 rows removing 40,079 rows, therefore, making the data more accurate.

#### Pivot table
I used pivot table and excel functions ton uncover key insight from the sales data in the Capstone project.\
Pivot table is used for summarization of data in the project in order to uncover insights for reporting. 

1. **Total Sales By Product:**
Pivot table to summarize total sales by product with pivot chart included.\
![Capstone Total Sales By Product (2)](https://github.com/user-attachments/assets/5b221c8f-39ed-4d41-a276-4a72bd32f34b)

2. **Total Sales By Region:**
Pivot table to summarize total sales by region with pivot chart included.\
![Capstone Total Sales by Region (2)](https://github.com/user-attachments/assets/22bda19d-b5f8-4c5c-9530-988ecc489c90)

3. **Total Sales By Month:**
Pivot table to summarize total sales by month with pivot chart and slicer included. The slicer is used to filter the data in the pivot table and chart to only the selected data.\
![Capstone Total Sales By Month (2)](https://github.com/user-attachments/assets/b8e28762-7928-44ce-97ee-196c2e0f47df)
I used yearly slicer to filter the pivot table and chart showing the total sales by month in each year.\
![Capstone 2023](https://github.com/user-attachments/assets/1bc2aa06-6910-4243-b834-bc78233475b5)
![Capstone 2024](https://github.com/user-attachments/assets/dc766e42-4406-43c8-8e27-6a2c029464f9)

#### Excel Functions
I used excel functions to make certain calculations and summarization in the dataset to attain insights from the project.
1. **Average Sales Per Product:**
I listed all the products and then used excel AVERAGEIF function to calculate the average sales per product of the sales data.
```
=AVERAGEIF($C$2:$C$9922,J7,$H$2:$H$9922)
```
The table of the average sale per product:\
![Capstone Average Sales Per Product (2)](https://github.com/user-attachments/assets/16f1edbd-977b-4335-9f78-74f849326de1)

2. **Total Revenue By Region:**
I listed all the regions and then used excel SUMIF function to calculate the total revenue by region.
```
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

