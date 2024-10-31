# Amazon Dashboard

## Table of Content 
---
  - [Project Overview](#project-overview)
  - [Data Sources](#data-sources)
  - [Tools](tools)
  - [Data Cleaning/Preparation](data-cleaning/preparation)
  - [Explorative Data Analysis](explorative-data-analysis)
  - [Data Analysis](data-analysis)
  - [Results Findings](#results-findings)
  - [Conclusion](#conclusion)
     
### Project Overview 
The objective of this project is to analyze sales data from a retail chain operating in three branches using an inetractive dashboard. This analysis seeks to uncover key insights, including customer demographics, sales perfomance across product line and overall trend in pricing terms and purchasing behaviours.

### Data Sources

### Tools
  - Power Query: Power Query was used for data extraction, transformation and loading.
  - Power BI: Power BI wa used to create calculate the KPIs and build the ineteractive dashboard.

### Data Cleaning/Preparation
  - Handle missing values
  - Standardize data types
  - Remove duplicates
  - Removing empty rows and columns
  - Trimming and cleaning each coumns

### Explorative Data Analysis
This project explored the sales data to answer the following questions:
  - Revenue contribution by Product Line
  - Monthly Revenue
  - Transactions across Payment Platforms
  - Revenue by City and Branch

### Data Analysis
Below are the DAX functions used in calculating the KPIs.
  - TOTAL QTY = SUM('Updated Amazon Sales'[Quantity])
  - NO OF TRANSACTIONS = COUNTROWS('Updated Amazon Sales')
  - REVENUE = SUMX('Updated Amazon Sales', 'Updated Amazon Sales'[Selling Price] * 'Updated Amazon Sales'[Quantity] + 'Updated Amazon Sales'[Tax 5%])
  - COGS = SUMX('Updated Amazon Sales', 'Updated Amazon Sales'[Unit price] * 'Updated Amazon Sales'[Quantity])
  - PROFIT = [REVENUE]-[COGS]
  - PROFIT MARGIN = DIVIDE([PROFIT], [REVENUE],0)
  - AVG RATING = AVERAGE('Updated Amazon Sales'[Rating])

### Results Findings

### Conclusion
