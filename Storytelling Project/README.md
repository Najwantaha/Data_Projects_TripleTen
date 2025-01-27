# Storytelling with Data Using Tableau 

**Project Overview:**

This project involves using Tableau to analyze the root causes of returned orders for a client. The primary goal was to build interactive visualizations to help identify factors influencing return rates. A well-structured dashboard was created to monitor returns, and a comprehensive story was constructed to explain the findings and guide the client in taking actionable steps to reduce returns and improve profitability.

## Objective and Goals

The objectives of this project were to:
- Build various visualizations to understand the factors contributing to returned orders.
- Analyze return rates across different dimensions, including product categories, customer types, geography, and time.
- Create a user-friendly dashboard to monitor return rates and identify key insights.
- Present a comprehensive story that explains the analysis, how to interpret the dashboard, and the actions the client can take based on the findings.

### Key Questions:
- What is causing the returns?
- Are there certain products, customers, or regions that contribute disproportionately to returns?
- Can we identify seasonal trends in returns?
- How can the client use this data to take actionable steps and reduce returns?

## Data Description

The analysis was based on data from two key tables:
- **Orders Table**: Contains information about each order, including the product, customer, price, and date.
- **Returns Table**: Contains information about whether each item was returned (with "Yes" for returned and "null" for not returned).

The **Returned** field was converted into a calculated field with values of 1 for "Yes" and 0 for "null", which was then used to calculate return rates and total returns.

## What Was Done and How

### 1. **Identifying Root Causes for Returns**

Several visualizations were created to analyze the root causes of returns:
   
- **Scatterplot of Total Sales vs. Total Returns by Product Subcategory**:
   - This visualization was used to check if there is a correlation between total sales and total returns across different product subcategories.
   - By analyzing this scatterplot, we identified whether sales volume tends to increase or decrease with return rates, and whether any subcategories exhibited unusual return patterns.

   **Analysis:**
   - In some cases, higher sales were associated with higher returns, but other product subcategories showed no clear correlation.

- **Bar Chart of Return Rate by Product Category**:
   - A bar chart was created to visualize the return rate by product category. This helped identify categories with unusually high or low return rates.
  
   **Analysis:**
   - Some product categories had significantly higher return rates than others, suggesting issues with product quality or customer satisfaction.

- **Return Rate by Customer**:
   - A visualization was built to identify customers who returned products more frequently. The analysis filtered out customers with only one order to focus on those with multiple returns.
   
   **Analysis:**
   - A small number of customers accounted for a disproportionate number of returns, which helped identify potential fraud or dissatisfaction among repeat customers.

- **Return Rate by Geography (State)**:
   - A map was created to analyze whether certain geographic locations had higher return rates.
   - This geographic analysis helped identify regions where returns were more concentrated.

   **Analysis:**
   - Certain states or cities showed higher return rates, which could indicate regional issues with product quality, shipping, or customer expectations.
     
- **Return Rate by Time (Month)**:
   - A line graph was created to analyze seasonal trends in return rates. This visualization helped determine whether returns were more frequent during specific months or seasons.

   **Analysis:**
   - The data showed a spike in returns after certain holiday seasons, suggesting that customers may be dissatisfied with gifts or post-holiday shopping.

- **Composite Charts of Return Rates**:
   - Two different composite charts were created to analyze return rates across multiple dimensions (e.g., time + geography or time + product category).
   - These charts provided deeper insights into how different factors combined to affect return rates.

   **Analysis:**
   - Composite charts highlighted specific time periods and geographic areas where returns were particularly problematic.

### 2. **Building a Dashboard for Monitoring Returns**

- **Low-Fidelity Mock-ups**: 
   - A series of hand-drawn sketches were created to outline the layout of the dashboard. These mock-ups helped visualize the flow and arrangement of key visualizations.

- **Dashboard Template**:
   - Using Tableau, a dashboard template was created, placing the visualizations into a cohesive layout.
   
   **Final Dashboard**:
   - The finalized dashboard included filters for product category, time period, and geography, enabling users to drill down into specific return trends and identify root causes.
  Link: [Dashboard](https://public.tableau.com/app/profile/najwan.taha/viz/Sprint5Project_17338631018010/MonitoringReturns)
  
### 3. **Presenting the Analysis and Dashboard**

- **Story Creation**:
   - A Tableau Story was constructed to present the analysis in a logical sequence, guiding the client through the findings and showing how the dashboard can be used.
   - The story included:
     - A summary of the return rate analysis.
     - An explanation of how returns should be measured (e.g., by return rate, total cost, or number of returns).
     - Identification of key root causes for returns.
     - An overview of the dashboard, with step-by-step instructions on how to interpret each visualization and use the filters.
     - Actionable steps that can be taken based on the insights from the dashboard.

## Results

- **Root Causes Identified:**
  - High return rates were concentrated in specific product categories and regions. Additionally, certain customers and time periods showed unusually high return rates, indicating potential quality issues or customer dissatisfaction.
  
- **Dashboard Utility:**
  - The dashboard provides a comprehensive overview of return trends, allowing the client to easily identify problem areas and take proactive measures to reduce returns.

## Suggestions for the Company and Next Steps

1. **Address High-Return Categories:**
   - Focus on investigating and improving product quality in categories with high return rates.

2. **Customer Engagement:**
   - Target customers with high return rates for follow-up or potential loyalty programs to improve satisfaction.

3. **Geographic Focus:**
   - Investigate regional issues related to returns and consider adjusting marketing or shipping strategies for high-return areas.

4. **Seasonal Trends:**
   - Implement measures to reduce returns during peak shopping seasons, such as post-purchase support or clearer product descriptions.

5. **Continuous Monitoring:**
   - Regularly update the dashboard to track changes in return rates and continuously monitor product and customer behavior.
