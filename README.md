# In-Depth-Analysis-of-Adidas-Sales-Operating-Profit-2020-2021

In this analysis, the aim is to evaluate the operating profit trends of Adidas product, retailers and sales method across different regions for the years 2020 and 2021. I set out to uncover which regions thrived and which faced challenges during this time.

Comprehending these patterns is more than just analyzing data; it is crucial for making knowledgeable business choices. This understanding will enable Adidas, a manufacturing company, to distribute resources more efficiently, improve product choices, and customize marketing tactics to suit the distinct requirements of each area. Ultimately, this analysis serves as a foundation for driving growth and improving overall financial performance, helping the company as a whole navigate the ever-changing landscape of the retail market.


## Tools Used
- **Python**: The primary programming language used for analysis.
- **Pandas**: For data manipulation and analysis.
- **NumPy**: For numerical computations.
- **Matplotlib**: For data visualization.
- **Seaborn**: For creating informative and attractive statistical graphics.

```
adidas_sales_data.info()
```

### DataFrame Overview
- **Class**: The object is a DataFrame, which is a two-dimensional, size-mutable, potentially heterogeneous tabular data structure in pandas, akin to a SQL table or a spreadsheet.
- **RangeIndex**: The DataFrame has a range index, meaning it uses sequential integer values (from **0** to **9647**) to label the rows.

### Column Breakdown
The DataFrame has a total of **13 columns**, each serving a specific purpose related to sales data. Here’s a brief explanation of each column:

1. **Retailer**: The name of the retailer selling the product. This is an object type (string).
  
2. **Retailer ID**: A unique identifier for each retailer, represented as an integer.
  
3. **Invoice Date**: The date of the transaction, recorded as an object type (string). Ideally, it should be converted to a date type for analysis.
  
4. **Region**: The geographical area where the sale occurred, categorized as an object type (string).
  
5. **State**: The state within the region where the sale occurred, also an object type (string).
  
6. **City**: The city within the state where the sale occurred, an object type (string).
  
7. **Product**: The type of product sold, classified as an object type (string).
  
8. **Price per Unit**: The price of each unit of the product sold, represented as an integer.
  
9. **Units Sold**: The number of units sold for each transaction, represented as an integer.
  
10. **Total Sales**: The total revenue generated from the sale (calculated as Price per Unit multiplied by Units Sold), represented as an integer.
  
11. **Operating Profit**: The profit made from the sale after deducting operating expenses, represented as a float. This is a key metric for evaluating profitability.
  
12. **Operating Margin**: The percentage of revenue that has turned into profit, also represented as a float. This is a measure of the efficiency of the company in managing its expenses relative to revenue.
  
13. **Sales Method**: The method through which the sale was made (e.g., In-store, Online, Outlet), represented as an object type (string).

### Summary Statistics
- **Non-Null Count**: Each column shows **9648 non-null**, indicating that there are no missing values in the dataset for any of the columns.
- **Data Types**: The DataFrame consists of:
  - **float64**: 2 columns (Operating Profit, Operating Margin)
  - **int64**: 4 columns (Retailer ID, Price per Unit, Units Sold, Total Sales)
  - **object**: 7 columns (Retailer, Invoice Date, Region, State, City, Product, Sales Method)

### Memory Usage
The DataFrame uses approximately **980 KB** of memory, which provides an indication of the data's size and complexity.

### Significance
This overview is crucial for familiarizing oneself with the different features characteristic of the dataset and verifying compatibility of data types that are going to be used in further analyses. For example, the comparison of the indicator of operating profit and the operating margin will be useful for comparing the financial results of Adidas in different regions and among various retailers.


### Summary of Operating Profit Analysis
Total Operating Profit for 2020: $63,375,662.58
Total Operating Profit for 2021: $268,759,098.87
Percentage Change from 2020 to 2021: 324.07%

| Year | Sales Method | In-store         | Online          | Outlet          |
|------|--------------|------------------|------------------|------------------|
|      |              | **2020**         | **2020**         | **2020**         |
|      | **Midwest**  | 652,862.50       | 89,154.76        | 1,928,212.50     |
|      | **Northeast**| 1,323,375.00     | 465,822.87       | 12,433,596.44    |
|      | **South**    | NaN              | 316,456.25       | 9,528,684.81     |
|      | **Southeast**| 11,765,812.50    | 402,806.61       | NaN              |
|      | **West**     | 17,853,500.00    | 842,245.75       | 5,773,132.59     |
|      |              | **2021**         | **2021**         | **2021**         |
|      | **Midwest**  | 22,512,787.50    | 15,455,379.22    | 12,172,950.00    |
|      | **Northeast**| 41,220,825.00    | 1,781,008.78     | 10,795,959.56    |
|      | **South**    | 1,348,000.00     | 23,677,486.97    | 26,267,376.04    |
|      | **Southeast**| 13,816,750.00    | 32,290,708.77    | 2,279,338.82     |
|      | **West**     | 17,097,375.00    | 21,234,106.49    | 26,809,046.72    |





This table presents the total sales figures for Adidas across different regions and sales methods (In-store, Online, Outlet) for the years 2020 and 2021. Each cell contains the operating profit associated with that specific combination of year, region, and sales method.

- **Columns**: The first three columns represent the years (2020 and 2021), while the last three represent the different sales methods.
- **Rows**: Each row corresponds to a specific region (Midwest, Northeast, South, Southeast, West), allowing for easy comparison of sales performance across regions and years.

### Insights:
1. **Growth Trends**: Notably, the sales figures for 2021 show significant growth compared to 2020 in most regions and sales methods, indicating an overall improvement in sales performance for Adidas.
2. **Sales Method Comparison**: The data allows for analyzing which sales methods are most effective in different regions. For instance, In-store sales in the Midwest and Northeast regions were substantial in both years, while the Online sales surged in the South in 2021, indicating a shift in consumer purchasing behavior.
3. **Data Gaps**: There are NaN (Not a Number) values in the data, particularly in the South for the In-store sales in 2020 and for the Outlet sales in the Southeast region. This might indicate either no sales occurred through these methods or missing data that requires further investigation.

Overall, this table serves as a critical resource for assessing the performance of Adidas across different sales channels and regions, helping inform strategic decisions for future sales and marketing efforts.


#### 1. Operating Profit Performance
The operating profit data across different retailers and regions in 2020 and 2021 reveals important trends that highlight the financial health and operational effectiveness of Adidas in various markets. Key observations include:

- **Midwest Region**: Foot Locker demonstrated a remarkable increase in operating profit from **$652,862.50** in 2020 to **$22,512,787.50** in 2021. This significant growth indicates that Foot Locker's sales strategies and operational efficiencies have resonated well with customers in this region, leading to higher profitability.

- **Northeast Region**: In the Northeast, the operating profit for Foot Locker rose from **$1,323,375.00** to **$41,220,825.00**, showcasing an impressive performance. Walmart and Amazon also showed substantial profitability, indicating effective market penetration and consumer engagement.

- **South Region**: The South displays variability in operating profit, especially for Sports Direct, which recorded a notable profit of **$1,864,598.87** in 2021. This indicates that despite the challenges, some retailers have managed to maintain healthy profit margins, reflecting strategic product placement and marketing efforts.

- **Southeast Region**: The Southeast region shows a dynamic profit landscape, particularly with Foot Locker's operating profit rising from **$11,765,812.50** in 2020 to **$13,816,750.00** in 2021. The presence of significant profits from both online and outlet sales illustrates a robust operational strategy that capitalizes on diverse sales channels.

- **West Region**: In the West, the operating profit figures for West Gear illustrate its dominance, with **$23,947,247.05** in 2021. This indicates that West Gear has effectively tapped into regional demand, likely through strategic inventory management and marketing initiatives.

#### 2. Retailer Comparison Based on Operating Profit
The analysis of operating profit among different retailers reveals competitive strengths and areas for improvement:

- **Amazon**: With strong operating profit figures across regions, Amazon's model shows resilience in the face of market fluctuations. The transition to e-commerce has paid off, leading to increased operational profitability.

- **Walmart**: Walmart's operating profits suggest that its traditional retail model, combined with a growing online presence, remains competitive. The profits indicate effective cost management and a strong supply chain, which are essential for maintaining profitability.

- **Foot Locker**: The substantial growth in Foot Locker's operating profit suggests that the retailer has effectively capitalized on marketing campaigns or exclusive product launches. This performance indicates that Adidas's partnership with Foot Locker is yielding significant financial benefits.

- **Kohl’s**: The lack of reported operating profit in certain regions indicates potential challenges that may be affecting Kohl's ability to compete. Understanding the causes behind these gaps could guide strategic adjustments to enhance profitability.

#### 3. Data Gaps and Their Implications
The presence of NaN values in the operating profit data indicates potential issues:

- **Missing Data Points**: These gaps might signify that certain retailers did not report sales data or had no operational presence for Adidas products in specific regions. For instance, the absence of data for Kohl’s in certain areas raises questions about its sales strategy.

- **Impact on Profit Analysis**: Addressing these missing values is crucial for a comprehensive understanding of operating profit trends. Gaps can obscure the full financial picture, making it difficult to gauge overall profitability accurately. Efforts should be made to gather complete data to facilitate a clearer analysis of performance across all channels.

### Conclusion
The analysis of operating profit across different retailers and regions provides critical insights into Adidas's financial performance. Understanding these dynamics allows Adidas to refine its operational strategies, enhance retailer partnerships, and adapt its marketing efforts to better align with consumer preferences. By continuously monitoring these metrics, Adidas can identify opportunities for growth and areas needing strategic intervention, ensuring sustained profitability in an evolving market landscape.

