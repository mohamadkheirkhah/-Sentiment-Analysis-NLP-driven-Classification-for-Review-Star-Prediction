# Yelp Reviews Sentiment Analysis

## Project Overview
This project focuses on sentiment analysis using Natural Language Processing (NLP) techniques to classify Yelp reviews into 1-star or 5-star categories based on their textual content. The dataset used is the Yelp Review dataset from Kaggle, where each observation represents a review of a business by a user.

## Data Preparation
- **Dataset:** Read the Yelp dataset (yelp.csv) and create a dataframe called 'yelp'.
- **Feature Engineering:** Add a new column called "text length," representing the number of words in the 'text' column.
- **Exploration:** Identify and find the longest review in the dataset.

## Exploratory Data Analysis (EDA)
- **Visualization:** Plot a histogram of reviews per each star rating (1 through 5).
- **Data Integrity:** Ensure there are no missing records in the dataset.

## NLP Classification Task
### Text Cleaning
- **Objective:** Remove punctuation and stop words from the reviews.
- **Implementation:** Create a function, `clean_text`, to tokenize each review into a list of words.

### Bag of Words
- **Technique:** Utilize CountVectorizer and apply the `clean_text` function as an analyzer.
- **Output:** Create a bag_of_words, where each row represents a review, and columns are words with values indicating the word occurrences.

### TF-IDF Transformation
- **Transformation:** Transform the bag_of_words into a sparse matrix using the "tf-idf" transformation.
- **Formula:** Define the tf-idf formula: `tf-idf(t, d) = tf(t, d) * idf(t)` with `idf(t) = log [ n / df(t) ] + 1`.

## Train Test Split
- **Data Splitting:** Split the data into training, cross-validation, and test sets.

## Training a Model
### Multinomial Naive Bayes
- **Algorithm:** Train a Multinomial Naive Bayes model for classification.

### Support Vector Machine (SVM)
- **Comparison:** Repeat the classification task using Support Vector Machine to compare results.

### Pipeline
- **Optimization:** Implement a pipeline for better organization and efficiency.

## Predictions and Evaluations
- **Performance Evaluation:** Evaluate the performance of the models.
- **Observation:** Initially observe a potential issue with the use of tf-idf, which is addressed by creating a pipeline with only CountVectorizer and Naive Bayes Classifier.
- **Improvement:** Demonstrate improved results and potential for further refinement.

## Conclusion
- **Algorithm Comparison:** Conclude that both Naive Bayes and SVM algorithms yield similar results for the sentiment analysis task.
- **Acknowledgment:** Acknowledge that further improvements can be made with additional data exploration and refinement.
