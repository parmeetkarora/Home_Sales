# Home_Sales


Home Sales Analysis
Project Overview

This project leverages SparkSQL to perform an in-depth analysis of home sales data. Using PySpark, key metrics are determined about home sales, with insights generated from various queries about average home prices based on home features, year built, and view ratings. SparkSQL features such as temporary views, caching, and data partitioning are utilized to optimize and manage the data processing workflow.


Repository Structure
Home_Sales.ipynb: Jupyter Notebook containing the complete analysis and code to answer the assignment questions.

home_sales_revised.csv: The dataset used for this analysis, containing details about various home sales.

Project Requirements and Steps

Initial Setup

Repository Creation: A new repository called Home_Sales was created for this project.

Data Download and Import: The home_sales_revised.csv file was read into a Spark DataFrame to prepare for analysis.

Analysis Questions
Using SparkSQL, the following questions were answered:

Average Price for Four-Bedroom Homes

Calculated the average sale price for homes with four bedrooms, grouped by year. 
Results were rounded to two decimal places.

Average Price for Three-Bedroom, Three-Bathroom Homes by Year Built

Found the average sale price of homes with three bedrooms and three bathrooms, grouped by the year built and rounded to two decimal places.

Average Price of Homes Meeting Specific Criteria

Queried the average price of homes with three bedrooms, three bathrooms, two floors, and over 2,000 square feet, grouped by the year built.
Average Price of Homes by View Rating (Above $350,000)


Determined the average price per "view" rating for homes where the average price was over $350,000, with the runtime calculated and rounded to two decimal places.

Optimization and Caching

Caching the Table


Cached the home_sales temporary table to improve performance, especially for repeated queries.

Runtime Comparison

Ran the last query both with and without caching, comparing runtimes to observe caching benefits.
Partitioning and Parquet Formatting
Partition by Date Built

Partitioned the data by date_built and saved it in Parquet format, optimizing data storage and retrieval.
Temporary Table for Parquet Data

Created a new temporary table for the Parquet-formatted data and ran the same average price query to observe runtime improvements.
Uncaching

Uncached the home_sales temporary table and verified it was successfully uncached.

Technologies Used

PySpark: Used to handle large datasets, create temporary views, and execute SQL queries on the data.

SparkSQL: Enabled SQL-like queries to extract specific metrics from the dataset.

Jupyter Notebook: Interactive environment for code execution and data visualization.

Data Partitioning: Improved data management and optimized query runtime.

Parquet Format: Efficient columnar storage format used for partitioned data.

Key Insights and Outcomes

This analysis showcases how SparkSQL and data optimization techniques can be used to efficiently process large datasets. By leveraging caching, partitioning, and Parquet formatting, significant performance improvements were achieved, demonstrating the utility of these techniques for data engineering tasks in real-world scenarios.

Conclusion

The Home_Sales project demonstrates the use of SparkSQL and PySpark for data analysis and optimization in a home sales context. By following the outlined steps, key metrics on home prices were efficiently derived, providing valuable insights into the housing market.

