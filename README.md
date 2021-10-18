# Amazon_Vine_Analysis
## Overview
This project is aimed to perform ETL on selected dataset, load transformed datasets into SQL for future analysis. The supported software for this project is AWS(Amazon Web Service), Google Colaboratory, PostgreSQL and JupyterNotebook. Sports dataset is being chose and being factored into 4 tables in order to prepare for future actions.

## Background
>In this project, you’ll have access to approximately 50 datasets. Each one contains reviews of a specific product, from clothing apparel to wireless products. You’ll need to pick one of these datasets and use PySpark to perform the ETL process to extract the dataset, transform the data, connect to an AWS RDS instance, and load the transformed data into pgAdmin. Next, you’ll use PySpark, Pandas, or SQL to determine if there is any bias toward favorable reviews from Vine members in your dataset. Then, you’ll write a summary of the analysis for Jennifer to submit to the SellBy stakeholders.

## Results
From the AWS and script, the dataset is being factored into 4 tables and all of them are being loaded into SQL.
###### Customer Table
![](https://github.com/WilliamBHW/Amazon_Vine_Analysis/blob/main/Resources/customers_table.png)
###### Product Table
![](https://github.com/WilliamBHW/Amazon_Vine_Analysis/blob/main/Resources/products_table.png)
###### Review Table
![](https://github.com/WilliamBHW/Amazon_Vine_Analysis/blob/main/Resources/review_id_table.png)
###### Vine Table
![](https://github.com/WilliamBHW/Amazon_Vine_Analysis/blob/main/Resources/vine_table.png)

<br>

Notice: Each table has their own column attribute and unique keys, datasets with corresponding column will need to have data type converted in order to be loaded into PostgreSQL. (for reference, please refer to ```Amazon_Reviews_ETL.ipynb``` and sections ```review_id_table```, ```vine_table```)<br>

After tables being loaded, vine_table is being pulled to analyze on the following categories (all reviews being selected are considered helpful):
- total number of reviews for paid and unpaid vine
- ![](https://github.com/WilliamBHW/Amazon_Vine_Analysis/blob/main/Resources/total_review.png) 
- number of 5 star reviews in paid vine 
- number of 5 star reviews in unpaid vine
- ![](https://github.com/WilliamBHW/Amazon_Vine_Analysis/blob/main/Resources/5star_review.png)
- percentage of 5 star reviews in paid vine
- ercentage 5 star reviews in unpaid vine
- ![](https://github.com/WilliamBHW/Amazon_Vine_Analysis/blob/main/Resources/5star_percent.png)

## Summary
There's a small portion of companies that paid for vine program to recieve rteviews on their product (in fact the number is too small compare to unpaid vine reviews but still large enough for analysis). There's around 12% difference between 5 star reviews of paid and unpaid vine program. For further analysis, condigure the helpful reviews' major words and set them as product labels would be a nice way to promt potential buyers through algorithm. Further more, reviews that are not 5 star also should be considered as they may contribute a large amount of information.
