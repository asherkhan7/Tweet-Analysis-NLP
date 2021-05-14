# Twitter Sentiment with NLP

Working with Brands and Product Emotions dataset from data.world

## Business Case

Build a model that can rate the sentiment of a Tweet based on its content.

## Data Analysis

After the data was cleaned, the data was split into three dataframes: positive, negative, and neutral tweets. Each dataframe was then stripped of stop words, tokenized, and lemmatized. A most frequent word-count was conducted for each dataframe and ploted on a line graph, all data was also normalized for better interpretation. 

The following are bar graphs containing the most requent words used in each tweet sentiment category:
![bar-graph](/Figures/word_count_bar_graphs.png)

The following are word clouds of the most frequent words used in each tweet sentiment category:
![word-cloud](/Figures/positive_wordcloud.png)
![word-cloud](/Figures/negative_wordcloud.png)
![word-cloud](/Figures/neutral_wordcloud.png)

## Modeling

For modeling, we began by defineing the tweets as our data and sentiment as our target variables. We again removed stopwords tockinzed, and lemmatized our data. We then conducted a train test split and processed the data using two methods:

- CountVectorization
- TF-IDF

After we fit transformed our data, we predicted and classified using Random Forest on both processing methods.

## Conclusions

Following are the Random Forest results from the two processing methods:

### CountVectorization-
Test Accuracy: 0.69

Negative:
- Precision: 0.69
- Recall: 0.22
- F1-Score: 0.34

Positive:
- Precision: 0.68
- Recall: 0.40
- F1-Score: 0.51

Neutral:
- Precision: 0.70
- Recall: 0.90
- F1-Score: 0.78

### TF-IDF-
Test Accuracy: 0.69

Negative:
- Precision: 0.66
- Recall: 0.17
- F1-Score: 0.27

Positive:
- Precision: 0.67
- Recall: 0.42
- F1-Score: 0.51

Neutral:
- Precision: 0.69
- Recall: 0.89
- F1-Score: 0.78
