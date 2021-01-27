# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 3: Web APIs & Classification

## Executive Summary

My company (a water sports equipment company) has approached me (a Forum Community Manager) to start classifying our forum posts into the different water sports category. The bulk of the posts consist of either a kayaking related post or a surfing related post.

## Problem:

The company has a single channel post system that requires a classification solution to help identify between the kayaking related posts and surfing related posts.

## How are we tackling this?

Reddit has a similar subreddits in `r/kayaking` and `r/surfing`. These two subreddits will provide me with tools to learn the words and classify posts that are related to the hobby.

## What are we working with:

Data gathered from the subreddits using the Reddit API has the following format:

Feature|Type|Description
---|---|---
**name**|_object_|Unique id of a post.
**title**|_object_|Title of a post.
**text**|_object_|Body text of a post.
**subreddit**|_object_|Which subreddit the post came from.

## Classification Process:

- Data cleaning and exploration.
  - Find most common words in each subreddit.
  - Remove words that contain the root word `kayak` and `surf`.
  - Remove overlapping words
- Comparing across different models
  - CountVectorizer + Logistic Regression
      - Logistic Model Coefficient Analysis
  - TfidfVectorizer + Logistic Regression
      - Logistic Model Coefficient Analysis
  - CountVectorizer + MultinomialNB
  - TfidfVectorizer + MultinomialNB
  - CountVectorizer + RandomForest
  - TfidfVectorizer + RandomForest
- Best Model Misclassification Error Analysis 

## Conclusion

### Findings

- **MultinomialNB + TfidfVectorizer Model** performs the best amongst the other models in terms of reducing overfitting and accuracy.
- The best model is able to predict at a **79.92% accuracy**.
- **Prevalent Type 1 Error** (Wrongly Predicting Kayaking Post) throughout all 4 models. Suggesting that there might be an existence of a bias due to the baseline score. In other words, when the model is unable to classify a post, it goes back to the baseline score as kayaking has a higher percentage of 51.3%.
- Generally TfidfVectorizer tends to improve the model by increasing score or reducing overfitting (although by a small margin)

### Limitations

- Many of the errors, were due to posts having root words that have been identified with strong coefficients. The machine was unable to distinguish the words.
- At 79.92% accuracy, the model may not be able to effectively predict (with low error) as the number of posts increases.
- Machine is also unable to classify or predict usage of special characters or emojis that may be of a prevalent use in the future.

### Recommendations & Further Exploration

- The accuracy suggests that you would require additional manpower to filter misclassified posts for your forum if the total number of posts is large.
- Train machine to be able to identify variations of a root word via lemmatization.
- Continually expand the database of stopwords with emojis, special characters and geographical locations or landmarks to be able to correctly classify future posts.
- Exploring media processing tools to classify video/image posts.
