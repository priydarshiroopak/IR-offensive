# Multilingual Hate Speech Detection Model

This repository contains the code and resources for a multilingual (English and Hindi) hate speech detection model. The model is designed to detect hate speech in textual data and can be used for a wide range of applications. This readme file provides an overview of the methodology used, experiments conducted, scope of improvement, and multilingual extensions.

## Methodology

### Translation
For translating non-English languages into English, two machine-learning approaches were employed. The first method utilized Google Translate, a Python module, which translates data online from Hindi to English. The second method involved building an extensive dictionary and using it to replace all Hindi words with their corresponding English translations. Despite the limitations of these approaches, they allowed the translation of other languages into English, which was a crucial step in the project for detecting hate speech.

### Pre-processing
The preprocessing approach involved collecting and cleaning the dataset by removing irrelevant or redundant data. Several standard text preprocessing techniques, including stop word removal, stemming, and other cleaning methods, were performed. Additionally, special characters, emojis, links, and account mentions were removed, and all text was converted to lowercase to ensure consistency in the dataset.

### Base Model
The Naive Bayes algorithm was used for hate speech detection. During the training phase, the algorithm calculates the probability of the occurrence of certain words or features in hate speech and non-hate speech texts. It uses this information to build a classification model. Once the model is built, it can be applied to new, unlabelled texts to determine if they are likely to be hate speech or not.

## Experiments

### Bag-of-Words
The bag-of-words method was used to train a machine learning model on a labeled dataset. The dataset was treated as a collection of individual words or n-grams, and each token was counted and represented as a feature vector. The model calculated the score of each word based on the assigned scores and added up the total score for each label. The label with the highest total score was then predicted as the label for the query text.

### TF-IDF
The term frequency-inverse document frequency (TF-IDF) method was used to detect hate speech by calculating the probability of a query being offensive, given a label. The TF-IDF method involved calculating the term frequency (TF) of each token and the inverse document frequency (IDF) of each token. The model then used these values to calculate the probability of a query being offensive.

## Scope of Improvement/Multilingual Extensions
Additional machine-learning methods and tools can be further explored to enhance the accuracy and efficiency of translations. More advanced NLP methods can also be used in conjunction with the bag-of-words approach to improve accuracy. The model can also be extended to support more languages for multilingual hate speech detection.

For more details, please refer to the [Offensive_query_detection_Report.pdf](Offensive_query_detection_Report.pdf) document in this repository. The ipyng notebook and datasets can be found in the [model](model) folder.