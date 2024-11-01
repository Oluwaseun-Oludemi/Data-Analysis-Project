# Amazon Dashboard

## Table of Content 
---
  - [Project Overview](#project-overview)
  - [Data Sources](#data-sources)
  - [Tools](tools)
  - [Data Cleaning/Preparation](data-cleaning/preparation)
  - [Explorative Data Analysis](explorative-data-analysis)
  - [Data Analysis](data-analysis)
  - [Results & Findings](#results-&-findings)
  - [Recommendations](#recommendations)
  - [Limitations](#limitations)
  - [Conclusion](#conclusion)
     
### Project Overview 
The objective of this project is to analyze sales data from a retail chain operating three branches in three cities using an inetractive dashboard. This analysis seeks to uncover key insights, including customer demographics, sales perfomance across product line and overall trend in pricing terms and purchasing behaviours.

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
``` TOTAL QTY = SUM('Updated Amazon Sales'[Quantity])
    NO OF TRANSACTIONS = COUNTROWS('Updated Amazon Sales')
    REVENUE = SUMX('Updated Amazon Sales', 'Updated Amazon Sales'[Selling Price] * 'Updated Amazon Sales'[Quantity] + 'Updated Amazon         Sales'[Tax 5%])
    COGS = SUMX('Updated Amazon Sales', 'Updated Amazon Sales'[Unit price] * 'Updated Amazon Sales'[Quantity])
   PROFIT = [REVENUE]-[COGS]
    PROFIT MARGIN = DIVIDE([PROFIT], [REVENUE],0)
    AVG RATING = AVERAGE('Updated Amazon Sales'[Rating])```


### Result & Findings
The following insights can guide decision-making and high-light trends in customer behavior, Product Performance, and Branch Efficiency
1. Branch Performance Revenue Distribution: The Branch analysis reveals that Branch C in Yangon generates the highest revenue overall, followed by Branch B in NAYPYITAW and MANDALAY. This could indicate a larger and more loyal customer based in YANGON or a higher demand in a specifc product lines. Transaction Volume:
Branch C also has the highest transaction volume, suggesting a strong customer flow and consistent sales activity.
2. Correlation Analysis Price and Quantity Correlation: There is a slight negative correlation between unit price and quanity, suggesting that lower-priced products tend to be bought in larger quantities. Selling Price and Tax: As expected, there is a strong positive correlation between selling price and tax amount, validating that tax is accurately calculated at 5% of the subtotal.
3. Strategic Implications Branch Implications: Given the high performance of Branch C in YANGON, It may be beneficial to explore expanding product lines or increasing stock levels in this branch.
  - Product Line Focus: Promoting top-selling product lines like Health and Beauty and Electronic Accessories could maximize revenue.
  - Targeted Marketing: Since members and female customers show higher spending,targeted campaigns, especially around weekends and peak months, and may yield better results.

### Recommendations
Based on the findings from the analysis, here are several recommendations that can help improve sales, optimize branch operations, and enhance customer satisfaction.
1. Focus on High-Performing Branches 
2. Enhance Loyalty Program For Members 
3. Product Line Strategy
4. Leverage Seasonal Sales Patters
5.  Gender-Specific Marketing vi. Improve Sales Tax Efficiency

### Limitations
Here are some limitations of the analysis, which could impact the insights and recommendations drawn from the data:
1. Data Coverage and Sample Size
2. Lack of Granular Customer Data
3. Seasonal and Economic Influences Not Accounted For
4. Potential Data Entry Errors and Outliers
5. Limitation in Product Line
6. Transactional Data Only(No Longitudinal Customer Analysis)
7. Assumption of Uniform Tax Rate

### Conclusion
While the analysis provides valuable insights, the limiations highlight the need for caution in interpretations.
Collecting additional data (such as product costs, inventory levels, and more detailed customer demographic) and expanding the timeframe can enhance accuracy and lead to a more comprehensive understanding of business performance.

