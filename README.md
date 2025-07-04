# Amazon-Case-study
Welcome to the RetailTech Insights E-commerce Analytics Repository. 
## Outline
- [Project Overview](#project-overview)
- [Data source](#data-source)
- [Tools used](#tools-used)
- [Data Transformation Process](data-transformation-process)
- [Business Questions](#business-questions)
- [Visualization](visualization)
- [Result and Insights](#result-and-insights)
- [Recommendations](#Recommendations)
- [Conclusion](#conclusion)

## Project Overview
This project focuses on analyzing, and transforming product and customer review data meticulously scraped from Amazon product pages into actionable intelligence. Our core mission is to generate comprehensive insights that will empower businesses to:
 - Enhance Product Offerings: Identify product strengths and weaknesses, uncover emerging trends, and pinpoint opportunities for innovation and improvement based on direct customer feedback.
 - Inform Marketing Strategies: Optimize targeting, refine messaging, and develop more effective campaigns by understanding customer preferences, pain points, and purchase drivers.
 - Improve Customer Engagement: Foster stronger customer relationships through a deeper understanding of their needs, leading to enhanced satisfaction and loyalty.
By leveraging the rich tapestry of Amazon data, this repository aims to be a valuable resource for data-driven decision-making in the dynamic e-commerce landscape.

## 📁Data source
 - Amazon Case Study.xlsx [Download Here](https://canvas.instructure.com/files/302721266/download?download_frd=1)

   **Dataset Description**
   The dataset consists of essential information about products and customer interactions, including:
     - Product Details: Name, category, price, discount, and ratings
     - Customer Engagement: User reviews, titles, and content

## 🧰**Tools used**
- Microsoft Excel [Download Here](https://microsoft-excel.en.softonic.com/)
  - Power Query Editor 
  - Pivot Tables
  - Calculated Columns
  - Charts (Bar, Column, Combo)

## 🧹Data Transformation Process
After downloading the raw data, several crucial steps were taken to clean and prepare it for analysis on Microsoft Excel. This ensured data integrity and facilitated more insightful findings:
- Duplicate Removal: To maintain data uniqueness, duplicate entries were identified and removed. Duplicates were eliminated based product name, ensuring that each row represents a unique product.
- Text Cleaning and Formatting: Within the Power Query Editor, text data underwent significant cleaning:
   - Excessive spacing was trimmed from words to ensure consistency and improve readability.
   - Spaces were then inserted into concatenated words to format the data appropriately (e.g., "Home&Kitchen" became "Home & Kitchen").
- Product Recategorization: For enhanced analysis, products were reclassified into a new, simplified column called **'Product Category'**  using a delimiter =LEFT(C2, FIND("|", C2) - 1). For example, a category like "Computers & Accessories|Accessories&Peripherals" might be simplified to "Computers & Accessories" within the new 'Product Category' column.  
- Price Range Creation: A new column, 'Price Range', was introduced to categorize products based on their price. This was achieved using the following IF function. This formula automatically assigns each product to a predefined price bracket, allowing for a more granular analysis of pricing tiers. 


## 🧠Business Questions 

1. What is the average discount percentage by product category?
2. How many products are listed per category?
3. What is the total number of reviews per category?
4. What is the number of unique products per price range bucket (e.g. <₹200, ₹200–₹500, >₹500)?
5. What is the average actual vs discounted price by category?
6. Which products have the highest number of reviews?
7. How many products have a discount of 50% or more?
8. What is the distribution of product ratings (e.g., how many rated 3.0, 4.0)?
9. What is the total potential revenue (actual_price × rating_count) by category?
10. Which products have the highest average ratings?
11. How does rating relate to discount level?
12. How many products have fewer than 1,000 reviews?
13. Which categories have products with the highest discounts?
14. Identify the top 5 products in terms of combined rating and number of reviews.

## 📊Visualization 
![Average Discount by Product Category](https://github.com/user-attachments/assets/14c8da9b-0084-4084-a5b2-d12c05ca1d39)

![Total Number of Products per Category ](https://github.com/user-attachments/assets/9370e617-a73e-4a9e-80b5-19de961d2676)

![Rating Relationship to the Level of Discount ](https://github.com/user-attachments/assets/38319a9f-6995-4756-97d9-45d6f1c6bd60)

![Top Discount Category](https://github.com/user-attachments/assets/ff86cd4f-fa43-4653-a12a-33e38be71549)


## 📈Result and Insights

 - **Discounting strategies are effective for both low and high-rated products:** We saw that steep discounts aren't just for unpopular items. The data reveals that high average discounts (over 80%) occur on products with lower ratings (around 2.8), suggesting a strategy to clear less popular inventory or incentivize purchases of underperforming items. Interestingly, the highest-rated products (rating of 5) also show significant average discounts (approaching 70%), which could be a tactic to reward loyal customers, drive sales volume on popular items, or maintain competitive pricing.
 - **Electronics & Computers and Accessories Rule the Roost:** These categories are Amazon's heavy hitters, raking in tons of reviews and showing massive potential for revenue. Certain items, like "boAt Bassheads 100 Earphones" and "Amazon Basics HDMI Cables," are clear winners, frequently appearing among the highest-rated and most-reviewed products.
 - **Review Gaps Exist:** While some categories are overflowing with reviews, others, like "Car & Motorbike" and "Health & Personal Care" have far fewer.
 - **Price Range Distribution Highlights Mid-Tier Popularity:** The 5,001-10,000 price range has the highest number of unique products (117)[cite: 84, 95], suggesting that a significant portion of Amazon's product catalog falls within this mid-tier pricing.

## Recommendations:
 - **Optimize Discounting:** Let's fine-tune when and how we offer discounts, ensuring they drive profits whether products are top-rated or need a boost. Are the high discounts on low-rated products effectively clearing inventory without significantly eroding profit margins? This will help refine discounting strategies, ensuring they are optimized for profitability and inventory management across the product rating spectrum.
 - **Focus on the Big Guns:** Given their high review volume and potential revenue; investing in Electronics and Computers & Accessories are key to major growth. 
 - **Leverage Top-Performing Products for Cross-Promotion:** Let's actively promote and bundle those highly-rated, highly-reviewed products to attract even more customers.
 - **Boost Review Generation:** We need to encourage more reviews for categories that are currently lagging to build trust and visibility.



**5. Analyze the "Blank" Rating Category and Price Range Gaps:**
    * [cite_start]**Action:** Investigate why a "blank" rating category exists and why it has the lowest average discount[cite: 2]. Additionally, explore why certain price ranges, such as those not listed or with very few products, have lower unique product counts. This could indicate missed market opportunities.
    * **Impact:** Understanding these gaps can uncover data quality issues, identify unaddressed customer segments, or reveal opportunities for new product introductions.

## Conclusion:

The Amazon sales data highlights a dynamic marketplace where discount strategies are applied across the rating spectrum, and certain product categories, particularly Electronics and Computers & Accessories, are dominant revenue and engagement drivers. The success of specific products like boAt Bassheads and Amazon Basics HDMI cables underscores the importance of product quality and effective branding. To further optimize performance, the repository should focus on refining discounting tactics, doubling down on high-performing categories and products, and actively addressing areas with lower engagement or data anomalies. By leveraging these insights, Amazon can further enhance its sales strategies and capitalize on market opportunities.

