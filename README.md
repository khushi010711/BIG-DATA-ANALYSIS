# BIG-DATA-ANALYSIS
*COMPANY*: CODTECH IT SOLUTIONS

*NAME*:KHUSHI SHAH

*INTERN ID*:CT04DL131

*DOMAIN*:DATA ANALYTICS

*DURATION*:4 WEEKS

*MENTOR*:NEELA SANTHOSH 

## DESCRIPTION

This Python script provides a practical example of using **Dask** for scalable data analysis on a large, simulated e-commerce dataset. It begins by generating a synthetic dataset of **1 million rows** using NumPy and Pandas. Each row represents an individual order, containing fields such as `order_id`, `product`, `customer`, `quantity`, and `price_per_unit`. The script then calculates a new column, `total_price`, by multiplying quantity with price per unit, representing the total cost of each order.

Once the dataset is created, it is converted from a Pandas DataFrame into a **Dask DataFrame** with 10 partitions. This conversion is essential for working with large datasets that may not fit entirely into memory, as Dask allows for parallel computation and out-of-core processing. The Dask DataFrame provides a scalable way to perform analytics while maintaining a familiar Pandas-like syntax.

The script performs three main analytical tasks:

1. **Total Sales per Product:** It groups the data by the `product` column and computes the sum of `total_price` for each product. This gives insight into which products generate the most revenue. The result is sorted in descending order for better visibility.

2. **Average Order Value by Customer:** By grouping the data by `customer` and calculating the mean of `total_price`, the script reveals which customers have the highest average order value, helping identify high-value customers.

3. **Product Purchase Frequency:** It uses `value_counts()` on the `product` column to determine how many times each product was purchased. This metric helps in understanding product popularity and demand trends.

After performing the computations, the results of the sales and customer analysis are saved to CSV files for future reference or reporting. This output can be useful for business intelligence dashboards or decision-making processes.

## OUTPUT

Total Sales by Product:
 product
Keyboard    3.884635e+08
Phone       3.876860e+08
Tablet      3.874650e+08
Laptop      3.872492e+08
Monitor     3.861574e+08
Name: total_price, dtype: float64

Average Order Value by Customer:
 customer
Diana      1942.548751
Charlie    1938.462617
Bob        1937.067757
Eve        1934.750870
Alice      1932.252656
Name: total_price, dtype: float64

Product Purchase Frequency:
 product
Phone       199970
Tablet      199962
Laptop      199918
Keyboard    200379
Monitor     199771
Name: count, dtype: int64[pyarrow]
