![Screenshot (40)](https://github.com/PRANITAWANI/Customer-Segmentation-Through-Purchase-History-Data/assets/135104675/1ce21576-e6ad-4c53-9aa0-bf688f02693d)
# Customer Segmentation Through Purchase History Data

## Dataset Information :

Data Source - [Kaggle](https://www.kaggle.com/datasets/mkechinov/ecommerce-purchase-history-from-electronics-store/data)

Raw Dataset Info - 2.6 Million records and 8 columns: event_time, order_id, product_id, category_id, category_code, brand, price, user_id.

Clean Dataset Info - 2 Million records and 19 columns: user_id, order_id, category_id, brand, price, cat_1, cat_2, cat_3, max_purchase_by_user, class_id, class_category, recency, frequency, monetary, customer_type, cust_value, Date, Time, spending.

## Data Cleaning & Preprocessing :
<ul> Removed duplicate records.
Kept the data for year 2020 only as there were only 2 distinct years(1970,2020).
Removed the records ,where brand values are none.
Assign category as miscellaneous where null values are present.
Split the category_code column into 3 columns (cat_1,cat_2,cat_3) on the occurrence of dot ‘.’
Calculated average of price column and assign that value to records where price were zero.
Among 2 million records , 1.5 million user ids are not available.
The challenge here was to fill null values of user id from available distinct user id such that it should not affect the consistency of data.
Calculated the count of distinct user IDs for each category and assigned random user IDs to null values on basis of category column.
