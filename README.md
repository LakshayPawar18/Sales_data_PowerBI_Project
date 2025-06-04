# Sales_data_Visualisation
This Power BI report analyzes sales performance from 2020 to 2024, showcasing top and bottom products by sales, profit, and units sold. It includes sales trends, promotion effectiveness, geographic sales distribution, interactive tabular data to understand the analysation thoroughly.
The raw data underwent comprehensive cleaning and restructuring in Power Query, including column reordering, type conversions, merging of related tables, and removal of unnecessary fields. Key steps involved promoting headers, filtering rows, replacing values, and adding custom columns to ensure data consistency. These transformations standardized the dataset structure while preserving all critical business dimensions needed for analysis.

# Page 1: Product Performance Analysis
This page presents a comprehensive overview of product performance by ranking the top and bottom 5 products across three key metrics: total sales, units sold, and profit. It helps identify best-selling and underperforming products, offering insights for inventory, marketing, and sales strategy optimization.
![Screenshot 2025-06-04 223050](https://github.com/user-attachments/assets/75aec10f-cbe5-4eee-858c-0771089a7bcc)


# Page 2: Sales & Profit Trends
This page visualizes overall sales trends over time, showing year-wise performance from 2020 to 2024. It includes a Profit vs. Net Sales comparison to highlight profitability patterns and an analysis of average discount values by promotion type, helping assess the impact of different promotional strategies.
![Screenshot 2025-06-04 223128](https://github.com/user-attachments/assets/c1738272-0eec-4b65-b6cf-fa2fb5cc0c6e)

# Page 3: Comparative KPI Analysis by DAX measures
This page provides a side-by-side comparison of total sales, profit, and quantities sold using dual bar charts. Each bar in the charts responds to a separate date filter, allowing dynamic period comparisons.
![Screenshot 2025-06-04 223146](https://github.com/user-attachments/assets/6ae2b9dd-b9fa-415a-bd9c-3c24b9511b50)
Behind the scenes, DAX measures are used to enable independent filtering on the same visual—enhancing analytical flexibility.
DAX Example- Sum of Net Sales = CALCULATE(SUM('Fact Table'[Net Sales  ]),all ('Date Table 1'), USERELATIONSHIP('Date Table 2'[Date],'Fact Table'[Date (dd/mm/yyyy)]))
![image](https://github.com/user-attachments/assets/2d7dadd3-b518-4983-904f-34f5c69428f4)

# Page 4: Comparitive KPI Analysis by Edit Interactions
This page displays the same sales, profit, and quantity metrics as Page 3 but adds interactive date filters using Power BI’s Edit Interactions feature. Unlike Page 3 (static DAX measures), users can dynamically adjust the date ranges (e.g., compare 2020–2024 vs. 2020–2022) to analyze performance across different time periods. The core calculations remain consistent, but the filters enable flexible, real-time comparisons.
![image](https://github.com/user-attachments/assets/0c364405-714e-4bcc-b1ca-ed3dcabd7912)

# Page 5: Table Visual
This page provides a detailed transaction log showing individual sales records, including product details, customer information, pricing, discounts, and profit metrics. The table format allows for granular analysis of each order. Key columns include Order ID, Discount Percentage, Net Sales, and Profit, enabling deep dives into specific transactions and promotional effectiveness.
![Screenshot 2025-06-04 223357](https://github.com/user-attachments/assets/1cf70e8f-9a91-4ad4-b240-1ae86927ddfe)
With filters to segment data by product, customer, or promotion.
![Screenshot 2025-06-04 223442](https://github.com/user-attachments/assets/a6ea7446-f4aa-4f9f-99a5-4a9f9a95b2ef)





