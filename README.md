# Amazon_Vine_Analysis
## Overview of Analysis
The purpose of this analysis was to determine if there was a bias between Vine (paid) and non-Vine (unpaid) reviews for different products sold by Amazon. For the analysis, I used PySpark to perform the ETL process by connecting to an AWS RDS instance, pulling a data set, transforming the dataset, and loading it into a PostgreSQL database using pgAdmin. 

Once the data was loaded, I then used PySpark to analyze the data and determine if there was any bias between Vine and non-Vine reviews.

## Results
The dataset that I used can be found here:
https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Books_v1_02.tsv.gz

My results answer the following three questions. Before answering these questions, I filtered the data to show reviews with greater than 20 "votes" and with greater than 50% of the votes being "helpful". Users can vote on reviews to determine if the review is helpful or unhelpful. Filtering this way means that we are only looking at reviews that have been voted helpful by more than 50% of voters. All answers to the following questions were determine after filtering the dataset.

1. How many Vine reviews and non-Vine reviews were there?
In this dataset, there were a total of 403,807 reviews. There were no Vine member reviews in this dataset, so the total number of non-Vine reviews is 403,807.
2. How many Vine reviews were 5 stars? How many non-Vine reviews were 5 stars?
There were 242,899 total (non-Vine) 5-star reviews. There were no Vine reviews, hence no 5-star Vine reviews.
3. What percentage of Vine reviews were 5 stars? What percentage of non-Vine reviews were 5 stars?
The percentage of non-Vine reviews that were 5-star is 60%. This is the same as the percentage of total reviews that were 5-star because there were no Vine reviews.

## Summary
After this analysis, it is not possible to determine if there is any positive bias with Vine reviews since there were no Vine reviews in the filtered dataset (filtered for 20+ votes, 50% or more of which are "helpful"). In order to determine if there is a bias, I could do a few things:
1. Repeat the analysis on the unfiltered dataset (all reviews regardless of if they are "helpful" or not, or if they have less than 20 votes).
2. Repeat the analysis on multiple datasets.

I would also like to compare the 5-star rating rates across different product categories to see if there are biases in some areas, but not all.
