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
- [Data Visualization]()
- [Recommendations]()
- [Conclusion]()

## Project Overview

This project explores historical sales performance across different regions, products, and customer demographics in a global electronics retail company. The analysis leverages transactional sales data, store information, customer profiles, and product catalogues to uncover trends, patterns, and actionable insights. The goal is to support data-driven decision-making that enhances marketing efforts, inventory planning, and customer satisfaction.

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

**Extraction of columns:** To create a unified data set for comprehensive analysis, various columns were extracted from other tables into the sales table using the VLOOKUP function in Excel. The extracted columns were product name, brand, unit cost, unit price, product category, subcategory, store country, store state, customer name, gender, city, customer country, customer state, and birthdate. This step was important to have all the necessary information in one single table for an easier and more efficient analysis.

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


