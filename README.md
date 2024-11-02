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
![Capstone Total Sales By Product (1)](https://github.com/user-attachments/assets/f6969140-c843-4304-9bc8-ce60c3776477)

2. **Total Sales By Region:**
Pivot table to summarize total sales by region with pivot chart included.\
![Capstone Total Sales By Region (1)](https://github.com/user-attachments/assets/e93dbe08-6f7c-41ef-8621-210d57ab513f)

3. **Total Sales By Month:**
Pivot table to summarize total sales by month with pivot chart and slicer included. The slicer is used to filter the data in the pivot table and chart to only the selected data.\
![Capstone Total Sales By Month (1)](https://github.com/user-attachments/assets/8751bf50-cec5-4c54-9162-7ea0ce839a0a) \
I used yearly slicer to filter the pivot table and chart showing the total sales by month in each year.\
![Capstone 2023 Slicer](https://github.com/user-attachments/assets/b5b2295b-e032-4640-8d41-7320387f6f63)
![Capstone 2024 Slicer](https://github.com/user-attachments/assets/430c5bec-38bd-4bbc-b85b-b97a22f49914)


#### Excel Functions
I used excel functions to make certain calculations and summarization in the dataset to attain insights from the project.
1. **Average Sales Per Product:**
I listed all the products and then used excel AVERAGEIF function to calculate the average sales per product of the sales data.
```
=AVERAGEIF(C2:C50001,J7,H2:H50001)
```
The table of the average sale per product:\
![Capstone Average Sales Per Product (1)](https://github.com/user-attachments/assets/b63f5693-28a2-4f27-ac14-7994ef886899)

2. **Total Revenue By Region:**
I listed all the regions and then used excel SUMIF function to calculate the total revenue by region.
```
=SUMIF(D2:D50001,J17,H2:H50001)
```
The table of the total revenue by region:\
![Capstone Total Revenue By Region (1)](https://github.com/user-attachments/assets/a68e52e1-86bd-4a08-9d76-ebcdc67a241a)

#### My Personal Interesting Report
I made a report of Region and Product By Revenue. In this report, the table shows the total revenue of the products in each region. I made a pivot chart which was a muktiple bar chart and also a region slicer that can be used to see the total revenue by product report for specific regions selected.\
![Capstone Region and Product By Revenue (1)](https://github.com/user-attachments/assets/13e7d3bf-193e-4b52-82c8-a3c1391ea280)

**Now the report using the slicer in specific regions**
![Capstone East Slicer](https://github.com/user-attachments/assets/7ccbf0af-51a2-4ad5-a24e-feff342e7919)
![Capstone North Slicer](https://github.com/user-attachments/assets/a782a64e-fedc-469a-acde-93d875ad3eed)
![Capstone South Slicer](https://github.com/user-attachments/assets/1990205e-cc5c-4507-9864-df89fd899323)
![Capstone West Slicer](https://github.com/user-attachments/assets/802a17e1-bbfa-4446-a731-ce815ecab0d1)


