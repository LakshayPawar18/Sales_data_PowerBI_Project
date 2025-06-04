# 📊 Sales Data Visualization

This Power BI report analyzes sales performance from 2020 to 2024, showcasing top and bottom products by sales, profit, and units sold. It includes sales trends, promotion effectiveness, geographic sales distribution, and interactive tabular data for thorough analysis.

**Data Transformation Process:**  
The raw data underwent comprehensive cleaning and restructuring in Power Query, including column reordering, type conversions, merging of related tables, and removal of unnecessary fields. Key steps involved promoting headers, filtering rows, replacing values, and adding custom columns to ensure data consistency.

---

## 📌 Page Overviews

### 🏆 Page 1: Product Performance Analysis
![Screenshot](https://github.com/user-attachments/assets/75aec10f-cbe5-4eee-858c-0771089a7bcc)

Presents a comprehensive overview of product performance by ranking the top and bottom 5 products across three key metrics:
- Total sales
- Units sold
- Profit

Helps identify best-selling and underperforming products for inventory, marketing, and sales strategy optimization.

---

### 📈 Page 2: Sales & Profit Trends
![Screenshot](https://github.com/user-attachments/assets/c1738272-0eec-4b65-b6cf-fa2fb5cc0c6e)

Visualizes:
- Year-wise performance (2020-2024)
- Profit vs. Net Sales comparison
- Average discount values by promotion type

Assesses impact of different promotional strategies.

---

### ⚖️ Page 3: Comparative KPI Analysis (DAX Measures)
![Screenshot](https://github.com/user-attachments/assets/6ae2b9dd-b9fa-415a-bd9c-3c24b9511b50)

Features:
- Side-by-side comparison of total sales, profit, and quantities sold
- Dual bar charts with independent date filtering
- Advanced DAX measures for flexible analysis

**DAX Example:**
"""dax
Sum of Net Sales = 
CALCULATE(
    SUM('Fact Table'[Net Sales]),
    ALL('Date Table 1'), 
    USERELATIONSHIP('Date Table 2'[Date],'Fact Table'[Date (dd/mm/yyyy)])
)"""
![Screenshot 2025-06-04 234924](https://github.com/user-attachments/assets/ef8f0aec-23f4-4767-8c9c-76be4f5a03d4)


# 🔄 Page 4: Comparative KPI Analysis (Edit Interactions)
This page displays the same sales, profit, and quantity metrics as Page 3 but adds interactive date filters using Power BI’s Edit Interactions feature. Unlike Page 3 (static DAX measures), users can dynamically adjust the date ranges (e.g., compare 2020–2024 vs. 2020–2022) to analyze performance across different time periods. The core calculations remain consistent, but the filters enable flexible, real-time comparisons.
![image](https://github.com/user-attachments/assets/0c364405-714e-4bcc-b1ca-ed3dcabd7912)

Features:
- Dynamic period comparison using interactive date filters
- Same core metrics as Page 3 (sales, profit, quantities)
- Power BI's Edit Interactions enabling real-time adjustments

Enables analysis of:
- Different fiscal year comparisons
- Campaign period effectiveness
- Seasonal performance variations

# 📋 Page 5: Transaction Details
This page provides a detailed transaction log showing individual sales records, including product details, customer information, pricing, discounts, and profit metrics. The table format allows for granular analysis of each order. Key columns include Order ID, Discount Percentage, Net Sales, and Profit, enabling deep dives into specific transactions and promotional effectiveness.
![Screenshot 2025-06-04 223357](https://github.com/user-attachments/assets/1cf70e8f-9a91-4ad4-b240-1ae86927ddfe)
With filters to segment data by product, customer, or promotion.
![Screenshot 2025-06-04 223442](https://github.com/user-attachments/assets/a6ea7446-f4aa-4f9f-99a5-4a9f9a95b2ef)





