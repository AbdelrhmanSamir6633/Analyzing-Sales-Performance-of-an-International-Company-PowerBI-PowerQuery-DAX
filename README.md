# Analyzing Sales Performance of an International Company | Power BI | Power Query | DAX

## Project Description

This project will evaluate sales data to uncover insights into seasonal trends, regional variations, product performance, and customer behavior. The findings will help the company make data-driven decisions to optimize sales strategies, improve market positioning, and drive revenue growth on a global scale.

Key deliverables will include interactive dashboards, in-depth visualizations, and detailed reports that highlight opportunities for enhancing sales performance and addressing challenges in various international markets.

## Content:

1- Problem Overview

2- Project Overview

3- Database Description

4- Tools and Technologies Used

5- Data Model

6- Analysis Process/Methodology

7- Key Visualizations

8- Data Source & Project Files





## (1/8) Problem Overview

![Problem Description](https://github.com/user-attachments/assets/220707b5-eb44-48e8-82fd-250bcdc19c47)


## (2/8) Project Overview

The business problem typically addressed involves identifying areas for improving performance, such as increasing sales, optimizing inventory, enhancing customer satisfaction, or improving operational efficiency, so the project will include specific Measures and Key deliverables which will result in interactive dashboards, in-depth visualizations, and detailed report that highlight opportunities for enhancing sales performance and addressing challenges in various international markets.

## (3/8) Database Description

This database contains sales data for an international company, structured across multiple fact and dimension tables to facilitate detailed analysis of sales transactions, customer behaviors, and product performance across different regions and currencies.

Fact Table: 
  - Fact_InternetSales: Stores transactional sales data from internet-based sales.

Dimension Tables:
  - dim_Customer: Contains information about the customers.
  - dim_Products: Contains details about the products being sold.
  - dim_Currency: Contains information about the currencies used for transactions.
  - dim_salesterritory: Contains information about the different sales territories.

This structure supports a variety of analyses, such as:

- Sales performance by product, region, customer, and currency.
- Currency impact on sales by using exchange rates to convert transactions to USD.
- Geographical analysis of sales territories.

## (4/8) Tools and Technologies Used

- Power BI for creating interactive data visualizations and dashboards.
- Power Query for data transformation.
- DAX for Creating Measures, Calculated Columns, Time Intelligence Calculations, and other Advanced Calculations.

## (5/8) Data Model

The model is structured with relationships connecting the Fact table (sales) to the relevant dimension tables (Customers, Products, Currency, SalesTeritory, and Date). These relationships enable robust reporting and writing DAX formulas for data exploration.

![0_Data Model](https://github.com/user-attachments/assets/96a10af7-b4f3-4cfd-bf5b-35a21c2a7e19)


## (6/8) Analysis Process/Methodology

1) Understanding the Business Problem: 
    - Identify the business problem or goals for the analysis based on the mentioned problem description above.
2) Data Exploration and Familiarization: 
    - Understand the structure, relationships, and contents of the dataset.
3) Data Cleaning and Transformation: 
    - Prepare the data for analysis by handling missing values, standardizing formats, and creating new calculated fields using Power Query such as:
      - Converting Sales Amount from all currencies to USD to be able to visualize it as required.
      - Remove duplicates, handle null values.
      - Filter unnecessary rows, and format columns appropriately.
      - Creating dim_Date table to compare metrics vs time:
        - ![00_dim_Date_Table](https://github.com/user-attachments/assets/eb5b408d-4bf7-4762-af06-9a965a7c40f9)

      - Creating around 15 Measure for various metrics and KPIs using DAX such as:

        1) Total Sales Amount in USD:
![1_Total Sales Amount USD](https://github.com/user-attachments/assets/1a89897f-e199-4413-936c-79c20dbe090b)

        2) Total Sales Amount of ALL Countries: (to be able to calculate the percentage of Sales correctly)
![2_Total Sales Amount ALL Countries](https://github.com/user-attachments/assets/3c825dbd-57fd-406a-b3d4-b7a1224cc94e)

        3) Sales Percentage:
![3_%Sales](https://github.com/user-attachments/assets/dc614234-acc8-4619-b8e7-9876c881f09f)

        4) Sales Amount ONE month ago:
![8_Sales One Month AGO](https://github.com/user-attachments/assets/a51c099c-aac3-4449-99b4-3f3d8723fe36)

        5) Sales Amount THREE month ago:
![9_Sales Three Month AGO](https://github.com/user-attachments/assets/dc468ac7-f7e7-4c99-b874-c2bd5627a814)

        6) Sales Amount SIX month ago:
![10_Sales Six Month AGO](https://github.com/user-attachments/assets/2ae1ec45-a76a-4bbf-bb1b-3c8074949a27)

        7) Sales Amount for ONLY LAST MONTH: 
![4_Only Last Month Sales](https://github.com/user-attachments/assets/7e1dfad3-bb61-4e5f-8fff-cedd4f0d7489)

        8) % year-over-year growth:
![15_%YoY Growth](https://github.com/user-attachments/assets/8ea3500f-4bf1-438f-90ae-ea780bff2e0b)

        9) Sales Amount per selected Currency:
![5_Sales Amount Selected Currency](https://github.com/user-attachments/assets/509574a3-e136-4ccd-afb5-fe288564a91a)

        10) Total Sales Amount of ALL Currencies: (to be able to represent the selected Currency vs ALL Currencies)
![7_Total Sales Amount ALL Currencies](https://github.com/user-attachments/assets/935a0223-3e2b-4747-b6f9-237306c1eba6)

        11) Dynamic Title for the selected Currency:
![6_Title Currency Type](https://github.com/user-attachments/assets/9b471755-7882-4592-a2fc-04b6c6c22333)

        12) Dynamic Title for Bar Chart that represents the selected Currency vs ALL Currencies
![11_Title Bar Chart](https://github.com/user-attachments/assets/420c065f-8c88-4d80-9f78-9724e56fe732)

        13) Total Number of Products sold: (to represent it in a Map showing Number of products sold for each Country)
![13_Total Products Sold](https://github.com/user-attachments/assets/68cee1ed-1566-4aeb-96e5-fa7f1a684530)

        14) Dynamic Title for Map: (to show the selected Country dynamically) 
![12_Title Map](https://github.com/user-attachments/assets/5884a5d2-7dbb-4ca7-b123-6f5a1732e319)

        15) Executed: last Date and Time the report was opened
![14_Executed](https://github.com/user-attachments/assets/99277a65-c0fb-4360-a003-380c47c0af1c)


    - Parameter: for Dynamic Data Source Connections
      - "Source" parameter is used to have the ability to change the data source dynamically, such as switching between different databases, servers, or file paths.

4) Exploratory Data Analysis (EDA):
    -  Identify patterns, trends, and insights within the data.

5) Data Visualization and Reporting:
    - Present key findings through visualizations and reports for better decision-making.

## (7/8) Key Visualizations

The Sales Overview Dashboard provides a high-level summary of the key performance metrics related to sales, offering valuable insights into the overall performance of the business
showing Total Sales Amount vs Time, Currency, and Country.

- <a href="https://app.powerbi.com/groups/me/reports/1ed566a7-bf8d-4c0e-bf71-23f053f420b8/1d6ee74968bc72975bcb?experience=power-bi&bookmarkGuid=d6ed3a85c8886f5188f6">Power BI Interactive Dashboards </a>

- Global Sales Analysis - Main Dashboard:
![Global Sales Analysis - Dashboard_page-0001](https://github.com/user-attachments/assets/55a2f79f-808d-4a79-b64f-d54135e4467f)

- Dynamic Tooltip:
  
![Dynamic Tooltip_page-0002](https://github.com/user-attachments/assets/cd34fa90-0f7a-4a3d-a19f-6fe1f3bd504c)

- Main Dashboard + Dynamic Tooltip:
![Main Dashboard + Dynamic Tooltip](https://github.com/user-attachments/assets/6c420aa5-634d-4ae4-9072-c7dc0b0b4075)

- Dashboard Snapshots:
  
  1) General Overview of dashboard:
![General Overview of dashboard](https://github.com/user-attachments/assets/832b128c-5bad-4950-a4a6-969e191d20cd)

  2) Customer Selection:
![Customer Selection](https://github.com/user-attachments/assets/37e86d5b-e644-41e0-ab23-6255ba5ae346)

  3) Currency Selection:
![Currency Selection](https://github.com/user-attachments/assets/6802d148-72a2-49d4-9e31-b3bf719931b5)

  4) Country Selection:
![Country Selection](https://github.com/user-attachments/assets/34fce43d-0228-493c-92f1-71227e0e4128)

  5) Time Selection:
![Time Selection](https://github.com/user-attachments/assets/26a7168b-4f0c-493a-8293-f9eac47b7da5)



## (8/8) Data Source & Project Files

- <a href="https://github.com/AbdelrhmanSamir6633/Analyzing-Sales-Performance-of-an-International-Company/blob/main/Data%20Source.xlsx">Data Source</a>

- <a href="https://github.com/AbdelrhmanSamir6633/Analyzing-Sales-Performance-of-an-International-Company/blob/main/Dashboard.pdf">Dashboard</a>

- <a href="https://github.com/AbdelrhmanSamir6633/Analyzing-Sales-Performance-of-an-International-Company/blob/main/FINAL%20PROJECT.pbix">Power BI file</a>













