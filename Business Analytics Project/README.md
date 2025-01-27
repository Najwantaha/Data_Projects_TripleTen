# Business Analytics for E-commerce Company

**Project Overview**

This project involves analyzing user activity data from an e-commerce company to provide insights into user interactions, conversion rates, and retention trends. The primary focus was to build a conversion funnel to understand how users interact with the website, prepare data for cohort analysis, and calculate retention rates for each cohort month by month. The goal was to identify areas where the company could improve in retaining users and converting them into paying customers.

## Objectives

The objectives of this analysis were to:
- Explore raw user activity data to understand how users engage with the website.
- Build a conversion funnel to track the flow of users from viewing products to completing a purchase.
- Perform cohort analysis to calculate monthly retention rates and track how users continue to interact with the platform over time.
- Provide actionable insights to the company to help them improve user retention and conversion rates.

### Key Questions:
- How do users interact with the website, from viewing products to making purchases?
- What are the conversion rates between viewing a product, adding it to the cart, and completing a purchase?
- How does user retention behave over time for different cohorts?
- What actions can the company take to improve user retention?

## Data Description

The dataset includes the following columns:

- **user_id**: Unique customer IDs.
- **event_type**: The type of activity by the user (e.g., viewing a product, adding to cart, purchase).
- **category_code**: The category of the product being viewed or purchased.
- **brand**: The company that makes the product.
- **price**: The price of the product, in USD.
- **event_date**: The date of the user activity, in `YYYY-MM-DD` format.

## What Was Done and How

1. **Explored Raw Data**
   - The raw data was thoroughly explored to understand user activities. This included analyzing the frequency and type of events (e.g., viewing products, adding to cart, purchases).

2. **Built Conversion Funnel**
   - A conversion funnel was built to track how users move through the website from viewing products to making a purchase.
   - The unique counts of users at each stage was calculated (viewing product → adding to cart → making a purchase) and used these counts to calculate conversion rates for each stage.

3. **Prepared Data for Cohort Analysis**
   - The data was prepared to perform cohort analysis by calculating the first purchase date for each user.
   - Cohorts were grouped by the month of the first purchase, and the users were tracked across multiple months to calculate retention rates.

4. **Calculated Retention Rates**
   - A pivot table was created to track monthly retention rates for each cohort. The table grouped users and transactions by the cohort's first purchase month.
   - Retention rates were calculated for each cohort using the formula in the retention table.
  
5. **Organized and Documented Spreadsheet**
   - The data, analysis, and results were organized into a clean, well-documented spreadsheet for easy understanding and reporting.
   - The cohort analysis and retention rates were included on separate sheets, making it easier to visualize and track user retention over time.

## Results
1. Retention rates gradually decreased over the first 4 months, with the company losing users at an alarming rate.
2. By month 4, retention rates dropped to 0%, suggesting that users who made their first purchase were not coming back to the platform.
3. This indicates a need for improvement in retaining users over time, as well as enhancing engagement strategies.

## Suggestions for the Company and Future Improvements
1. **Improving Conversion Rates**
The company should work on strategies to increase the conversion rate from product views to added items in the cart and from cart to purchase. This could involve offering discounts or reminders to users who add products to their cart but do not complete a purchase.

2. **Increasing Retention Rates**
To prevent users from dropping off, the company could improve the post-purchase experience by sending follow-up emails, offering loyalty rewards, or introducing features to re-engage users.

3. **Improved User Onboarding**
New users might be leaving the site due to a lack of engagement. The company could invest in improving user onboarding to retain first-time users and convert them into loyal customers.

4. **Advanced Cohort Analysis**
Future analyses could explore additional cohorts, such as by user demographics or source of traffic, to understand how different customer segments behave.

5. **Customer Feedback Integration**
Gathering direct feedback from customers regarding their shopping experience on the website could provide valuable insights into areas that need improvement.
