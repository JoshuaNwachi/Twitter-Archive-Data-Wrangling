# Twitter-Archive-Data-Wrangling
## Introduction
In this project, we obtained three datasets from different sources: a Twitter archive, image predictions, and tweet metadata through the tweepy API. The datasets were used to combine, clean and prepare data for analysis.

## Data Sources
1. Twitter Archive: The Twitter archive contained information about tweets including the tweet ID, timestamp, text, ratings column, etc.

2. Image Predictions: The image predictions contained predictions about the breed of dogs in the tweets as well as confidence levels for each prediction.

3. Tweet Metadata: The tweet metadata contained information about the tweet such as the number of retweets and favorites.

## Data Quality and Tidiness Issues
Several quality and tidiness issues were identified in the datasets. Some of the issues include:

1. Twitter Archive:
* The timestamp column was not in the correct datetime format.
* Invalid dog names in the name column.
* Values in the rating_denominator column were not 10.
* Columns in_reply_to_status_id, in_reply_to_user_id, retweeted_status_id, retweeted_status_user_id, and tweet_id were formatted as floats instead of strings.
2. Image Predictions:
* The tweet ID column was formatted as an integer instead of a string.
* Duplicated values in the jpg_url column.
* Dog breed, confidence level, and test results separated into three different columns.
3. Tweet Metadata:
* The id column was renamed to tweet_id to match the other datasets.
## Data Cleaning and Preparation
To address the quality and tidiness issues, the following cleaning and preparation steps were performed:

1. Twitter Archive:
* Converted the timestamp column to the correct datetime format.
* Replaced invalid dog names with the value "None".
* Reformatted the in_reply_to_status_id, in_reply_to_user_id, retweeted_status_id, retweeted_status_user_id, and tweet_id columns as strings.
* Dropped the unnecessary columns in_reply_to_status_id, in_reply_to_user_id, retweeted_status_id, retweeted_status_user_id, and retweeted_status_timestamp.
2. Image Predictions:
* Reformatted the tweet ID column as a string.
* Removed duplicated values in the jpg_url column.
* Unpivoted the dog breed, confidence level, and test results into a single column.
* Combined the cleaned and prepared datasets into a single dataset for analysis.

## Analyzing and Visualizing Data
We address six analytical questions and provide visualizations to support our findings.
* What is the distribution of ratings given to dogs on the platform?
* What are the most popular dog breeds among users on the platform?
* What are the most popular dog names among users on the platform?
* What are the most popular dog stages among users on the platform?
* Is there a correlation between retweet count and favorite count?
* What is the frequency of different dog breeds in the data?
## Conclusion
Data wrangling efforts involved significant cleaning and preparation to make the data usable for analysis. Issues were corrected and data was structured to allow answering the research questions set out. Despite the challenges, a clean and well-structured dataset was created, ready for further analysis.






