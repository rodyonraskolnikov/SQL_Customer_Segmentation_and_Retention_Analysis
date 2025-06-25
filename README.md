 # Intermediate SQL - Sales Analysis

 ## Overview
 {insert overview here}

 ## Business Questions
 1. 
 2. **Cohort Analysis:** How do different customer groups generate revenue? 
 3. 

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

 ![image_name](image_name.png)

 **Key Findings:**
 - **Revenue per customer** shows an alarming decreasing trend over time  
    - **2022–2024 cohorts** are consistently performing worse than earlier cohorts  
    - **NOTE:** Although net revenue is increasing, this is likely due to a larger customer base, which is **not reflective of customer value**

 **Business Insights**
 - **Value extracted from customers** is decreasing over time and needs further investigation.  
- In **2023**, we saw a **drop in number of customers acquired**, which is concerning.  
- With both **lowering LTV** and **decreasing customer acquisition**, the company is facing a **potential revenue decline**.

 ## Strategic Recommendations

 1. {insert strategic recommendations here}

 ## Technical Details