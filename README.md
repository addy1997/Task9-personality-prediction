# Task9: Personality Prediction

_Note: The neural net architecture mentioned below is tentative and still under experimentation. We aim to investigate the alternative architectures if necessary._

# Overview

In this task, we aim to use a supervised ML-based approach to predict Big Five personality traits (O.C.E.A.N) from textual data. Tweets often reflect various aspects of user's personality. So, we decided to use tweets to derive these traits. We use Convolutional Neural Networks(CNN) to predict these traits. This approach is partly based on Fei-liu's language independent & composition moel for personality traits.

# Method

Our method involves 4 stages:

* Data preprocessing
* Document-level feature extraction
* Filtering
* Feature extraction (at word-level)
* Classification

## Data preprocessing stage

* This stage involves data splitting, cleansing, unification, and reduction to lowercase.

## Document-level feature extraction

* In this stage, we use the Maireasse baseline to extract positive and negative emotion words from the tweets.

## Filtering stage

* At this stage, we evaluate the tweets for presence of neutral words which don't have a strong emotion (positive or negative) associated with it. Such tweets are eliminated to reduce the input size and training time. 

## Feature extraction stage

* After extracting the words (as mentioned in stage 2), they are converted into word embeddings. Word2Vec principle is used for this. The words are aggregated together to form a sentence as fixed-length word vectors. 

## Classification

* For classification, we use a CNN with 2 hidden layers. Layer description is given below:

![Neural network](https://github.com/addy1997/Twitter_personality/blob/main/proposed_CNN_model.png)

# Current scenario and Challenge

Currently, we are in the data processing stage. _The major challenge is implementing the second layer to aggregate sentence vectors into a document vector_. 

