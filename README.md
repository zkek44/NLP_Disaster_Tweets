# NLP_Disaster_Tweets
This repository contains my solution to the Kaggle "Natural Language Processing with Disaster Tweets" competition. The task is to classify whether a given tweet refers to a real disaster or not.

📌 Problem Statement
Given a dataset of tweets, the goal is to predict whether each tweet is about a real disaster (target = 1) or not (target = 0). This is a binary text classification problem.

🗃️ Dataset
train.csv: 7,613 labeled tweets

test.csv: 3,263 unlabeled tweets (for submission)

Columns: id, text, keyword, location, target

Source: Kaggle Competition Data

🔍 Project Pipeline
1. Exploratory Data Analysis (EDA)
Visualized tweet length distribution

Word clouds for most frequent terms

Analyzed keyword frequency by class

Cleaned text (lowercasing, punctuation removal, stopword filtering)

2. Preprocessing
Used GloVe Twitter embeddings (200d) for semantic representation

Tokenized and padded tweet sequences using Keras

3. Model Architectures
Compared multiple RNN-based architectures:

Simple RNN

GRU

Bidirectional LSTM

Used early stopping and dropout for regularization

4. Evaluation
Best model: Simple RNN

Validation accuracy: 81.1%

Precision (class 1): 0.82

Recall (class 1): 0.71

Confusion matrix and F1-score analysis

5. Submission
Generated predictions on the test set

Submission file in id,target format

🚀 Results & Takeaways
GloVe Twitter embeddings significantly improved semantic understanding of tweets.

Surprisingly, Simple RNN outperformed deeper models, likely due to the short sequence length of tweets.

Future improvements could involve transformer-based models (e.g., BERT), data augmentation, or ensembling.
