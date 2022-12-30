# Amazon_Vine_Analysis

## Purpose of Analysis

The purpose of this analysis was to analyze customer reviews written by members of the paid Amazon Vine program and compare to customer reviews not written by members of the paid Amazon Vine program. 

For this analysis data from the tools V1 dataset was utilized. It was obtained from https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Tools_v1_00.tsv.gz

## Analysis Procedure

### ETL 

Google colab and spark was used to perform ETL (extract, Transform, Load) along AWS RDS (relational database service) and postgres. (4) Dataframes were generated and exported to AWS RDS (review_id_df, products_table_df,customers_table_df, vine_table_df) and then loaded into Postgres as tables (review_id_table, products_table,customers_table, vine_table).  Below are screen captures of the 4 tables loaded into postgres:

Also the associated google colab notebook is Amazon_Reviews_ETL.ipynb located in this directory.

![review_id_table](https://github.com/y2k600f4/Amazon_Vine_Analysis/blob/main/review_id_table.PNG)
![products_table](https://github.com/y2k600f4/Amazon_Vine_Analysis/blob/main/products_table.PNG)
![customers_table](https://github.com/y2k600f4/Amazon_Vine_Analysis/blob/main/customers_table.PNG)
![vine_table](https://github.com/y2k600f4/Amazon_Vine_Analysis/blob/main/vine_table.PNG)


### Analysis

From google colab the vine_df was written to a csv file to be used by Pandas to perfrom the analysis. The analysis of interest was comparing 5-star customer reviews reviews written by members of the paid Amazon Vine program and compare to customer reviews not written by members of the paid Amazon Vine program.  

The associated jupyter note book is amazon_vine_analysis.ipynb located in this directory.

### Results

o	How many Vine reviews and non-Vine reviews were there?

285 Vine reviews and 31545 non-Vine reviews

o	How many Vine reviews were 5 stars? How many non-Vine reviews were 5 stars?

![5_star_yes](https://github.com/y2k600f4/Amazon_Vine_Analysis/blob/main/5_star_yes.PNG)
![5_star_no](https://github.com/y2k600f4/Amazon_Vine_Analysis/blob/main/5_star_no.PNG)


163 Vine 5-Star reviews and 14614 non-Vine 5-Star reviews

o	What percentage of Vine reviews were 5 stars? What percentage of non-Vine reviews were 5 stars?

![calc](https://github.com/y2k600f4/Amazon_Vine_Analysis/blob/main/calc.PNG)

57.2% 5-star Vine reviews and 46.3% 5-star non-Vine reviews

## Summary

Almost 60% of the reviews from the Vine program received 5-star reviews compared to ~45% or 15% less for the non-Vine reviews.
There may be a bias towards provided higher (5-Star) reviews for the Vine program due to it being paid.

An additional analysis that is revcommended to support the statement that the Vine program reviews are biased is to analyze and compare the lower star reviews for bot the Vine and non-Vine program.







