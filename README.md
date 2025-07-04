# Amazon-Case-study
Welcome to the RetailTech Insights E-commerce Analytics Repository. This project focuses on analyzing, and transforming product and customer review data meticulously scraped from Amazon product pages into actionable intelligence. Our core mission is to generate comprehensive insights that will empower businesses to:
 - Enhance Product Offerings: Identify product strengths and weaknesses, uncover emerging trends, and pinpoint opportunities for innovation and improvement based on direct customer feedback.
 - Inform Marketing Strategies: Optimize targeting, refine messaging, and develop more effective campaigns by understanding customer preferences, pain points, and purchase drivers.
 - Improve Customer Engagement: Foster stronger customer relationships through a deeper understanding of their needs, leading to enhanced satisfaction and loyalty.
By leveraging the rich tapestry of Amazon data, this repository aims to be a valuable resource for data-driven decision-making in the dynamic e-commerce landscape.

## Outline
- [Project Overview](#project-overview)
- [Data source](#data-source)
- [Tools used](#tools-used)
- [Business Questions from Case study](#business-questions-from-case-study)
- [Result and Insights](#result-and-insights)
- [Recommendation](#Recommendation)
- [Conclusion](#conclusion)
- 
## 📁 Data source
 - Amazon Case Study.xlsx [Download Here](https://canvas.instructure.com/files/302721266/download?download_frd=1)

   **Dataset Description**
   The dataset consists of essential information about products and customer interactions, including:
     - Product Details: Name, category, price, discount, and ratings
     - Customer Engagement: User reviews, titles, and content

## 🧰 **Tools used**
- Microsoft Excel [Download Here](https://microsoft-excel.en.softonic.com/)
  - Power query editor 
  - Pivot Tables
  - Calculated Columns
  - Charts (Bar, Column, Combo)

## Data Transformation Process
After downloading the raw data, several crucial steps were taken to clean and prepare it for analysis on Microsoft Excel. This ensured data integrity and facilitated more insightful findings:
- Duplicate Removal: To maintain data uniqueness, duplicate entries were identified and removed. Conditional formatting was initially used to highlight cells containing duplicate values. Subsequently, duplicates were eliminated based product name, ensuring that each row represents a unique product.
- Text Cleaning and Formatting: Within the Power Query Editor, text data underwent significant cleaning:
- Excessive spacing was trimmed from words to ensure consistency and improve readability.
- Spaces were then inserted into concatenated words to format the data appropriately (e.g., "Home&Kitchen" became "Home & Kitchen").
- Product Recategorization: For enhanced analysis, products were reclassified into a new, simplified column called **'Product Category'**. This involved replacing the initial words of existing categories with more concise terms. For example, a category like "Computers & Accessories|Accessories&Peripherals|Cables&Accessories|Cables|USBCables" might be simplified to "Computers & Accessories" within the new 'Product Category' column. This can also be done by using a delimiter =LEFT(C2, FIND("|", C2) - 1)
- Price Range Creation: A new column, 'Price Range', was introduced to categorize products based on their price. This was achieved using the following IF function:
=IF(F2<1000,"<1,000",IF(F2<=5000,"1,000–5,000",IF(F2<=10000,"5,001–10,000",IF(F2<=20000,"10,001–20,000",IF(F2<=50000,"20,001–50,000",IF(F2<=100000,"50,001–100,000",">100,000"))))))
This formula automatically assigns each product to a predefined price bracket, allowing for a more granular analysis of pricing tiers. 

After cleaning, a pivot table was inserted on a new worksheet to answer the questions 

## 🧠 Business Questions (Task to do)

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



