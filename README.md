 # Intermediate SQL - Sales Analysis

 ## Overview
Analysis of customer behavior, retention, and lifetime value for an e-commerce company to improve customer retention and maximize revenue.

## Business Questions

1. **Customer Segmentation:** Who are our most valuable customers?
2. **Cohort Analysis:** How do different customer groups generate revenue?
3. **Retention Analysis:** Which customers haven't purchased recently?
k
 # Analysis Approach

 ### 1. Customer Segmentation Anaylsis

- Categorized customers based on total lifetime value (LTV)
- Assigned customers to High, Mid, and Low-value segments
- Calculated key metrics: total revenue


 Query: [1_customer_segmentation.sql](1_customer_segmentation.sql)

 ## Visualization ##

 ![Customer segmentation pie chart](images/6.3_customer_segementation.png)

 **Key Findings:**
- High-value segment (25% of customers) drives 66% of revenue ($135.4M)
- Mid-value segment (50% of customers) generates 32% of revenue ($66.6M)
- Low-value segment (25% of customers) accounts for 2% of revenue ($4.3M)

 **Business Insights**
- High-Value (66% revenue): Offer premium membership program to 12,372 VIP customers, as losing one customer significantly impacts revenue
- Mid-Value (32% revenue): Create upgrade paths through personalized promotions, with potential $66.6M → $135.4M revenue opportunity
- Low-Value (2% revenue): Design re-engagement campaigns and price-sensitive promotions to increase purchase frequency

 ### 2. Cohort Analysis
 - Tracked revenue and customer count per cohorts
 - Cohorts were grouped by year of first purchase
 - Analyzed customer retention at a cohort level

 Query: [2_cohort_analysis.sql](/2_cohort_analysis.sql)


 ## Visualization ##

 Customer Revenue by Cohort (Adjusted for time in market) - First Purchase Date

 ![image_name](images/5.2_customer_revenue_normalized.png)

 Investigate Monthly Revenue & Customer Trends (3 Month Rolling Average)

![image_name](images/5.2_monthly_revenue_customers_3mo.png)

 **Key Findings:**
 
* Customer revenue is falling — older cohorts (2016–2018) spent over \$2,800, while the 2024 cohort averages only around \$1,970.
* Both revenue and customer numbers peaked in 2022–2023 but are now declining in 2024.
* Revenue and customer metrics show high volatility, with steep drops in 2020 and 2024, highlighting persistent retention issues.


 **Business Insights:**

* Improve retention and reduce churn by offering personalized incentives to recent cohorts (2022–2024).
* Address revenue instability by launching loyalty programs or subscriptions to promote consistent customer spending.
* Analyze cohort behavior and apply effective tactics from high-value cohorts (2016–2018) to newer groups.


  ### 3. Customer Retention

- Identified customers at risk of churning  
- Analyzed last purchase patterns  
- Calculated customer-specific metrics

 Query: [3_retention_analysis.sql](3_retention_analysis.sql)

 ## Visualization ##

 ![Customer Churn by Cohort Year](images/7.3_customer_churn_cohort_year.png)

 **Key Findings:**
- Cohort churn stabilizes at ~90% after 2–3 years, indicating a predictable long-term retention pattern.  
- Retention rates are consistently low (8–10%) across all cohorts, suggesting retention issues are systemic rather than specific to certain years.  
- Newer cohorts (2022–2023) show similar churn trajectories, signaling that without intervention, future cohorts will follow the same pattern.

 **Business Insights**
- Strengthen early engagement strategies to target the first 1–2 years with onboarding incentives, loyalty rewards, and personalized offers to improve long-term retention.  
- Re-engage high-value churned customers by focusing on targeted win-back campaigns rather than broad retention efforts, as reactivating these users may yield higher ROI.
- Predict & preempt churn risk and use customer-specific warning indicators to proactively intervene with at-risk users before they lapse.

 ## Strategic Recommendations

1. **Customer Value Optimization** (Customer Segmentation)  
   - Launch VIP program for 12,372 high-value customers (66% revenue)  
   - Create personalized upgrade paths for mid-value segment ($66.6M → $135.4M opportunity)  
   - Design price-sensitive promotions for low-value segment to increase purchase frequency

2. **Cohort Performance Strategy** (Customer Revenue by Cohort)  
   - Target 2022–2024 cohorts with personalized re-engagement offers  
   - Implement loyalty/subscription programs to stabilize revenue fluctuations  
   - Apply successful strategies from high-spending 2016–2018 cohorts to newer customers

3. **Retention & Churn Prevention** (Customer Retention)  
   - Strengthen first 1–2 year engagement with onboarding incentives and loyalty rewards  
   - Focus on targeted win-back campaigns for high-value churned customers  
   - Implement proactive intervention system for at-risk customers before they lapse

## Technical Details

- **Database:** PostgreSQL  
- **Analysis Tools:** PostgreSQL, DBeaver
- **Visualization:** ChatGPT
