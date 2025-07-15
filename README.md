Superstore Sales Analysis with PySpark & Time Series Forecasting
This project focuses on analyzing and forecasting sales data from a superstore using Apache Spark (PySpark). It integrates time series forecasting, Spark SQL, and data visualization through Matplotlib and Seaborn to uncover business insights.

1. Dataset Overview
Source: The dataset is loaded using spark.table("superstore_sales_dataset").

Features: Includes fields such as Order Date, Ship Date, Region, Category, Sales, State, City, and others relevant to sales analysis.

2. Data Exploration
Initial exploration steps included:

Using .show(), .printSchema(), and .describe() for an overview of the dataset.

Identifying key variables for analysis, including Sales, Customer, Date, and Region.

3. Data Cleaning
Cleaning steps involved:

Removing duplicate records using dropDuplicates().

Eliminating rows with missing values using dropna().

Casting columns to appropriate data types (e.g., Sales to DoubleType, Order Date to DateType).

Verifying the schema post-cleaning to ensure consistency.

4. Exploratory Data Analysis (PySpark)
Performed aggregate analysis using PySpark:

Identified top customers based on total sales.

Aggregated sales across various dimensions such as:

Country, City, State, Region

Year, Month, and Quarter

Used functions like groupBy(), agg(), and orderBy() for summarization.

Applied Window functions to extract top-performing customers per region.

5. Time Series Forecasting
After aggregating sales by month:

Converted the PySpark DataFrame to Pandas for modeling purposes.

Developed a seasonal Auto ARIMA model using the pmdarima library.

Split the dataset into training and testing sets (80/20 ratio).

Evaluated model performance using:

Mean Squared Error (MSE)

Mean Absolute Error (MAE)

R-squared (R²) score

6. Advanced Transformations with PySpark SQL
Applied more complex logic using PySpark SQL and DataFrame API:

Utilized .select(), .when(), and .isin() for conditional selections.

Performed string operations using .like(), .startswith(), .endswith(), and .substr().

Created new derived columns using logical expressions and conditional logic.

7. Data Visualization
Visualizations were created using Pandas, Matplotlib, and Seaborn to support the analysis:

Bar charts for sales by region

Line plots for monthly sales trends

Box plots for sales distribution across product categories

Heatmaps showing correlations among numerical variables

8. Technologies Used
Apache Spark (PySpark) on Databricks

Python libraries: Pandas, Matplotlib, Seaborn

pmdarima for time series modeling

Spark SQL and PySpark DataFrame API

9. Project Objectives
Identify trends and patterns in historical sales data

Understand customer and regional sales behavior

Forecast future sales using time series models

Build scalable, distributed data processing pipelines using PySpark
