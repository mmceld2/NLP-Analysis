 # Tweet Sentiment Analysis

## Business Problem
We are freelancers building a model to determine positive, negative, and neutral reactions from tweets. Our goal is to help businesses know customers' immediate feelings and emotions associated with products. This model will help companies be more in touch with their customer base and enable them to address issues quickly and make better marketing decisions.

## Data
[Link to data](https://data.world/crowdflower/brands-and-product-emotions)<br>
Data comes from data.world and contains 9091 tweets. Tweets are from the SXSW tech conference where Apple launched the Ipad2 and are referencing either Google or Apple. 
The dataset consists of tweets that are classified as objects in our dataframe and the sentiment of the tweets as determined by a person.
Two major limitations are the imbalance of sentiments and the chaotic structuring of the tweets. 
The labels are the sentiments that were rated to be positive, negative, neutral, or unknown. We decided to combine the unknown and neutral categories into just neutral.

## Pre-Processing
One NA row was dropped as it had no tweet body. Punctuation was removed and words were tokenized. Snowball stemmer was used to help increase model accuracy. We searched words in the body of the tweet in order to salvage 4886 NA values that were missing the company label. This helped with our EDA process. The original dataset had four categories but we cut down to three by combining two of them into a neutral catgory.

## EDA 

<img src="Images_4_project/download.png" align="center"><br>


This makes the breakdown of our target values 60% neutral, 34% positive, and 6% negative.


<img src="Images_4_project/download (1).png" align="center"><br>

Distribution of tweet sentiment by company of item tweeted about. Apple has more tweets overall, along with more positive tweets.

<img src="Images_4_project/download (2).png" align="center"><br>

Apps and other products have the highest percentage of positive tweets, perhaps because apps were new and very popular at the time. (This data IS from 2011.)

<img src="Images_4_project/download (4).png" align="center"><br>

This wordloud shows the unique words most associated with the positive tweets, showing words like great, cool, and party. This makes sense that these would be associated with positive tweets.

<img src="Images_4_project/download (5).png" align="center"><br>

This wordcloud shows the unique words associated with negative tweets. Words like fail, headache, battery, and long. A common complaint during the festival was the poor battery life of the iphone!

# Model
Our final model is a TFIDFVectorizer with an SVC classifier. This gave us an accuracy score of 70%

<img src="Images_4_project/image.png" align="center"><br>

Our model needs improvement on finding negative sentiments. Moving forward we would like to find more negative tweets for further model training as more data would help improve the accuracy.

For all model iterations please refer to the final notebook.

# Conclusion
An NLP model can help a company:
- Determine sentiment of product quickly after release <br>
- Identify problems not directly reported to company <br>
- Provide quicker feedback than relying on actual reviews <br>
- Can be used to make improvements on events that happen annually <br>

You can see our final notebook [here](https://github.com/mmceld2/NLP-Analysis/blob/main/Final_Notebook-Copy1.ipynb) and our slide deck [here](https://github.com/mmceld2/NLP-Analysis/blob/main/NLP%20Analysis.pdf).

## Contributors: <br>
Mitch McElderry
-  [GitHub](https://github.com/mmceld2)
-  [LinkedIn](https://www.linkedin.com/in/mitch-mcelderry-35a47a99/)

Dillon Medd
-  [GitHub](https://github.com/dmedd98)
-  [LinkedIn](https://www.linkedin.com/in/dillon-medd/)

Angie Rincon
-  [GitHub](https://github.com/AngieKay)
-  [LinkedIn](https://www.linkedin.com/in/angie-davis-rincon-880587125/)







