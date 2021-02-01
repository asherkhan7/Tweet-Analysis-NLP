# Twitter Sentiment with NLP

Working with Brands and Product Emotions dataset from data.world

## Business Case

Build a model that can rate the sentiment of a Tweet based on its content.

## Data Analysis

After the data was cleaned, the data was split into three dataframes: positive, negative, and neutral tweets. Each dataframe was then stripped of stop words, tokenized, and lemmatized. A most frequent word-count was conducted for each dataframe and ploted on a line graph, all data was also normalized for better interpretation. 

The following are bar graphs containing the most requent words used in each tweet sentiment category:
![bar-graph](/figures/word count bar graphs.png)

The following are word clouds of the most frequent words used in each tweet sentiment category:
![word-cloud](/Figures/positive_wordcloud.png)
![word-cloud](/Figures/negative_wordcloud.png)
![word-cloud](/Figures/neutral_wordcloud.png)
