# Superstore Sales Analysis and Forecasting


## Introduction

The Superstore Sales and Forecasting project aims to analyze historical sales data from a superstore and develop a predictive model to forecast future sales. Leveraging Power BI, DAX, Power Query, and advanced analytical techniques, this project provides insights into sales trends, consumer preferences, geographic patterns, and more. By integrating a dashboard and forecasting capabilities, stakeholders can make informed decisions to optimize inventory, marketing strategies, and overall business operations.

## Problem Statement

The superstore management seeks to understand sales patterns, identify key contributors to revenue, and predict future sales to enhance operational efficiency. The challenges include:

1. Analyzing historical sales data to uncover trends, peaks, and patterns.
2. Identifying top-performing products, categories, and regions.
3. Understanding consumer preferences in terms of payment, shipping, and product categories.
4. Developing an accurate sales forecasting model to predict future sales and plan accordingly.

## Process

<code> <b>Data Cleaning and Transformation</b> </code>

* The initial phase involved performing data cleaning tasks, including the removal of null values, the elimination of unnecessary columns, handling duplicates, and adjusting data types to ensure data quality.

<code> <b>Data Modeling</b> </code>

* The subsequent step was to create calculated measures and tables using DAX (Data Analysis Expressions) in Power BI, enhancing the dataset's analytical capabilities.

```
# Created time-series table of sales for forecasting.
  TimeSeriesTable = 
  SUMMARIZE(
    SuperStore_Sales_Dataset,
    SuperStore_Sales_Dataset[Order Date],
    "Total Sales", SUM(SuperStore_Sales_Dataset[Sales])
  )  
  
  # Calculate a measure to determine the number of days it took for delivery.
  DaysToDeliver = 
  DATEDIFF(
    SuperStore_Sales_Dataset[Order Date],
    SuperStore_Sales_Dataset[Ship Date],
    DAY
  )
```

<code> <b>Data Analysis</b> </code>

* Following data modeling, an in-depth data analysis was conducted within Power BI, utilizing various visualization techniques like matrices to identify trends in sales, region-wise sales, category-wise sales, and other pertinent insights.

<code> <b>Dashboard Creation</b> </code>

* The project proceeded with the development of an interactive and dynamic dashboard in Power BI. This dashboard was allowing for seamless navigation between different charts and visualizations to provide a more comprehensive view of the data.

<code> <b>Sales Forecasting</b> </code>

* To deliver forward-looking insights, Power BI's advanced forecasting feature was utilized to perform a 15-day sales forecast. This forecasting capability assists stakeholders in anticipating future trends and making informed decisions.

## Dashboard

The dashboard section offers an array of visualizations that empower users to explore and understand historical sales data. Key features of the dashboard include:

* Visualization of monthly and yearly sales trends.
* Comparison of sales across different categories and sub-categories.
* Geographical distribution of sales.
* Identification of top payment modes, segments, ship modes, and much more.



## Sales Forecasting

The sales forecasting page focuses on predicting sales for the subsequent 15 days. Leveraging historical sales data and advanced forecasting techniques of Power BI.


## Key Insights

The dashboard and forecasting page unveil the following key insights:

1. **Monthly Peaks:** Noteworthy sales spikes in February, August, and October hint at recurring patterns.

2. **Parallel Growth:** While 2020 exhibits higher sales than 2019, the trend patterns remain consistent.

3. **Geographic Leaders:** California takes the lead in sales, closely followed by New York.

4. **Region Impact:** The West region contributes the most to overall sales.

5. **Payment Preference:** Cash On Delivery (COD) emerges as the preferred payment method.

6. **Consumer Champion:** The consumer segment generates the highest sales figures.

7. **Top Category:** Office Supplies stand out as the dominant sales category.

8. **Preferred Shipping:** Standard Class is the preferred shipping choice.

9. **Sub-Category Stars:** Phones and chairs emerge as the top-selling sub-categories.

## Tech Stack

<code> <b>Power BI</b> </code> Desktop Design, visualization, and interactive reporting.

<code> <b>DAX (Data Analysis Expressions)</b> </code> Creation of calculations and measures supporting data visualizations.

<code> <b>Advanced Analytics</b> </code> Predict future sales trends based on historical data.

<code> <b>Power Query</b> </code> Clean and transform raw data into a structured format.


___

Enjoy exploring the Power BI Sales Insights and Forecasting Dashboard! If you have questions or feedback, feel free to contact me.

Contact: shreesht0@gmail.com


