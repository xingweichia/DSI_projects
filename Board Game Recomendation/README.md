# DSI Capstone Project: Board Game Recommendation


## Problem Statement

[BoardGameGeek](https://www.boardgamegeek.com/) is an online board gaming resource and community. 
The site is updated on a real-time basis by its large and still growing user base, making the 'Geek the largest and most up-to-date place to get gaming information! 

As part of Board Game Geek, our team of data scientist is tasked to constantly make improvement on our website by using latest data collected. In this project, we are tasked to make a more user friendly recommendation system based on data updated in August 2020. We were also tasked to do topic modelling on the user comments to further understand player needs.

## Overview

There are a total of 4 part of codes:
1. Data Cleaning and Exploratory Data Analysis
2. Topic Modelling
3. Modelling with user rating
4. Modelling with board game features

There is also a data description included for more information on the data used in this project.

As the size of the dataset is too big, the data can be obtain from the link provided below.

[Data Source](https://www.kaggle.com/jvanelteren/boardgamegeek-reviews?select=games_detailed_info.csv)

- Board Game infomation such as ranking, designer and publisher. (19330 Board Games)
- Board game user rating and reviews. (15M users)


## Executive Summary

1. Board Game Recommendation_Data

Based on the EDA, we found out that top 5 board games with higher rank are based on bayes average score which are the composite scores of the games which not only take into account the rating of the games but also the sales or other results of the games.

2. Topic Modelling

Data sampling was done on the dataset with a total of almost 15M user entries of rating or comments. After dropping the empty comment, we are left with ~3M rows and only games that have at least 5k user ratings will be included. In order to have a smooth topic modelling process, we also only include comments that have word counts from 10 to 200 words.

Comments were then classified to two classes: Positive or Negative. The threshold being used here is the average rating 6.40. Comments that have ratings more than or equal to 6.40 will be classified as positive and vice versa.

There are some interesting findings from the topic modelling, for example, regardless of positive or negative comments, the most discussed topics are board game mechanic, board game expansion, and playing time. This finding lead us to build a recommendation system that take these topics as a main filter for users when requesting for recommendations.

3. Board Game Recommendation_User Rating

The first model was built by using the user rating of the game to make a recommendation system based on the pairwise distance scores. There are limitations on data collected as there are no user ratings from a single user on multiple games, thus, the recommendation system based on collabrative filtering is not applicable. In this case, the first recommendation system is purely based on the average rating of a board game to recommend the top 5 board games that have similar user ratings.

4. Board Game Recommendation_Board Games Features

In order to enhance the recommendation system, few different models was built with different features. The modelling process took the results from topic modelling into account and built a recommendation system based on board game mechanic and etc. After combining all the keywords, TF-IDF vectorizer was used to create the feature matrix so that the cosine similarity score can be calculated and used to make recommendations.


## Limitation & Recommendation

#### Deploy the models 
- Due to time constraint, the next step for this project will be deploying the models and building the recommendation system in the website for users

#### User profile data for collabrative filtering 
- In order to build a more customised recommendation system, the team should put in effort to collect more user ratings from different games and from there we can easily get the user profile and build a recommendation system that suits each user based on their preferences.

#### Board game features improvements
- Based on the topic modelling, we have some findings that can be provided to board game publishers for further improvements on the board game thus potentially increasing user base and sales. 

