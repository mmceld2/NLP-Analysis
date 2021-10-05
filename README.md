# NLP-Analysis

Data comes from data.world and we are working with about 9091 rows of data. 


Our data are all tweets from twitter during the sxsw that are classified as objects in our dataframe. The tweets are targeted toward an apple or google product, listed along with tweet is the sentiment(positive, negative, neutral) connected to the product or company.


Our target is developing a model that can analyze tweets and determine the sentiment of it. The labels are the sentiments that were rated by humans to be positive, negative, neutral or unknown. We decided to combine the unknown and neutral categories into just neutral. Distribution of the labels are:

Positive: 34%

Neutral: 60%

Negative: 6%


Two major limitations are the imbalance of sentiments and the chaotic structuring of the tweets. 

