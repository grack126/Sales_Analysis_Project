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

<img src="images\customer_segmentation.png" alt="Customer Segmentation" width="80%">
<a href="https://public.tableau.com/views/COntoso_customer_segmentation/Dashboard1?:language=en-GB&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link" target="_blank">🔗 View the Interactive Tableau Dashboard</a>

📊 **Key Takeaways:**
- High-value group (top 25%) contributes the majority share of revenue at 66% ($135.4M)  
- Medium-value group (middle 50%) brings in 32% of revenue ($66.6M)  
- Low-value group (bottom 25%) accounts for just 2% of revenue ($4.3M)  

💡 **Strategic Recommendations**
- **High-Value (66% revenue):** Launch a loyalty or rewards program tailored to the top spenders to deepen retention and reduce churn risk  
- **Medium-Value (32% revenue):** Introduce tier-based benefits or limited-time incentives to encourage more frequent or larger purchases, with the potential to elevate them to the high-value segment  
- **Low-Value (2% revenue):** Test automated win-back emails, discounts for cart abandonments, and product bundles to boost engagement and spending consistency 

### 2. Customer Revenue by Cohort
**🖥️ Query**: [2_cohort_analysis.sql](2_cohort_analysis.sql)

- Tracked revenue and customer count per cohorts
- Cohorts were grouped by year of first purchase
- Analyzed customer revenue at a cohort level

**📈 Visualization:**

<img src="images\cohort_analysis_final.png" alt="Customer Revenue Normalized" width="80%">
<a href="https://public.tableau.com/views/Contoso_cohort_analysis/Dashboard1?:language=en-GB&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link" target="_blank">🔗 View the Interactive Tableau Dashboard</a>


📊 **Key Findings:**  
- Customer revenue is declining, older cohorts (2016-2018) spent ~$2,800+, while 2024 cohort spending dropped to ~$1,970.  
- Revenue and customers peaked in 2022-2023, but both are now trending downward in 2024.  
- High volatility in revenue and customer count, with sharp drops in 2020 and 2024, signaling retention challenges.  

💡 **Business Insights:**  
- Boost retention & re-engagement by targeting recent cohorts (2022-2024) with personalized offers to prevent churn.  
- Stabilize revenue fluctuations and introduce loyalty programs or subscriptions to ensure consistent spending.  
- Investigate cohort differences by applying successful strategies from high-spending cohorts (2016-2018) to newer ones.

### 3. Customer Retention
🖥️ Query: [customer_retention.sql](customer_retention.sql)

- Identified customers at risk of churning
- Analyzed last purchase patterns
- Calculated customer-specific metrics

**📈 Visualization:**

<img src="images\churn_analysis.png" alt="Customer Churn by Cohort Year" style="width: 80%; height: auto;">
<a href="https://public.tableau.com/views/Total_customer_retention_churn_per_cohort/Dashboard1?:language=en-GB&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link" target="_blank">🔗 View the Interactive Tableau Dashboard</a>

📊 **Key Findings:**  
- Cohort churn stabilizes at ~90% after 2-3 years, indicating a predictable long-term retention pattern.  
- Retention rates are consistently low (8-10%) across all cohorts, suggesting retention issues are systemic rather than specific to certain years.  
- Newer cohorts (2022-2023) show similar churn trajectories, signaling that without intervention, future cohorts will follow the same pattern.  

💡 **Business Insights:**  
- Strengthen early engagement strategies to target the first 1-2 years with onboarding incentives, loyalty rewards, and personalized offers to improve long-term retention.  
- Re-engage high-value churned customers by focusing on targeted win-back campaigns rather than broad retention efforts, as reactivating valuable users may yield higher ROI.  
- Predict & preempt churn risk and use customer-specific warning indicators to proactively intervene with at-risk users before they lapse.

## Strategic Recommendations

1. **Customer Value Optimization** (Customer Segmentation)
   - Launch VIP program for 12,372 high-value customers (66% revenue)
   - Create personalized upgrade paths for mid-value segment ($66.6M → $135.4M opportunity)
   - Design price-sensitive promotions for low-value segment to increase purchase frequency

2. **Cohort Performance Strategy** (Customer Revenue by Cohort)
   - Target 2022-2024 cohorts with personalized re-engagement offers
   - Implement loyalty/subscription programs to stabilize revenue fluctuations
   - Apply successful strategies from high-spending 2016-2018 cohorts to newer customers

3. **Retention & Churn Prevention** (Customer Retention)
   - Strengthen first 1-2 year engagement with onboarding incentives and loyalty rewards
   - Focus on targeted win-back campaigns for high-value churned customers
   - Implement proactive intervention system for at-risk customers before they lapse

## Technical Details
- **Database:** PostgreSQL
- **Analysis Tools:** PostgreSQL, Dbeaver
- **Visualization:** Tableau