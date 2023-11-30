# Maven Toys🧸 - Sales performance analysis

_Welcome to Maven Toys - Where Play Sparks Ingenuity⚡!_

<p align="center">
    <img width="500" src="https://github.com/HannahIgboke/Maven-Toys---Sales-performance-analysis./blob/main/Images/Maven_Toys.png" alt="customer_orders">
</p>

# Table of contents

- [About the company](https://github.com/HannahIgboke/Maven-Toys---Sales-performance-analysis./tree/main#about-thecompany)
- [Project brief](https://github.com/HannahIgboke/Maven-Toys---Sales-performance-analysis./tree/main#project-brief)
- [Business objectives](https://github.com/HannahIgboke/Maven-Toys---Sales-performance-analysis./tree/main#business-objectives)
- [Deliverable](https://github.com/HannahIgboke/Maven-Toys---Sales-performance-analysis./tree/main#deliverable)
- [About the dataset](https://github.com/HannahIgboke/Maven-Toys---Sales-performance-analysis./tree/main#about-thedataset)
- [Skills demonstrated](https://github.com/HannahIgboke/Maven-Toys---Sales-performance-analysis./tree/main#skills-demonstrated)
- [The analysis process](https://github.com/HannahIgboke/Maven-Toys---Sales-performance-analysis./tree/main#the-analysisprocess)
  - [Data importation](https://github.com/HannahIgboke/Maven-Toys---Sales-performance-analysis./tree/main#data-importation)
  - [Data profiling and cleaning](https://github.com/HannahIgboke/Maven-Toys---Sales-performance-analysis./tree/main#data-profiling-andcleaning)
  - [Data modeling](https://github.com/HannahIgboke/Maven-Toys---Sales-performance-analysis./tree/main#data-modeling)
  - [Data analysis - insights and recommendations](https://github.com/HannahIgboke/Maven-Toys---Sales-performance-analysis./tree/main#data-analysis---insights-and-recommendations)
  - [Data visualization - Power BI report](https://github.com/HannahIgboke/Maven-Toys---Sales-performance-analysis./tree/main#data-visualization---power-bi-report)
- [Next steps and other recommendations](https://github.com/HannahIgboke/Maven-Toys---Sales-performance-analysis./tree/main#next-steps-and-other-recommendations)
 

---------------------------------------------------------------------------------------------------------------------------------------------------------

## About the company 🏢

Maven Toys is a fun and creative toy company that goes beyond regular play. They believe in making toys that not only entertain but also inspire imagination. As a top player in the toy industry, their goal is to create special moments for kids. Now, they're using data analysis to bring even more joy to families.

---------------------------------------------------------------------------------------------------------------------------------------------------------


## Project brief📝


In this project, I will be assuming the role of a BI consultant who has just been hired by this fictional company - Maven Toys. As they look to **expand their business with new stores**, they've brought me in to analyze interesting patterns and trends in their data and help them make informed decisions.

--------------------------------------------------------------------------------------------------------------------------------------------------------- 

## Business objectives ✍

Maven Toys major objective is to expand their business with new stores. Based on historical data from January 2017 to September 2018, they have posed the following business questions to help them make a decision:

1. What is our Year-over-year (YOY) revenue and profit growth? How did we perform in the previous year?
2. Maven Toys has set a target of $8.5 million in revenue for each year - 2017 and 2018. How much progress did we or have we made towards this goal?
3. Which product categories drive the biggest profits? Is this the same across store locations?
4. Can you find any seasonal trends or patterns in the sales data?
5. What is our market penetration? That is, how many stores and cities are we currently in?
6. Is there a relationship between the number of stores in a city and the revenue generated there?
7. How would you categorize our product pricing? What is the effect of this product pricing on the revenue generated each year?
8. What are our best and worst performing stores in terms of profit and revenue.
9. How would you advice Maven Toys to proceed with their expansion based on the insights you've garnered?

---------------------------------------------------------------------------------------------------------------------------------------------------------

## Deliverable 🚚

A dashboard or report containing analysis and actionable insights.

---------------------------------------------------------------------------------------------------------------------------------------------------------

## About the dataset 

The dataset provided contains 4 tables in CSV format:

- The Products table contains the 35 products sold at Maven Toys (each record represents one product), with fields containing details about the product category, cost, and retail price.
- The Stores table contains the 50 Maven Toys store locations (each record represents one store), with fields containing details about the store location, type, and date it opened.
- The sales table contains the units sold in over 800,000 sales transactions from January 2017 to September 2018 (each record represents the purchase of a specific product at a specific store on a specific date).
- The inventory table contains over 1,500 records that represent the stock on hand of each product in each store at the current point in time (Oct. 1, 2018).

---------------------------------------------------------------------------------------------------------------------------------------------------------

## Skills demonstrated

Tool used: Microsoft Power BI. the following skills an concepts were aapplied through out this project:
- Data cleaning and transformation in Power Query
- Data modeling
- Data Analysis Expressions (DAX) codes
- Data visualization
- Project documentation

---------------------------------------------------------------------------------------------------------------------------------------------------------


## The analysis process

This is an iterative roadmap undertaken to ensure the accuracy of results and a comprehensive analysis. For this project, I am using Microsoft Power BI.

### Data importation

I imported all the CSV files provided into my Power BI workspace, after which I opened them individually in Power Query to carry out data cleaning.


### Data profiling and cleaning 🧹

Data profiling is crucial as it provides a comprehensive understanding of the quality, structure, and relationships within a dataset, ensuring that potential issues are identified early on. Cleaning the data is equally vital to enhance accuracy, eliminate inconsistencies, and maintain the integrity of the information, ensuring reliable insights and informed decision-making.

In power query, I carried out the following tasks:

- Promoting headers to ensure appropriate column names.
- I converted the data types of the id columns in each table from whole numbers to text since they are identifiers and would not be used for calculations.
- I added three new columns, total product cost, total product price, and profit, to the sales dataset.
- I double-checked the column data types and converted the wrong data types to the appropriate data types.
- I trimmed the names of the stores in the stores table to reduce redundancy and create explicit and easy-to-read store names.

Furthermore, I created a Dates table that would serve as my primary date table for this analysis. I did this using the CALENDARAUTO() function, which creates a Date table by assessing the earliest and latest date in all of my tables. From this date table, I extracted the year, quarter, month, and day.

### Data modeling

Data modeling is crucial in Power BI analysis because it structures and organizes raw data into a coherent framework, enabling relationships and hierarchies that form the foundation for insightful visualizations. For this analysis, Power BI automatically connected related tables, resulting in a star schema model.

<p align="center">
    <img width="1000" src="https://github.com/HannahIgboke/Maven-Toys---Sales-performance-analysis./blob/main/Images/Data_model.PNG" alt="Star schema model">
</p>


A star schema model is a type of dimensional model in which data is organized into a central fact table (in this case, the sales table) surrounded by a number of dimensional tables (the other tables).


### Data analysis - insights and recommendations

To propagate my analysis I created several measures and new columns to aid the process.

---------------------------------------------------------------------------------------------------------------------------------------------------------

**1. What is our Year-over-year (YOY) revenue and profit growth? How did we perform in the previous year?**

A YOY comparison is an effective way to evaluate the financial performance of Maven Toys by comparing the revenue and profit for the same period in the current year with the same period in the previous year. The time period compared here is January to September for both years.

<p align="center">
    <img width="700" src="https://github.com/HannahIgboke/Maven-Toys---Sales-performance-analysis./blob/main/Images/YOY_growth.PNG" alt="YOY growth">
</p>


In 2018, over that time period, Maven Toys made $6.96 million. The same period in 2017 generated $5.32 million in revenue. This results in 30.9% year-over-year growth. In 2018, profit totaled $1.82 million; the same period last year came off at $1.57 million. This implied a 16% year-over-year growth in profit. Cumulatively, from January 2017 until September 2018, Maven Toys generated $14.44 million in revenue and made a total of $3.39 million in profit.

---------------------------------------------------------------------------------------------------------------------------------------------------------

**2. Maven Toys has set a target of $8.5 million in revenue for each year - 2017 and 2018. How much progress did we or have we made towards this goal?**

<p align="center">
    <img width="700" src="https://github.com/HannahIgboke/Maven-Toys---Sales-performance-analysis./blob/main/Images/Revenue_progress_towards_target.PNG" alt="Revenue progress towards target">
</p>


By December 2017, Maven Toys was 88.03% (i.e., approximately $7.48 million) into the goal. In 2018, by September 30th, Maven Toys was 81.9% into the goal (approximately $6.96 million).
When compared to the same period last year, I found out that by September 30, 2017, Maven toys were only 62.59% (approximately $5.32 million) into their target.

This is a positive growth rate, and with the expected increase in sales by the remaining part of the year (October to December - the holiday and festive season), Maven Toys would hit its target.

---------------------------------------------------------------------------------------------------------------------------------------------------------

**3. Which product categories drive the biggest profits? Is this the same across store locations?**

The arts & crafts and the toys product categories drove the most sales.


<p align="center">
    <img width="700" src="https://github.com/HannahIgboke/Maven-Toys---Sales-performance-analysis./blob/main/Images/Profit_by_product_category.PNG" alt="Profit generated by product category">
</p>


YTD, across store locations, I observed that in downtown and residential location stores, the arts & crafts product categories drove the most profits, while in commercial and airport location stores, the toys category pushed the arts & crafts category off the table slightly and drove more profit.

---------------------------------------------------------------------------------------------------------------------------------------------------------

**4. Can you find any seasonal trends or patterns in the sales data?**

<p align="center">
    <img width="700" src="https://github.com/HannahIgboke/Maven-Toys---Sales-performance-analysis./blob/main/Images/Monthly_revenue_trend.PNG" alt="Monthly revenue trend">
</p>


The following trends and patterns were observed:
- The month of December generated the most revenue. The month being a festive season brings with it lots of occasions and celebrations, including Christmas and Boxing Day, among others.
- There was a noticeable dip in the month of August for both years. This can be attributed to the season when parents are more focused on back-to-school supplies and preparations for their kids. This month, parents prioritize purchasing school supplies, clothing, and other essentials over toys during this period.
- For both years, January was off to a slow start, though not as low as that of August. This can be attributed to post-holiday lulls and budget constraints as consumers become more budget conscious and recover from holiday expenses, thereby leading to reduced spending on non-essential items, in this case toys.
- Between April and June, there is an almost steady revenue generation rate. This is so because these months coincide with spring and early summer in many regions. During this time, people often engage in outdoor activities, leading to an increased demand for outdoor toys and recreational products. Also, many schools have spring breaks during these months, leading to increased family activities and potential purchases of toys for entertainment during the break.
- I also observed that in 2017, after the August dip, sales steadily began climbing in the ember month until the end of the year.

**_Recommendations_**

Based on the patterns observed above, I would recommend the following to the Maven Toys management team:

- An expansion into educational toy categories, for example - jigsaw puzzles, building blocks, STEM kits, coding toys, etc. This would encourage parents to invest in these toy categories to help their kids development, especially during the school year.
- Collection of data on consumers in order to analyze customer spending habits and consumer behavior, customer lifetime value (CLV), churn and retention rate
- A feedback form should be sent regularly on a month-by-month basis to keep track of customers preferences as the months pass by.

---------------------------------------------------------------------------------------------------------------------------------------------------------

**5. What is our market penetration? That is, how many stores and cities are we currently in?**

2017 till date Maven Toys has a total of 50 stores spread across 29 cities.

<p align="center">
    <img width="700" src="https://github.com/HannahIgboke/Maven-Toys---Sales-performance-analysis./blob/main/Images/Market_penetration.PNG" alt="Market penetration">
</p>


58% of stores are located in downtown areas, 24% in commercial areas, 12% in residential areas, and 6% around airports.


<p align="center">
    <img width="700" src="https://github.com/HannahIgboke/Maven-Toys---Sales-performance-analysis./blob/main/Images/Stores_per_location.PNG" alt="Stores per location">
</p>

---------------------------------------------------------------------------------------------------------------------------------------------------------

**6. Is there a relationship between the number of stores in a city and the revenue generated there.**


Yes there is. There is a strong positive correlation between the number of stores in a city and the revenue generated in that city. This means that as the number of stores in a city increases, the amount of revenue generated increases as well. It is important to note that there may be a hidden variable that can affect the amount of sales generated in the stores in each city.


<p align="center">
    <img width="700" src="https://github.com/HannahIgboke/Maven-Toys---Sales-performance-analysis./blob/main/Images/Relationship.PNG" alt="Relationship between number of stores in a city with revenue generated">
</p>



**_Recommendations_** 

While the strong positive correlation between the number of stores in a city and the revenue generated is a valuable insight, it's prudent to consider potential confounding factors that might influence this relationship. I recommend that the following factors be considered and analyzed:

- Population Density: Cities with a higher population density may naturally support more stores and higher sales due to a larger customer base.
- Economic Factors: The economic health of a city, including factors like income levels, employment rates, and overall economic stability, can significantly impact consumer spending. Wealthier cities might have higher sales potential.
- Competition: A city with a high concentration of toy stores may experience saturation, affecting the revenue generated by each individual store.
- Local Trends and Preferences: Consumer preferences and cultural trends can vary by region. Adapting product offerings to align with local preferences is crucial for success. Consider factors such as popular toy trends and cultural influences.
- Location of Stores Within Cities: The specific location of each store within a city (e.g., proximity to popular attractions, accessibility, foot traffic) can significantly influence its individual performance.
- Operational Efficiency:Assess the operational efficiency of each store. Factors such as inventory management, staff training, and store layout can influence the customer experience and, consequently, sales.

---------------------------------------------------------------------------------------------------------------------------------------------------------

**7. How would you categorize our product pricing? What is the effect of this product pricing on the revenue generated year to date?**

To do this, I categorized the product prices into three groups: low (≤$10), medium (> $10 to ≤ $20), and high (> $20). The DAX code for this is seen below.


<p align="center">
    <img width="700" src="https://github.com/HannahIgboke/Maven-Toys---Sales-performance-analysis./blob/main/Images/DAX_code.PNG" alt="DAX code">
</p>


YTD, Maven Toys has generated $14.44 million in revenue. 24.6% ($3.55 million) of this was generated by high-priced products, 18.5% ($2.67 million) by low-priced products, and 56.9% ($8.22 million) by medium-priced products.

---------------------------------------------------------------------------------------------------------------------------------------------------------

**8. What are our best and worst performing stores in terms of profit and revenue.**

The image below shows the top and bottom 5 stores in terms of revenue as well as the most and worst profitable stores. 

<p align="center">
    <img width="700" src="https://github.com/HannahIgboke/Maven-Toys---Sales-performance-analysis./blob/main/Images/Store_analysis.PNG" alt="Best and worst performing stores by revenue and profit">
</p>


On further analysis (you can interact with the report [here](https://app.powerbi.com/groups/me/reports/2e17172d-e27b-4066-81fa-dbe9094798c9/ReportSection9ff2d1c5d60c7b204339?experience=power-bi)) I discovered that most of the stores that drove the most revenue and profit were located in cities that had 3 to 4 stores. The bottom and worst performing stores in revenue and profit were located in cities with one or two stores.

---------------------------------------------------------------------------------------------------------------------------------------------------------

**9. How would you advice Maven Toys to proceed with their expansion based on the insights you've garnered?**

Based on the insights gathered from my analysis, Maven Toys can approach the topic of expansion based on store locations. Recall that we have 4 store locations - Downtown, Residential, Commercial, and Airport. Below is a breakdown of how each area type can impact sales along with recommendations for the expansion strategy:


#### DOWNTOWN AREAS: stores located in the central business districts of cities.

Sales Impact: Since Downtown areas often have high foot traffic, this makes them ideal for impulse purchases and for attracting a diverse customer base. 

Recommendation: Maven Toys should consider expanding further in downtown areas, especially in cities with strong economic activity and high population density. There should be a focus on storefront visibility and unique promotions to capture the attention of passersby.

#### COMMERCIAL AREAS: stores near shopping centers and business parks.

Sales Impact: Commercial areas attract a mix of professionals and families. The proximity to business hubs could result in increased weekday sales, while weekends might see family-oriented shoppers.

Recommendation: Maven Toys needs to further evaluate the performance of existing stores in commercial areas and, if successful, consider expanding strategically in similar locations and exploring partnerships with nearby businesses for cross-promotions.

#### RESIDENTIAL AREAS: stores located in or near residential neighborhoods.

Sales Impact: Residential areas cater to local residents, offering a more community-focused shopping experience. Sales might be influenced by the demographics of the neighborhood, including the age group of families with children.

Recommendation: Assess the demographic profile of successful residential stores and identify neighborhoods with similar characteristics for expansion.

#### AIRPORT AREAS: stores situated in proximity to airports.

Sales Impact: these areas attract a mix of local and international customers. Travelers, especially families with children, usually seek entertainment options or souvenirs.

Recommendation: Assess the performance of airport stores and consider expansion in cities with high air traffic. Maven Toys should tailor product offerings to cater to travelers and explore partnerships with airport authorities for promotional opportunities.

---------------------------------------------------------------------------------------------------------------------------------------------------------

### Data visualization - Power BI report
For further analysis and exploration to address any questions that could arise I have created a 3 page interactive report published [here](https://app.powerbi.com/groups/me/reports/2e17172d-e27b-4066-81fa-dbe9094798c9/ReportSection9ff2d1c5d60c7b204339?experience=power-bi). 


<p align="center">
    <img width="700" src="https://github.com/HannahIgboke/Maven-Toys---Sales-performance-analysis./blob/main/Images/Sales_Performance_report.PNG" alt="Sales_Performance_report">
</p>


<p align="center">
    <img width="700" src="https://github.com/HannahIgboke/Maven-Toys---Sales-performance-analysis./blob/main/Images/Sales_Performance_by_products.PNG" alt="Sales_Performance_by_products">
</p>


<p align="center">
    <img width="700" src="https://github.com/HannahIgboke/Maven-Toys---Sales-performance-analysis./blob/main/Images/Sales_Performance_by_stores.PNG" alt="Sales_Performance_by_stores">
</p>

---------------------------------------------------------------------------------------------------------------------------------------------------------

## Next steps and other recommendations

- Marketing and Promotion Efforts: Variances in marketing strategies and promotional efforts among different cities can affect sales. Further analyses on the effectiveness of marketing campaigns and how they contribute to revenue generation should be made
- Conduct a pilot testing experiment to assess the effectiveness of customers placing orders on the Maven Toys website, considering factors such as the cost of product shipments, packaging, and related expenses.


------------------------------------------------------------------------------------------------------------------------------------------------------------------

![Thank you](https://github.com/HannahIgboke/Maven-Toys---Sales-performance-analysis./assets/116895464/3c988713-4ad4-47f5-827c-4c0aecbffc27)


That was a long one, but I'm glad you stuck to the end😊. Feel free to star this repository so you can always come back to it.

