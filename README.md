# 📊 Sales Data Visualization

This Power BI report analyzes sales performance from 2020 to 2024, showcasing top and bottom products by sales, profit, and units sold. It includes sales trends, promotion effectiveness, geographic sales distribution, and interactive tabular data for thorough analysis.

**Data Transformation Process:**  
The raw data underwent comprehensive cleaning and restructuring in Power Query, including column reordering, type conversions, merging of related tables, and removal of unnecessary fields. Key steps involved promoting headers, filtering rows, replacing values, and adding custom columns to ensure data consistency.

---

## 📌 Page Overviews

### 🏆 Page 1: Product Performance Analysis
![image](https://github.com/user-attachments/assets/f9c70dcd-8601-43ea-bf9f-05a5a934d28b)

Presents a comprehensive overview of product performance by ranking the top and bottom 5 products across three key metrics:
- Total sales
- Units sold
- Profit

Helps identify best-selling and underperforming products for inventory, marketing, and sales strategy optimization.

---

### 📈 Page 2: Sales & Profit Trends
![image](https://github.com/user-attachments/assets/12d0f348-0d83-4303-a119-4e88c3d16acb)

Visualizes:
- Year-wise performance (2020-2024)
- Profit vs. Net Sales comparison
- Average discount values by promotion type

Assesses impact of different promotional strategies.

---

### ⚖️ Page 3: Comparative KPI Analysis (DAX Measures)
![image](https://github.com/user-attachments/assets/a3dbd0fa-160a-4367-a0c2-06a89e8f768b)

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
![image](https://github.com/user-attachments/assets/91092f13-3bd4-4a39-aeb0-ffd2b73bbb4b)


# 🔄 Page 4: Comparative KPI Analysis (Edit Interactions)
This page displays the same sales, profit, and quantity metrics as Page 3 but adds interactive date filters using Power BI’s Edit Interactions feature. Unlike Page 3 (static DAX measures), users can dynamically adjust the date ranges (e.g., compare 2020–2024 vs. 2020–2022) to analyze performance across different time periods. The core calculations remain consistent, but the filters enable flexible, real-time comparisons.
![image](https://github.com/user-attachments/assets/f3b6420f-bf8e-4e61-8787-be0184653a4e)

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
![image](https://github.com/user-attachments/assets/cea73876-a1a5-47b9-9f31-109ff78f3573)

With filters to segment data by product, customer, or promotion.
![image](https://github.com/user-attachments/assets/7c86e251-3c70-4152-9e88-ca4d1efe4d83)
