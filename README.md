# Maven Toys🧸 - Sales performance analysis

_Welcome to Maven Toys - Where Play Sparks Ingenuity!_

<p align="center">
    <img width="500" src="https://github.com/HannahIgboke/Maven-Toys---Sales-performance-analysis./blob/main/Images/Maven_Toys.png" alt="customer_orders">
</p>

# Table of contents

- About the company
- Project brief
- Business objectives
- Deliverables
- About the dataset
- Skills demonstrated
- The analysis process
  - Data importation
  - Data profiling and cleaning





## About the company

Maven Toys (a fictional company) is a dynamic and forward-thinking toy company that transcends the boundaries of traditional play. Maven Toys believes in the power of play to not only entertain but to ignite ingenuity and spark creativity. As a leading force in the toy industry, they are on a mission to create joyous moments that go beyond the ordinary.

Their commitment to excellence extends from the imaginative products that define their brand to the meticulous analysis of data driving their strategic expansion. Maven Toys is not just a company; it’s a celebration of the boundless potential of play, where each moment becomes a canvas for imagination, and each toy is a key to unlocking new realms of creativity.


## Project brief

At Maven Toys, we understand that every child’s smile is a testament to the joy encapsulated within our products. Now, with a strategic vision to extend this joy to even more families, we have therefore initiated a comprehensive data-driven analysis.

In this project, I will be assuming the role of a BI consultant who has just been hired by Maven Toys. As they look to expand their business with new stores, they’ve brought me in to analyze interesting patterns and trends in their data and help them make informed decisions.

## Business objectives

Maven Toys major objective is to expand their business with new stores. Based on historical data from January 2017 to September 2018, they have posed the following business questions to help them make a decision:

1. Maven Toys has set a target of $8.5 million in revenue for each year—2017 and 2018. How much progress did we or have we made towards this goal?
2. What is our year-over-year (YOY) revenue and profit growth? How did we perform in the previous year?
3. Which product categories drive the biggest profits? Is this the same across store locations?
4. Can you find any seasonal trends or patterns in the sales data?
5. What is our market penetration? That is, how many stores and cities are we currently in?
6. Is there a relationship between the number of stores in a city and the revenue generated there?
7. How would you categorize our product pricing? What is the effect of this product pricing on the revenue generated each year?
8. What is your recommended expansion plan? How would you advise Maven Toys to proceed with their expansion based on the insights you’ve garnered?


## Deliverables

A dashboard or report containing analysis and actionable insights

## About the dataset

The dataset provided contains 4 tables in CSV format:

- The Products table contains the 35 products sold at Maven Toys (each record represents one product), with fields containing details about the product category, cost, and retail price.
- The Stores table contains the 50 Maven Toys store locations (each record represents one store), with fields containing details about the store location, type, and date it opened.
- The sales table contains the units sold in over 800,000 sales transactions from January 2017 to September 2018 (each record represents the purchase of a specific product at a specific store on a specific date).
- The inventory table contains over 1,500 records that represent the stock on hand of each product in each store at the current point in time (Oct. 1, 2018).

## Skills demonstrated

Tool used: Power BI

- Data cleaning using Power Query
- Data modelling
- DAX calculations and expressions
- Data visualization


## The analysis process

This is an iterative roadmap undertaken to ensure the accuracy of results and a comprehensive analysis. For this project, I am using Microsoft Power BI.

### Data importation

I imported all the CSV files provided into my Power BI workspace, after which I opened them individually in Power Query to carry out data cleaning.

### Data profiling and cleaning

Data profiling is crucial as it provides a comprehensive understanding of the quality, structure, and relationships within a dataset, ensuring that potential issues are identified early on. Cleaning the data is equally vital to enhance accuracy, eliminate inconsistencies, and maintain the integrity of the information, ensuring reliable insights and informed decision-making.

In power query, I carried out the following tasks:

- Promoting headers to ensure appropriate column names
- I converted the data types of the id columns in each table from whole numbers to text since they are identifiers and would not be used for calculations.
- I added three new columns, total product cost, total product price, and profit, to the sales dataset.
- I double-checked the column data types and converted the wrong data types to the appropriate data types.
- I trimmed the names of the stores in the stores dataset to reduce redundancy and create explicit and easy-to-read store names.

Furthermore, I created a Dates table that would serve as my primary date table for this analysis. I did this using the CALENDARAUTO() function, which creates a Date table by assessing the earliest and latest date in all of my tables. From this date table, I extracted the year, quarter, month, and day.

### Data modeling

Data modeling is crucial in Power BI analysis because it structures and organizes raw data into a coherent framework, enabling relationships and hierarchies that form the foundation for insightful visualizations. For this analysis, Power BI automatically connected related tables, resulting in a star schema model.

<p align="center">
    <img width="1000" src="https://github.com/HannahIgboke/Maven-Toys---Sales-performance-analysis./blob/main/Images/Data_model.PNG" alt="customer_orders">
</p>

A star schema model is a type of dimensional model in which data is organized into a central fact table (in this case, the sales table) surrounded by a number of dimensional tables (the other tables).







