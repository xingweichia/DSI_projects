## Project 3: Sub-reddit Posts Classification


### Problem Statement

In a fast paced society, people have less time to read books and there is a growing trend observed in the amount of people listening to audiobooks instead. A book publishing company is looking to publish a new audiobook. As reddit is a network of communities based on people's interests, two subreddits ['r/audiobooks'](https://www.reddit.com/r/audiobooks/) and ['r/booksuggestions'](https://www.reddit.com/r/booksuggestions/) are chosen in order to understand readers interests in audiobooks. 


### Overview

In this project, data collection was done by doing web scrapping on the both subreddit sites. Data obtained consists of all the information of the posts and we are going to look into the `selftext` of the posts and carry out classification. Besides classification, we would also try to get some insight from the content of the posts. 


### Data Collection & Data Cleaning

Data collection part of the project is included in 'Project 3 Data Collection' notebook. Data cleaning was done by dropping duplicate data and checking of null values. Stemming and Lemmatization was also done in order to provide the clean data to be fitted and transformed with vectorizers, giving us the feature of models.

### Modeling and Evaluation

There are a total of 8 models built, 4 models (Logistic Regression, K-Nearest Neighbors, Multinomial Naive Bayes, Multinomial Naive Bayes with best vectorizer parameter) each for two different vectorizer (Count Vectorizer & TF-IDF Vectorizer). Accuracy and sensitivity are the key factors for model evaluation. Among all the models, Multinomial Naive Bayes model with TF-IDF Vectorizer gives the highest accuracy of 0.8308 and sensitivity of 0.8068. 

### Observation

On the wrongly classified posts, there are few same frequently appearing words found in both subreddits. This could be the main reason of wrong classification. In order to further improve the model, we could further remove some of the frequent words that appear in both subreddits.

### Recommendations
Based on the classification done with data from subreddits 'audiobooks' and 'booksuggestions', there are some pointers that a publisher can take note of:
1. If the publisher is going to publish an audiobook, the most used audiobook website would be [Audible](https://www.audible.com/). Thus, publishing at the website would be ideal to reach out to more people. 

2. Words like 'Narrator' and 'free' did frequently appear in subreddit 'audiobooks' posts, this can be a hint for the publisher that the narrator's voice and the price of the audiobooks would be the main concern for readers.

3. As the word 'fiction' and 'love' appear to be the preditor of the subreddit 'booksuggestions', publishers can assume that the most popular genres is fiction, non-fiction or love. 

4. As the community in 'booksuggestions' are usually asking for recommendations or suggestions of good books, the sales and marketing team can consider joining the community to advertise new published books by the company.

