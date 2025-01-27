# Landscape Reviewing of Apps using Power BI

**Project Overview:**

This project involves reviewing apps listed on the Shopify platform to identify key factors that contribute to the success of Shopify apps. The analysis was performed using Power BI, where I created visualizations to uncover insights about app types, review patterns, and developer responsiveness. The project also included exploring relationships between tables and using DAX formulas to enhance the data model and generate new insights.

## Objective

The goals of this project were to:
- Analyze the types of apps available on the Shopify platform.
- Investigate reviews using DAX to measure app success based on user feedback.
- Identify app developers that are most responsive to customer reviews.
- Provide key statistics and visual insights into the app landscape on Shopify.

### Key Questions:
- What types of apps are most prevalent on the Shopify platform?
- How do review counts and ratings correlate?
- How helpful are the reviews, and how do developers respond to them?
- Which developers have the best responsiveness to user feedback?

## Data Description

The dataset, `shopify.xlsx`, contains public data scraped from the Shopify App Store and includes 4 key tables:

1. **apps**: Contains details of the apps listed on the Shopify app marketplace.
   - `id`: Unique identifier for each app.
   - `name`: Name of the app.
   - `lastmod`: Last modified date of the app.
   - Other details like price, developer, and status.

2. **apps_categories**: Join table connecting apps with categories.

3. **categories**: Contains categories that apps belong to. Each app can belong to multiple categories.

4. **reviews**: Contains reviews left by users for apps. Each review includes the rating, helpful_count, and developer response information.
   - `app_id`: ID of the app related to the review.
   - `rating`: Rating given by the user.
   - `helpful_count`: The number of people who found the review helpful.
   - `developer_reply`: Whether the developer has replied to the review.

## What Was Done and How

### App Landscape

The goal of this section was to analyze the types of apps available on the Shopify platform and understand the review trends.

1. **KPI Card for Unique Apps Count**:
   - A KPI card was created to show the unique number of apps listed on the Shopify platform.

2. **Line Chart of Review Count by Last Modified Date**:
   - A line chart was created showing the total review count on the Y-axis and the last modification date (`lastmod`) on the X-axis. This helped visualize the trends in app activity over time.

3. **Scatterplot of Reviews Count vs. Average Rating**:
   - A scatterplot was built comparing the number of reviews (`reviews_count`) with the average rating (`rating`) for each app. This helped identify apps with high numbers of reviews but low ratings and vice versa.

### Reviews

In this section, the focus shifted to analyzing the reviews in more depth, using DAX formulas to enhance insights.

1. **Helpful Reviews Column**:
   - A new column was created using DAX to weigh reviews by their helpfulness. The formula for the `helpful_reviews` column is:
   
     ```DAX
     helpful_reviews = reviews[rating] * (1 + reviews[helpful_count])
     ```
   
   - A card visualization was created to show the average helpful review score, which combined the rating and helpful count to give a more meaningful score for each review.

2. **Developer Answered Column**:
   - A new column, `developer_answered`, was created using a DAX expression to indicate whether the developer responded to the review. If the `developer_reply` column was not blank, the value was `1` (TRUE); otherwise, it was `0` (FALSE).

   ```DAX
   developer_answered = IF(ISBLANK(reviews[developer_reply]), 0, 1)

   
   - A scatterplot was made to compare the average rating (rating) by whether the developer responded (developer_answered). This analysis helped uncover patterns in how developer responses correlate with ratings.

 3. **App Reviews**:
    - The final section focuses on the relationships between apps and their reviews, with an emphasis on analyzing developer responsiveness.
    - A relationship was established between the **apps** table and the **reviews** table using the `app_id` column from the reviews table and the `id` column from the apps table. This relationship enabled further analysis of the reviews by linking them directly to the respective apps and developers.
    - A **bar chart** was created to show the sum of ratings for each developer. This visualization helped identify which developers received the most user feedback.
      
  4. **Helpful Reviews Average by Developer**:
     - A new **bar chart** was created to compare the average helpful review score (`helpful_reviews`) by each developer. This chart provided a clearer understanding of which developers received more helpful feedback on average, combining both rating and helpful count.

5. **Developer Responsiveness Analysis**:
   - A **bar chart** was created to compare the responsiveness of developers by using the `developer_answered` column, which measures how many developers responded to reviews. A filter was applied to only display developers with more than 500 reviews, ensuring that the chart highlights developers with significant user feedback.

  ## Results

### Key Insights:
- The most successful apps are often those with a high number of reviews and high average ratings.
- Developers who respond to reviews tend to receive higher ratings from users. The correlation between developer responses and positive feedback suggests that active engagement with customers can improve user satisfaction.
- Some apps, even with a high review count, tend to have lower ratings, which may indicate dissatisfaction with certain features.

### Top Responsive Developers:
- A few developers stood out for their high responsiveness to user reviews. These developers actively engage with customer feedback, which likely contributes to higher ratings and user trust.

## Suggestions for App Developers and Next Steps

### 1. Focus on Developer Engagement:
   - Developers who respond to reviews tend to see better ratings. It's essential for developers, especially for high-volume apps, to have a structured process for responding to customer feedback promptly. Engaging with users' concerns can lead to higher ratings and improved customer loyalty.

### 2. Increase Review Quality:
   - While having many reviews is important, ensuring that reviews are helpful should be a priority. Developers should focus on improving app quality and encouraging users to leave detailed, constructive reviews. 

### 3. Further Analysis:
   - Additional analyses can be performed to explore trends over time, such as how new features or updates impact reviews and ratings. 
 
