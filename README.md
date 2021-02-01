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

# CountVectorization-

Evaluations for test:
[[25 78   10]
[  8 974 102]
[  3 349 239]
                                    precision    recall  f1-score   support

                  Negative emotion       0.69      0.22      0.34       113
No emotion toward brand or product       0.70      0.90      0.78      1084
                  Positive emotion       0.68      0.40      0.51       591

                          accuracy                           0.69      1788
                         macro avg       0.69      0.51      0.54      1788
                      weighted avg       0.69      0.69      0.66      1788



Evaluations for train:
 [[ 456    1    0]
 [   2 4299    3]
 [   0   33 2354]]
                                    precision    recall  f1-score   support

                  Negative emotion       1.00      1.00      1.00       457
No emotion toward brand or product       0.99      1.00      1.00      4304
                  Positive emotion       1.00      0.99      0.99      2387

                          accuracy                           0.99      7148
                         macro avg       1.00      0.99      0.99      7148
                      weighted avg       0.99      0.99      0.99      7148



# TF-IDF-

Evaluations for test:
 [[ 19  85   9]
 [  6 965 113]
 [  4 341 246]]
                                    precision    recall  f1-score   support

                  Negative emotion       0.66      0.17      0.27       113
No emotion toward brand or product       0.69      0.89      0.78      1084
                  Positive emotion       0.67      0.42      0.51       591

                          accuracy                           0.69      1788
                         macro avg       0.67      0.49      0.52      1788
                      weighted avg       0.68      0.69      0.66      1788



Evaluations for train:
 [[ 456    1    0]
 [   2 4298    4]
 [   0   32 2355]]
                                    precision    recall  f1-score   support

                  Negative emotion       1.00      1.00      1.00       457
No emotion toward brand or product       0.99      1.00      1.00      4304
                  Positive emotion       1.00      0.99      0.99      2387

                          accuracy                           0.99      7148
                         macro avg       1.00      0.99      0.99      7148
                      weighted avg       0.99      0.99      0.99      7148
