# Capstone Sales Data
## This is where I documented the Sales Performance Analysis for a Retail Store
### Project Title: Sales Performance Analysis for a Retail Store
**Summary:** In this project, you are tasked with analyzing the sales performance of a retail store. 
You will need to explore sales data to uncover key insights such as top-selling products, regional 
performance, and monthly sales trends. The goal is to produce an interactive Power BI 
dashboard that highlights these findings.

## EXCEL
- Perform an initial exploration of the sales data. Use pivot tables to summarize total sales by product, region, and month.
- Use Excel formulas to calculate metrics such as average sales per product and total revenue by region.
- Create any other interesting report.

#### Pivot table
Firstly, I used pivot table and excel functions ton uncover key insight from the sales data in the Capstone project.\
Pivot table is used for summarization of data in the project in order to uncover insights for reporting. 

1. **Total Sales By Product:**
Pivot table to summarize total sales by product with pivot chart included.\
![Capstone Total Sales By Product](https://github.com/user-attachments/assets/182341f4-f927-4895-b377-db8e507efe9f)

2. **Total Sales By Region:**
Pivot table to summarize total sales by region with pivot chart included.\
![Capstone Total Sales By Region](https://github.com/user-attachments/assets/bcf74f0a-2e92-4cea-b80c-7e73702f3a93)

3. **Total Sales By Month:**
Pivot table to summarize total sales by month with pivot chart and slicer included. The slicer is used to filter the data in the pivot table and chart to only the selected data.\
![Capstone Total Sale By Month](https://github.com/user-attachments/assets/2e6250fc-a6ea-49d1-b563-e275f83fe13d) \
I used yearly slicer to filter the pivot table and chart showing the total sales by month in each year.\
![Capstone Total Sales By Month Year 2023 Slicer](https://github.com/user-attachments/assets/f06bf469-18b9-4cf5-8c4c-c8d236c993b4)
![Capstone Total Sales By Month Year 2024 Slicer](https://github.com/user-attachments/assets/6d25aefb-97ce-4c1b-852e-58a588b86c60)

#### Excel Functions
I used excel functions to make certain calculations and summarization in the dataset to attain insights from the project.
1. **Average Sales Per Product:**
I listed all the products and then used excel AVERAGEIF function to calculate the average sales per product of the sales data.
```
=AVERAGEIF(C2:C50001,J7,H2:H50001)
```
The table of the average sale per product:\
![Capstone Average Sales Per Product](https://github.com/user-attachments/assets/24944856-7125-4974-b295-a5f2f7520a0d)

2. **Total Revenue By Region:**
I listed all the regions and then used excel SUMIF function to calculate the total revenue by region.
```
=SUMIF(D2:D50001,J17,H2:H50001)
```
The table of the total revenue by region:\
![Capstone Total Revenue By Region](https://github.com/user-attachments/assets/35ce6e43-4c82-4766-a8ba-bd2568d47002)

#### My Personal Interesting Report
I made a report of Region and Product By Revenue. In this report, the table shows the total revenue of the products in each region. I made a pivot chart which was a muktiple bar chart and also a region slicer that can be used to see the total revenue by product report for specific regions selected.\
![Capstone Region and Product By Revenue](https://github.com/user-attachments/assets/b28e52d3-dd92-4428-9a25-1d35cddfd64a)

**Now the report using the slicer in specific regions**


