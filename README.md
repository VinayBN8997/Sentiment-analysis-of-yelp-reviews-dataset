# Sentiment-analysis-of-yelp-reviews-dataset
  A deep neural network model for the sentiment analysis of multi-class problem. Natural language processing methods are done to convert the text data into numerical input for networks. 
  
  Sentiment analysis is contextual mining of text which identifies and extracts subjective information in source material, and helping a business to understand the social sentiment of their brand, product or service while monitoring online conversations. However, analysis of social media streams is usually restricted to just basic sentiment analysis and count based metrics. This is akin to just scratching the surface and missing out on those high value insights that are waiting to be discovered.
  
For data: https://drive.google.com/open?id=1txVKoVvh48PtVG8xjL-4Qff8ihZZo3Y2
This data was obtained for the kaggle competition: https://www.kaggle.com/c/sentclf
Since it was private competition, we are using the train data only and then train-test split it
All rights are own by YELP reviews dataset.
Please refer acknowledgement of the kaggle page to more details on restrictions.

CLeaning/pre-processing:
1 Removed Punctuations (Python String Lib)
2 Removed Stop words(NLTK.Corpus)
3 Removed errors, corrupt data 
4 Removed other languages(Detected using Lang detect)
5 Removed Special Characters (decode(utf-8))
6 Stemming (NLTK.stem, SnowballStemmer)

Vectorization:
WORD2VEC - imported from gensim.models library 
Word2vec is a two layer shallow neural network which produces a low- dimensional vector representation from a corpus of text,  which preserves the contextual similarity of words. So word embeddings turn text into numbers.


TFIDF- imported from sklearn.feature_extraction.text library
If the document is very large, we have to take into account specific terms that appear in a very few documents, as they are more informative. IDF provides high values for rare words and low values for common words.
Wik = Tfik * log(N / nk)
Tk = term k in document Di
Tfik = frequency of term Tk in document Di
Idfk = inverse document frequency of term Tk in Corpus
N = total number of documents in the Corpus
Nk = the number of documents in Corpus that containTk 
Idfk = log(N / nk) 






