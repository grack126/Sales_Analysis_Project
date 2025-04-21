# SQL Project - Sales Analysis

## Overview
Analysis of customer behavior, retention, and lifetime value for an e-commerce company to improve customer retention and maximize revenue.

## Business Questions
1. **Customer Segmentation:** Who are our most valuable customers?
2. **Cohort Analysis:** How do different customer groups generate revenue?
3. **Retention Analysis:** Which customers haven't purchased recently?

## Data Cleaning

**🖥️ Query**: [2_cohort_analysis.sql](2_cohort_analysis.sql)

- Aggregated sales and customer data into revenue metrics
- Calculated first purchase dates for cohort analysis
- Created view combining transactions and customer details

## Analysis

### 1. Customer Grouping by Value

**🖥️ Query Used**: [customer_segmentation.sql](customer_segmentation.sql)

- Grouped customers by total lifetime value (LTV)  
- Labeled segments as High, Medium, and Low value  
- Measured important metrics like overall revenue contribution  

**📈 Visualization:**

<img src="C:\Users\workl\AppData\Roaming\DBeaverData\workspace6\Sales_Analysis_Project\images\customer_segmentation.png" alt="Customer Segmentation" width="50%">

📊 **Key Takeaways:**
- High-value group (top 25%) contributes the majority share of revenue at 66% ($135.4M)  
- Medium-value group (middle 50%) brings in 32% of revenue ($66.6M)  
- Low-value group (bottom 25%) accounts for just 2% of revenue ($4.3M)  

💡 **Strategic Recommendations**
- **High-Value (66% revenue):** Launch a loyalty or rewards program tailored to the top spenders to deepen retention and reduce churn risk  
- **Medium-Value (32% revenue):** Introduce tier-based benefits or limited-time incentives to encourage more frequent or larger purchases, with the potential to elevate them to the high-value segment  
- **Low-Value (2% revenue):** Test automated win-back emails, discounts for cart abandonments, and product bundles to boost engagement and spending consistency  