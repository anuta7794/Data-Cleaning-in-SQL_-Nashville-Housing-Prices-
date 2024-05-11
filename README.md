# **Data Cleaning in SQL "Nashville Housing"**

In this project, I performed an exploratory analysis on the "Nashville Housing Data" database in SQL Server Management Studio. The data was retrieved from (https://www.kaggle.com/datasets/tmthyjames/nashville-housing-data). The main goal of this project was to clean this data to make it more friendly to use.  

### **Steps:**

1) **_Standardize Sale Format._**

I standardized the data format using **CONVERT**.





2) **_Populate Property Address Data._**

There were **NULL** values in the “Property Address” column. I populated it with property address values using **self-JOIN** and **ISNULL** function. 


3) **_Breaking Out Address into Individual Columns (Address, City, State)._**

I broke out “Property Address” into “Property Split Address”, “Property Split City”, "Owner Split Address”, “Owner Split City”, and "Owner Split State” using **SUBSTRING** and **CHARTINDEX** as well as **PARSENAME** and **REPLACE**.


4) **_Change Y and N to Yes and No in "Sold as Vacant" field._**

I changed Y and N to YES’s and NO’s using **CASE** statements.


6) **_Remove Duplicates._**

I removed duplicates using **ROW_NUMBER**, a **CTE** and window function of **PARTITION BY**.


8) **_Delete Unused Columns._**

In the end, I deleted a few useless columns that I no longer wanted to see such as “Property Address”, “Owner Address”, “Tax District”, and “Sales Date” using **DROP** function.

