# **Data Cleaning in SQL "Nashville Housing"**

In this project, I performed an exploratory analysis on the "Nashville Housing Data" database in SQL Server Management Studio. The data was retrieved from (https://www.kaggle.com/datasets/tmthyjames/nashville-housing-data). The main goal was to clean this data to make it more friendly to use.  

Steps:

1) Standardize Sale Format

I standardized the data format using CONVERT.




2) Populate Property Address Data

There were NULL values in the “Property Address” column. I populated it with property address values using self-JOIN and ISNULL function. 

3) Breaking Out Address into Individual Columns (Address, City, State)

I broke out “Property Address” into “Property Split Address”, “Property Split City”, Owner Split Address”, “Owner Split City”, Owner Split State” using SUBSTRING and CHARTINDEX as well as PARSENAME and REPLACE.

  
4) Change Y and N to Yes and No in "Sold as Vacant" field
I changed Y and N to YES’s and NO’s using CASE statements.

5) Remove Duplicates
I removed duplicates using ROW_NUMBER, a CTE and window function of PARTITION BY.
6) Delete Unused Columns
In the end, I deleted a few useless columns that I no longer wanted to see such as “Property Address”, “Owner Address”, “Tax District”, and “Sales Date”.

