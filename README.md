# Sentiment-analysis-of-yelp-reviews-dataset

  A deep neural network model for the sentiment analysis of multi-class problem. Natural language processing methods are done to convert the text data into numerical input for networks. 
  
  Sentiment analysis is contextual mining of text which identifies and extracts subjective information in source material, and helping a business to understand the social sentiment of their brand, product or service while monitoring online conversations. However, analysis of social media streams is usually restricted to just basic sentiment analysis and count based metrics. This is akin to just scratching the surface and missing out on those high value insights that are waiting to be discovered.
  
For data: https://drive.google.com/open?id=1txVKoVvh48PtVG8xjL-4Qff8ihZZo3Y2

This data was obtained for the kaggle competition: https://www.kaggle.com/c/sentclf

Since it was private competition, we are using the train data only and then train-test split it
All rights are own by YELP reviews dataset.
Please refer acknowledgement of the kaggle page to more details on restrictions.

## CLeaning/pre-processing:

1 Removed Punctuations (Python String Lib)

2 Removed Stop words(NLTK.Corpus)

3 Removed errors, corrupt data 

4 Removed other languages(Detected using Lang detect)

5 Removed Special Characters (decode(utf-8))

6 Stemming (NLTK.stem, SnowballStemmer)

## Vectorization:

### WORD2VEC
Imported from gensim.models library 
Word2vec is a two layer shallow neural network which produces a low- dimensional vector representation from a corpus of text,  which preserves the contextual similarity of words. So word embeddings turn text into numbers.

CBOW means continuous bag of words. SG means Skip Gram. With a corpus, CBOW model predicts the current word from a window of surrounding context words, while Skip-gram model predicts surrounding context words given the current word.

For example, let's say we have the following sentence: "I love dogs". CBOW model tries to predict the word "love" when given "I", "dogs" as inputs, on the other hand, Skip-gram model tries to predict "I", "dogs" when given the word "love" as input.


### TFIDF 
Imported from sklearn.feature_extraction.text library
If the document is very large, we have to take into account specific terms that appear in a very few documents, as they are more informative. IDF provides high values for rare words and low values for common words.

Wik = Tfik * log(N / nk)

Tk = term k in document Di

Tfik = frequency of term Tk in document Di

Idfk = inverse document frequency of term Tk in Corpus

N = total number of documents in the Corpus

Nk = the number of documents in Corpus that containTk 

Idfk = log(N / nk) 
 
## Deep Neural Network Model
Using keras

![Model summary](https://user-images.githubusercontent.com/33830482/43615284-873d18a0-96d4-11e8-8f8a-1a18943d5bc6.png)

## Results

# confusion matrix

![Confusion matrix](https://user-images.githubusercontent.com/33830482/43615309-9e01aa7e-96d4-11e8-91d0-293597b9ef17.png)

# classification report

![Classification report](https://user-images.githubusercontent.com/33830482/43615314-aa2d050a-96d4-11e8-8110-6f4dd3a7d6f9.png)

