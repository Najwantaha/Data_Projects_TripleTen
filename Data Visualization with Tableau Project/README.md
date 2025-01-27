# Data Visualization with Tableau – Superstore Operations Review

**Project Overview:**

This project involves analyzing and visualizing the operations of a superstore to help identify key issues affecting profitability and to provide actionable insights. Using Tableau, we built visualizations for profit and loss analysis, advertising effectiveness, and product returns. The goal was to help the store avoid bankruptcy by providing clear and data-driven recommendations on areas to focus on or improve.

## Objectives

The goals of this project were to:
- Review the store’s operations and identify important centers of profit and loss.
- Determine whether advertising would be a worthwhile investment based on state and month combinations.
- Analyze product returns to detect any abnormal return rates and provide insights on which products or customers to target for improvement.
- Provide a comprehensive dashboard summarizing the findings and recommendations for the store's management team.

### Key Questions:
- **Profits & Losses:** Which product categories or regions are the biggest profit centers and loss-makers? Which products should the store stop selling, and which subcategories should be focused on or removed?
- **Advertising:** Is advertising worth the investment, and if so, which states and months are the most profitable for advertising?
- **Returned Items:** Which products or customers have the highest return rates? How does product return rate relate to profit, and should certain business strategies change based on this information?

## Data Description

The analysis was conducted using data from multiple tables related to sales, returns, and advertising effectiveness, including:

- **Orders table**: Information about each order made by customers, including order date, product ID, shipping mode, and profit.
- **Returns table**: Contains data about whether products were returned or not (with "Yes" or "null" indicating return status).
- **Product information**: Details on each product's category, subcategory, and sales performance.
- **Advertising data**: Metrics on advertising campaigns and their performance by region and time.

## What Was Done and How

### 1. **Profits & Losses Visualization:**
   - We analyzed which pairs of dimensions (e.g., subcategory + region, or shipping mode + product ID) had the highest profit and the greatest loss.
   - Visualizations were created to highlight the most profitable and the most loss-making areas, including a breakdown of profits by subcategory and region.
   - For the products that should be discontinued, visualizations were made to identify products with negative or low profits.

   **Analysis:**  
   - Identified the top 2 profit centers and top 2 loss-makers, which helped to focus on improving operations in loss-making areas.
   - Visualized products and subcategories that had negative or low profits, advising the store to stop selling these items.

### 2. **Advertising Visualization:**
   - For advertising analysis, we created a visualization that shows the average profit per unit sold by month and state to determine the best time and place to advertise.
   - The top 3 state and month combinations with the highest average profit were identified to suggest when advertising would be most effective.

   **Analysis:**  
   - Identified the 3 best states and months for advertising and calculated the potential advertising budget based on expected return on investment.
   - Visualized average profits by month for those top states and analyzed how much the store should be willing to spend on advertising during those months.

### 3. **Returned Items Visualization:**
   - We used the Returns table to analyze the rate at which products were being returned and to identify which products and customers had the highest return rates.
   - A calculated field was created in Tableau to convert the "Returned" field into 1 (for Yes) and 0 (for null), allowing for easy visualization of return rates.
   - We visualized the correlation between product return rate and average profit to determine if the store should continue selling certain products.

   **Example Analysis:**  
   - Identified products with the highest return rates and highlighted customers who return products most frequently.
   - Explored the relationship between return rates and profit to determine whether the store should keep selling high-return-rate products.
   -  A separate visualization was made showing the average return rate and average profit by shipping mode, product type, or state to determine if certain strategies should change.

### Dashboard Creation:
   - A comprehensive dashboard was created in Tableau to summarize all the visualizations and insights gathered.
   - The dashboard includes:
     - Profit and loss analysis.
     - Advertising effectiveness by state and month.
     - Return rates and their impact on profitability.
   - This dashboard serves as a tool for the store's management to quickly assess operations and make data-driven decisions.

   **Example Dashboard:**
   link: [https://public.tableau.com/views/Sprint4Project_17319757631570/Dashboard1?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link](https://public.tableau.com/app/profile/najwan.taha/viz/Sprint4Project_17319757631570/Dashboard1)

## Results

- **Profits & Losses:** 
  - Identified key product subcategories and regions contributing to high profits, while also highlighting underperforming areas that need attention.
  - Recommended discontinuing certain products with low or negative profits.
  
- **Advertising Effectiveness:**
  - The analysis identified the best states and months to focus advertising efforts, with a clear ROI justification for each recommendation.
  - Suggested advertising budgets for the identified top-performing states and months based on average profit.

- **Returned Items:**
  - Visualized products with abnormal return rates, allowing the store to target and investigate high-return-rate products.
  - Showed how high-return-rate products negatively affect overall profitability, suggesting strategic changes in product offerings or quality control.

## Suggestions for the Company and Future Improvements

1. **Profitable Products:** 
   - Focus more on the high-profit product categories and consider discontinuing products that result in losses.
  
2. **Advertising Strategy:** 
   - Use the insights from the advertising analysis to guide marketing efforts, particularly during peak months for certain states.

3. **Product Return Management:** 
   - Investigate high-return-rate products and implement quality control or change product offerings.
   - Reevaluate the return policies or improve the product descriptions to reduce unnecessary returns.

4. **Continuous Monitoring:**
   - Regularly monitor these key metrics to identify new opportunities and areas for improvement. Use the Tableau dashboard for ongoing analysis and decision-making.
