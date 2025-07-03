# Amazon-Case-study
Welcome to the RetailTech Insights E-commerce Analytics Repository. This project focuses on analyzing, and transforming product and customer review data meticulously scraped from Amazon product pages into actionable intelligence. Our core mission is to generate comprehensive insights that will empower businesses to:
 - Enhance Product Offerings: Identify product strengths and weaknesses, uncover emerging trends, and pinpoint opportunities for innovation and improvement based on direct customer feedback.
 - Inform Marketing Strategies: Optimize targeting, refine messaging, and develop more effective campaigns by understanding customer preferences, pain points, and purchase drivers.
 - Improve Customer Engagement: Foster stronger customer relationships through a deeper understanding of their needs, leading to enhanced satisfaction and loyalty.
By leveraging the rich tapestry of Amazon data, this repository aims to be a valuable resource for data-driven decision-making in the dynamic e-commerce landscape.

## Data source
 - Amazon Case Study.xlsx [Download Here](https://canvas.instructure.com/files/302721266/download?download_frd=1)

   **Dataset Description**
   The dataset consists of essential information about products and customer interactions, including:
     - Product Details: Name, category, price, discount, and ratings
     - Customer Engagement: User reviews, titles, and content

## **Tools used**
Microsoft Excel [Download Here](https://microsoft-excel.en.softonic.com/)

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

## Business Questions (Task to do)

1. What is the average discount percentage by product category?
The highest average discount percentage by product category is Home Improvement with 58%. Other products category average discount percentage include: Car & Motorbike 42%; Computers & Accessories 53%; Electronics 49%; Health & Personal Care 53%; Home & Kitchen Appliances 40%; Musical Instruments 46%; Office Products 12%; Toys & Games 0%	

2. How many products are listed under each category?
   The total count of products per category include:
   - Car & Motorbike:	1
   - Computers & Accessories	375
   - Electronics:	476
   - Health & Personal Care:	1
   - Home & Kitchen Appliances:	448
   - Home Improvement:	2
   - Musical Instruments: 2
   - Office Products:	31
   - Toys & Games:	1

4. What is the total number of reviews per category?
   Sum of rating count per product category:
   - Car & Motorbike:	1,118
   - Computers & Accessories:	6,335,177
   - Electronics:	13,938,131
   - Health & Personal Care:	3,663
   - Home & Kitchen Appliances:	2,991,069
   - Home Improvement:	8,566
   - Musical Instruments:	88,882
   - Office Products:	149,675
   - Toys & Games:	15,867

5. Which products have the highest average ratings?
Three products had the highest average ratings of 5 and they include: 
- Amazon Basics Wireless Mouse | 2.4 GHz Connection, 1600 DPI | Type - C Adapter | Upto 12 Months of Battery Life | Ambidextrous Design | Suitable for PC/Mac/Laptop
- REDTECH USB-C to Lightning Cable 3.3FT, [Apple MFi Certified] Lightning to Type C Fast Charging Cord Compatible with iPhone 14/13/13 pro/Max/12/11/X/XS/XR/8, Supports Power Delivery - White
- Syncwire LTG to USB Cable for Fast Charging Compatible with Phone 5/ 5C/ 5S/ 6/ 6S/ 7/8/ X/XR/XS Max/ 11/12/ 13 Series and Pad Air/Mini, Pod & Other Devices (1.1 Meter, White)

6. What is the average actual price vs the discounted price by category?

6. Which products have the highest number of reviews?
   The products with the highest number of reviews are:
   - Amazon Basics High-Speed HDMI Cable, 6 Feet (2-Pack),Black	with a total of 426,973
   - Amazon Basics High-Speed HDMI Cable, 6 Feet - Supports Ethernet, 3D, 4K video,Black		with a total of426,973
   - Amazon Basics Flexible Premium HDMI Cable (Black, 4K@60Hz, 18Gbps), 3-Foot		with a total of 426,973


8. How many products have a discount of 50% or more?
A total number of 653 products had a discount of 50% and more. One product had a discount of 94%, and 91%, 89% respectively. 53 products were rated 50%; 7 products with a discount of 90%; 
14: 51%, 13 52%; 23 53%; 22 54%
9. What is the distribution of product ratings (e.g., how many products are rated 3.0,

4.0, etc.)?

9. What is the total potential revenue (actual_price × rating_count) by category?

10. What is the number of unique products per price range bucket (e.g., <₹200,

₹200–₹500, >₹500)?

