# Global-Electronics-Retailer-Analysis
An Excel project analysing six years’ worth of data from a retail company that sells electronic devices from different brands. The dataset includes customer, store, sales, product, and exchange rate tables. It tracks customer info, store locations, order details, product pricing, and currency exchange rates to support detailed business analysis.

**Table of contents**
- [Project Overview](https://github.com/DamilolaArogundade/Global-Electronics-Retail-Analysis/edit/main/README.md#project-overview)
- [Project Scope](https://github.com/DamilolaArogundade/Global-Electronics-Retail-Analysis?tab=readme-ov-file#project-scope)
- [Project Objectives](https://github.com/DamilolaArogundade/Global-Electronics-Retail-Analysis?tab=readme-ov-file#project-objectives)
- [Expected Outcome](https://github.com/DamilolaArogundade/Global-Electronics-Retail-Analysis?tab=readme-ov-file#expected-outcome)
- [Document Purpose](https://github.com/DamilolaArogundade/Global-Electronics-Retail-Analysis?tab=readme-ov-file#document-purpose)
- [Use Case](https://github.com/DamilolaArogundade/Global-Electronics-Retail-Analysis?tab=readme-ov-file#use-case)
- [Data Source](https://github.com/DamilolaArogundade/Global-Electronics-Retail-Analysis?tab=readme-ov-file#data-source)
- [Data Cleaning and Preparation](https://github.com/DamilolaArogundade/Global-Electronics-Retail-Analysis?tab=readme-ov-file#data-cleaning-and-preparation)
- [Data Analysis and Insight](https://github.com/DamilolaArogundade/Global-Electronics-Retail-Analysis?tab=readme-ov-file#data-analysis-and-insight)
- [Data Visualization](https://github.com/DamilolaArogundade/Global-Electronics-Retail-Analysis?tab=readme-ov-file#data-visualisation)
- [Recommendations](https://github.com/DamilolaArogundade/Global-Electronics-Retail-Analysis?tab=readme-ov-file#recommendations)
- [Conclusion](https://github.com/DamilolaArogundade/Global-Electronics-Retail-Analysis?tab=readme-ov-file#conclusion)

## Project Overview

This project examines historical sales performance across various regions, products, and customer demographics within a global electronics retail company. The analysis leverages transactional sales data, store information, customer profiles, and product catalogues to uncover trends, patterns, and actionable insights. The goal is to support data-driven decision-making that enhances marketing efforts, inventory planning, and customer satisfaction.

## Project Scope

The scope of this analysis includes:

- Sales transactions from 2016 to the first quarter of 2021
- Customer demographic details, including age, gender, location, and country.
- Store attributes such as location, opening date, and size.
- Product data covering brands, categories, pricing, and cost.

## Project Objectives

The primary objectives of this analysis are:

- Identify high-performing products and categories by revenue and sales volume.
  
- Evaluate customer demographics to understand key consumer segments.
- Compare regional sales across different countries and store locations.
- Determine trends over time (seasonal patterns, yearly growth).
- Analyze profit margins and pricing efficiency.
- Recommend strategies to boost sales and improve customer targeting.

## Expected Outcome

- A dashboard showing sales trends and KPIs (e.g., total revenue, average order value, profit).
  
- Clear understanding of top-selling and underperforming products.
- Identification of profitable customer age groups and countries.
- Insights into which store locations are most successful.
- Recommendations for marketing, pricing, and inventory strategies.

## Document Purpose

This document serves as a comprehensive summary of the analysis conducted. It presents key findings in a simple, visual, and readable format for business stakeholders, including management, sales teams, and marketing departments. It bridges the gap between raw data and strategic decisions.

## Use Case

The set of people benefiting from this analysis is sales managers, marketing strategists, operations heads, and executives.

**Use Cases Include:**

- Product planning: Knowing which items to stock more of or discontinue.
  
- Customer targeting: Tailoring campaigns based on demographics.
- Regional expansion: Identifying regions with potential for new stores.
- Performance reviews: Evaluating store and product success over time.
- Revenue optimization: Identifying peak times and leveraging them to increase sales through promotions.

## Data Source

The dataset for this project was sourced from the [Maven Analytics website](https://app.mavenanalytics.io/datasets?search=global+e), designed specifically for practice purposes. It was downloaded in a zip file that contained five tables (Customers, Sales, Stores, Exchange Rate, and Products) comprising 15,267, 62,885, 68, 11,216, and 2,518 rows, respectively, and 10, 9, 5, 3, and 10 columns, respectively. The dataset includes key attributes essential for a comprehensive analysis, such as:

- Order number: Unique ID for each order
  
- Order date: date order was placed
- Customer key: primary key to identify customers
- Store key: primary key to identify stores
- Product key: primary key to identify products
- Quantity: number of items purchased
- Product name: product name
- Product brand: product brand
- Product category: product category name
- Unit cost: cost to produce the product in USD
- Unit price: product list price in USD
- Store country: store country
- Store state: states where the stores are located
- Customer gender: customer gender
- Customer country: countries where customers are located
- Customer birthdate: customer’s date of birth

Each of the variables in these columns contributed crucial insights into our analysis for the global electronics retail company.

## Data Cleaning and Preparation

Clean data is essential for accurate and reliable analysis. It ensures that insights are based on consistent and error-free information, making it easier for analysts and decision-makers to draw meaningful conclusions. I reviewed the dataset for common issues like missing values, duplicates, and formatting inconsistencies. Overall, the data was well-structured and complete, except for the City column, where city names had inconsistent capitalization. I corrected this using the PROPER function to standardize the format and put it in a new column called the *Customer City* column. All other columns had the correct data types, the data values were accurate, and no duplicate records were found.

After this careful review, the data set is well organized and suitable for analysis; this means the insights I will gain from this data set will be accurate, dependable, and useful.

### Additional Processing Steps

**Extraction of columns:** To create a unified data set for comprehensive analysis, various columns were extracted from other tables into the sales table using the VLOOKUP function in Excel. The extracted columns were product name, brand, unit cost, unit price, product category, subcategory, store country, store state, customer name, gender, city, customer country, customer state, and birthdate. This step was crucial to have all the necessary information in one single table, facilitating easier and more efficient analysis.

**Addition of new columns and table:** New columns and a table were added as they were essential to draw insights from the data set. These new columns and tables were:

- **Age category table**: This table was created to group the customers into different age categories to analyze how customers’ demographics affect sales patterns. It was created on the sales table.
  
- **Month**: This column represents the month in which each order was placed, and it was extracted from the order date column using the TEXT function. Having this column will help in analyzing the monthly sales trend.
- **Year**: This column represents the year in which each order was placed, and it was extracted using the YEAR function. This column will help us analyze our sales percentage for each year and year-over-year (YOY) growth.
- **Revenue**: This was calculated by multiplying the unit price by quantity. This column captures the revenue generated by each order.
- **Profit margin**: This was calculated by deducting the unit cost price from the unit price. This column was crucial in determining how much profit was made on each product sold.
- **Profit**: This was calculated by multiplying the profit by the quantity to determine the profit made on each order. This column is important to analyze the total profit made over the years.
- **Age**: This column displays the age of customers who placed an order with the company using the DATEDIF function. This column was crucial in determining the customer’s age groups.
- **Age group**: This column represents the age group each customer falls into, allowing for analysis on how customers’ demographics influence purchasing. This column was created using the VLOOKUP function to extract the categories from the age category table.


## Data Analysis and Insight

The primary aim of this analysis is to derive insight from the global electronics retail sales data by conducting a comprehensive examination of key factors. This in-depth exploration focused on several key goals.
- What types of products does the company sell, and where are the customers located?
  
- Are there any seasonal patterns or trends for order volume or revenue?
- Is there a difference in average order value (AOV) for online sales vs. in-store sales?
- How well are the product categories performing in terms of sales?
- How do customer demographics influence sales patterns and total spending?
- What are the top 5 selling brands and the least 5 selling brands in terms of revenue?
- What is the sales percentage every year?
- How much do stores in each country contribute to total revenue?
- What is the year-over-year (YOY) growth in sales?

The key benefits of this analysis include:
- This analysis helps to identify the top-performing products, brands, and sales channels for better strategic focus
  
- It helps reveal customer demographics and buying patterns to inform promotions and marketing, as well as create a buyer persona.
- It uncovers the seasonal trends and yearly growth, enabling improved forecasting and planning, especially during peak periods.
- It guides pricing, inventory, and promotional decisions based on order values and product category performance.
- It highlights regional and country-level stores' contribution to smarter market expansion.
- It supports data-driven decision-making that boosts revenue, efficiency, and customer satisfaction.

As a result, this analysis provides insights addressing the following questions:


**1. What types of products does the company sell, and where are the customers located?**

The primary objective of this analysis is to determine the types of products this company deals with and sells, as well as to identify the sources of its customers. This information supports better inventory planning and marketing strategies based on customers’ geographic locations.

a.  To answer this question, we need to determine the type of products the company sells first. This was achieved by creating a pivot table. The product category was placed in the row section. This result is presented below in a table.

| Type of products |
|------------------|
| Audio            |
| Cameras and Camcorders|
| Cell phones |
| Computers |
| Games and Toys |
| Home Appliances |
| Music, Movies, and Audio Books |
| TV and Videos |

b.  Where are the customers located? To answer this question, a pivot table was created. The customer country column was placed in the row section, and the customer name was placed in the value section to count the number of customers who came from each country. The results are displayed in the table below.

| Customer's Location | Number of Customers |
|---------------------|---------------------:|
| Australia           |               2,941 |
| Canada              |               5,415 |
| France              |               1,730 |
| Germany             |               5,956 |
| Italy               |               2,685 |
| Netherlands         |               2,250 |
| United Kingdom      |               8,140 |
| United States       |              33,767 |

From the analysis above,

- The types of products the company sells are audio, cameras and camcorders, cellphones, computers, games and toys, home appliances, music, movies and audiobooks, and TV and video.
  
- We can see that customers are located in Australia, Canada, France, Germany, Italy, the Netherlands, the United Kingdom, and the United States. The United States has the highest number of customers at 33,767 customers, while France has the lowest number of customers at 1,730 customers.	

**2. Are there any seasonal patterns or trends for order volume or revenue?**

This question aims to identify periods when sales increase or decrease to forecast demand, plan inventory, optimise marketing efforts, and make better business decisions moving forward.
To answer this question, we are going to look at

a.  **Monthly sales trend**

To achieve this, a pivot table was created. The month column was placed in the row section, and the revenue column was placed in the value section to sum up the revenue made in each month. The results were visualised using the line chart below.

![](https://github.com/DamilolaArogundade/Global-Electronics-Retail-Analysis/blob/main/Monthly%20sales%20trend.png)

From the analysis above

- February has the highest overall revenue of all the years at $7,842,476.2, followed by December and January at $7,496,608.9 and $6,759,981.2, respectively.
  
- April has the lowest revenue inflow over the years at $607,334.0

b.  **Monthly order volume**

This was achieved by creating a pivot table. The month column was placed in the row section, and the quantity column was placed in the value section to count the number of product quantities ordered in each month over the years. The result was visualised using the bar chart below.

![](https://github.com/DamilolaArogundade/Global-Electronics-Retail-Analysis/blob/main/Monthly%20order%20volume.png)

From the analysis above

- December has the highest order volume with 8,655 products ordered, followed by February and January with 8,464 and 7,683 products ordered, respectively. This could be because December is the peak season of winter, and it is a gift-giving season. This extends into January and February since it is still the winter season.

- April has the lowest order volume with 640 products ordered, followed by March with 2,760 products. This could be because people are already back to budgeting and are taking finances more seriously. Some may be saving up for summer and would like to cut back on unnecessary expenses.

**3. Is there a difference in average order value (AOV) for online sales vs. in-store sales?**
   
This analysis aims to identify the channel that generates the most revenue, whether online or in-store. This will guide stakeholders on investment in online or physical stores.

To calculate the AOV for the online store, a pivot table was created, with quantity and revenue placed in the value section. The filter section was then used to filter only the online stores by specifying the store country. The purpose of this is to display the total orders and total revenue generated from the online store, allowing for the calculation of the average order value (AOV), which is calculated as total revenue divided by total orders.

| Total Orders | Total Revenue | AOV Online |
|-------------:|--------------:|-----------:|
|      41,311  |   11,404,325  |     276.1  |

To calculate the AOV for the physical stores, a pivot table was created, with quantity and revenue placed in the value section. The filter section was then used to filter only the physical stores by specifying the store countries. The purpose of this is to display the total orders and total revenue generated from the physical stores, allowing for the calculation of the average order value (AOV), which is calculated as total revenue divided by total orders.

| Total Orders | Total Revenue | AOV in-store sales |
|-------------:|--------------:|-----------:|
|       156,446  |   44,351,155  |     283.5  |

From the analysis above, AOV online sales is 276.1, while AOV in-store sales is 283.5. To answer the question, there is a 7.4 difference in AOV between online sales and in-store sales, with in-store sales having the higher AOV. This could be because the company has a large number of stores in various countries, which allows for increased customer inflows.

**4. Sales performance by product category**
   
This analysis aims to assess the performance of various product categories in terms of sales. This helps to improve merchandising and product development. This analysis will be answered in two parts.

**a.  Total revenue generated by each product category**

To achieve this, a pivot table was created, with the product category placed in the rows section and the revenue placed in the values section, allowing for the calculation of total revenue generated by each product category over the years. The results were visualised using a bar chart below.

![](https://github.com/DamilolaArogundade/Global-Electronics-Retail-Analysis/blob/main/Total%20Revenue%20by%20Product%20category.png)

From the analysis above

- Computers generated the most revenue at $19,301,595.50, followed by home appliances at $10,795,478.60. This could be because computers and home appliances are typically priced on the high side. So they make more money than other electronics.

- Games and toys generated the least revenue over the years at $724,829.40, followed by music, movies, and audiobooks at $3,131,006.40. This could be because these products cost less, so they do not generate high revenue.

b.  Total quantity ordered by each product category

To achieve this, a pivot table was created, with the product category placed in the row section and quantity placed in the values section, allowing for the calculation of the total number of each product category sold. This analysis was visualised using a bar chart, as seen below.

![](https://github.com/DamilolaArogundade/Global-Electronics-Retail-Analysis/blob/main/Total%20quantity%20per%20product%20category.png)

From this analysis

- Computers had the highest quantity sold at 44,151, followed by cellphones at 17,609. These could be because technology is rapidly replacing many things, and people need computers and cellphones more these days.

- TV and video were ordered the least at 11,236 orders, followed by cameras and camcorders at 17,609 orders. 


**5. How do customer demographics influence sales patterns and total spending?**
   
This question aims to understand how customers’ demographics (gender, age, location, income level, etc.) affect their spending habits, specifically what they buy, how they make purchases, and how much they spend. This helps to create a buyer persona and also tailor marketing strategies for different demographic groups. This question will be analysed in 3 different parts.

a. Total revenue generated based on Gender

To achieve this, a pivot table was created, with the customer gender column placed in the row section and the revenue column placed in the value section to calculate the total revenue generated from both genders. The results were then formatted as a percentage to show the contribution of each gender to the total revenue. The result was visualised using a pie chart, as seen below

![](https://github.com/DamilolaArogundade/Global-Electronics-Retail-Analysis/blob/main/Total%20revenue%20per%20gender.png)

The analysis above shows that the male gender contributed more to the total revenue at 50.82%; i.e., they spent more at the store than the female gender, who contributed 49.18% to the total revenue over the years.

b.  Total revenue by age groups

To achieve this, a pivot table was created, with the age group column placed in the row section and the revenue column placed in the value section to calculate the revenue generated by each age group over the years. The results were then formatted as a percentage to show the contribution made by each age group. This was visualised using a pie chart, as seen below

![](https://github.com/DamilolaArogundade/Global-Electronics-Retail-Analysis/blob/main/Total%20Revenue%20Per%20Age%20group.png)

From the analysis above

- The seniors contributed the highest to the total revenue at 45%. This could be because they spend money buying gifts and electronics for their grandchildren. It is well known that seniors have a lot of money and spend it generously on their grandchildren.

- Although young adults and middle-aged people make up the bulk of the customers, their contribution to the total revenue is low compared to that of the seniors—young adults at 25.55% and middle-aged at 29.45%. Middle-aged people tend to have more because they have disposable income to make purchases.

c.  Total revenue based on customers’ location (countries)

To achieve this, a pivot table was created. The customer country column was placed in the row section, and the revenue column was placed in the value section to calculate the revenue contributed by customers from each country to the total revenue. The results were visualised using a bar chart, as shown below.

![](https://github.com/DamilolaArogundade/Global-Electronics-Retail-Analysis/blob/main/Revenue%20per%20customer%20countries.png)

From the analysis above

- Customers from the United States contributed the most to the total revenue at $29,871,631.2, followed by the United Kingdom and Germany at $7,084,088.1 and $5,414,149.8, respectively.
  
- Customers from France contributed the least to the total revenue at $1,515,338.2, followed by the Netherlands at $1,962,154.3

**6. What are the top 5 selling brands and the least 5 selling brands in terms of revenue generated**
   
This analysis aims to determine which brands are generating significant revenue, and to identify the brands that customers are not really purchasing. The benefit of this analysis is to understand the key revenue drivers. It will also help to inform discontinuation or promotion strategies.

a. Top 5 selling brands

To identify the top-selling brands, a pivot table was created. The product brands column was placed in the row section, and the revenue column was placed in the value section to calculate the revenue generated by each brand. A filter pane was employed to showcase the top 5 best-selling brands exclusively. The results were visualised in the bar chart below.

![](https://github.com/DamilolaArogundade/Global-Electronics-Retail-Analysis/blob/main/Top%205%20selling%20brands.png)

From the analysis above,

- WWI Desktop PC2.33 X233O Black was the top revenue generator at $505,450
  
- Adventure Works Desktop PC2.33 XD233 Black, Adventure Works Desktop PC2.33 XD233 Brown, Adventure Works Desktop PC2.33 XD233 Silver, and Adventure Works Desktop PC2.33 XD233 White—while not the top revenue contributors, these brands are still very popular among customers.

b. The least 5 selling brands 

To identify the least-selling brands, a pivot table was created. The product brands column was placed in the row section, and the revenue column was placed in the value section to calculate the revenue generated by each brand. A filter pane was employed to showcase the least 5 selling brands exclusively. The results were visualised in the bar chart below.

![](https://github.com/DamilolaArogundade/Global-Electronics-Retail-Analysis/blob/main/Least%205%20selling%20brands.png)

From the analysis above

- The brand that generated the lowest revenue at $15.20 is SV USB Data Cable E600 Silver. This product was purchased the least by the customers.
  
- Litware 80mm Dual Ball Bearing Case Fan E1001 Green, SV USB Data Cable E600 Grey, SV USB Data Cable E600 Pink, and SV USB Sync Charge Cable E700 Silver also generated low revenue at $19.96, $21.85, $25.65, and $15.92, respectively.

**7. Sales percentage per year**
   
This analysis examines the yearly contribution to total revenue to identify the year with the highest and lowest sales. By comparing annual performance, stakeholders can gain insights into what worked well and what underperformed each year and use this information to make informed decisions and apply effective strategies to boost future sales.

To achieve this, a pivot table was created, with the Year column added to the row section and the revenue column added to the values section to calculate the total revenue generated per year. The results were then formatted as a percentage to show the contribution each year made. The results were visualised using a donut chart below

![](https://github.com/DamilolaArogundade/Global-Electronics-Retail-Analysis/blob/main/Sales%20percentage%20per%20year.png)

The analysis above shows that

- 2019 contributed the most to the total revenue at 32.76%, followed by 2018 at 22.94%.
  
- 2021 contributed the least to the total revenue at 1.86%, likely due to the limited availability of data that year, which only spanned two months. Excluding 2021 because of incomplete data, 2016 becomes the lowest contributing year, accounting for 12.46% of total revenue.
  
**8. What is the year-over-year (YOY) growth in sales?**
   
This analysis tracks year-over-year changes in sales to determine whether the company’s performance is improving or declining annually. The insights gained will help stakeholders identify the factors that may have caused dips in sales and guide future strategies to optimise performance and minimise losses, even during unexpected circumstances. The results are shown in the table below.

| Year | Total Revenue     | %YOY     |
|------|-------------------|----------|
| 2016 | $6,946,793.56     | 0.00%    |
| 2017 | $7,421,422.27     | 6.83%    |
| 2018 | $12,788,960.66    | 72.32%   |
| 2019 | $18,264,382.48    | 42.81%   |
| 2020 | $9,294,632.14     | -49.11%  |
| 2021 | $1,039,288.48     | -88.82%  |

The analysis indicates a steady increase in sales up to 2019, with a significant jump from 6.83% in 2016 to 72.43% in 2019. Although 2019 saw a 42.81% increase compared to the previous year, the growth rate was smaller than the one recorded the year before. In 2020, sales declined sharply by -49.11%, reflecting nearly half the revenue of 2019. This drop was likely due to the global impact of COVID-19, which disrupted in-store purchases and overall consumer spending. The growth rate for 2021 is not considered in this analysis because data for that year are incomplete.

**9. Total revenue generated from each store, categorized by country**

This analysis aims to measure revenue generated from each sales channel offered by the company. It helps highlight the strengths and weaknesses of different regional markets, providing valuable insights to guide stakeholder decisions on whether to scale operations up or down in specific areas.

To achieve this, a pivot table was created, with the store country column placed in the row section and the revenue column placed in the value section to calculate the revenue generated from each sales channel. The results were visualised using a bar chart, as seen below.

![](https://github.com/DamilolaArogundade/Global-Electronics-Retail-Analysis/blob/main/Revenue%20generated%20from%20stores%20categorized%20by%20country.png)

From the analysis above

- Stores in the United States generated the highest revenue at $23,764,425.86, followed by the online sales channel with $11,404,324.63. This may be attributed to higher consumer spending habits in the U.S. and the convenience that online shopping offers to customers.
  
- The stores in France generated the least revenue at $1,229,545.95, followed by the Netherlands at $1,591,344.48.

## Data visualisation

![](https://github.com/DamilolaArogundade/Global-Electronics-Retail-Analysis/blob/main/Dashboard%201.png)
![](https://github.com/DamilolaArogundade/Global-Electronics-Retail-Analysis/blob/main/Dashboard%202.png)

## Recommendations

Based on the analysis above, here are a few recommendations for the global electronics retail company

- Take advantage of peak seasons like December to February by running gift promotions, holiday bundles, and targeted marketing. During slower months (March to May), use discounts or flash sales to keep sales steady.
  
- Plan staffing, stock, and promotions around busy and slow periods to avoid shortages or excess.
- To improve online sales, offer free shipping or discounts on larger orders to increase average order value (AOV).
- Keep investing in high-performing products like computers and home appliances (they bring in the most money), and make sure to stock up on high-demand items like cell phones. For products that don’t sell well, like games and toys, try targeting them to niche audiences who might still be interested.
- Target senior customers more with marketing that speaks to gift-giving, grandchildren, and ease of use, especially during the holidays, since they spend the most.
- Promote top-selling brands more through ads and online features. Consider dropping or discounting low-performing brands to make space for better ones.
- Look back at what worked in 2018–2019 (the best growth years) and try to repeat successful strategies. Don’t rely too much on physical stores—things like COVID showed how important it is to have strong online options too.
- Review low-performing stores in countries like France and the Netherlands. If they keep underperforming, consider closing them and focusing on expanding online sales in those regions to cut costs and reach more people.

## Conclusion

This project has successfully uncovered key drivers of sales performance across products, customers, and regions. By understanding who buys what, where, and when, the company can make more informed decisions that improve profitability and customer satisfaction. Continued analysis over time will help track the impact of changes and refine business strategies further.



Thank you for viewing this project. I completed this project to showcase my data analysis skills using a data set from a fictitious company from Mavin Analystics. I am actively seeking data analyst roles and am open to new opportunities. If you are interested in discussing or have any feedback, I would love to hear from you.

### Contact me

**Email:** Raimotarogundade@gmail.com

**LinkedIn:** 
