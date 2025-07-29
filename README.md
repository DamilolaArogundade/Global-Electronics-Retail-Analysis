# Global-Electronics-Retailer-Analysis
An Excel project analysing six years’ worth of data from a retail company that sells electronic devices from different brands. The dataset includes customer, store, sales, product, and exchange rate tables. It tracks customer info, store locations, order details, product pricing, and currency exchange rates to support detailed business analysis.

**Table of contents**
- [Project Overview](https://github.com/DamilolaArogundade/Global-Electronics-Retail-Analysis/edit/main/README.md#project-overview)
- Project Scope
- Project Objectives
- Expected Outcome
- Document Purpose
- Use Case
- Data Source
- Data Cleaning and Preparation
- Data Analysis and Insight
- Data Visualization
- Recommendations
- Conclusion

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

## Additional Processing Steps

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

