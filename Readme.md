# Sentimental analysis
## Documentation for this dataset

### content

### What's inside is more than just rows and columns. Make it easy for others to get started by describing how you acquired the data and what time period it represents, too.
### The data is a CSV with emoticons removed. Data file format has 6 fields:
<p>0 - the polarity of the tweet (0 = negative, 2 = neutral, 4 = positive) 
<p>1 - the id of the tweet (2087)
<p>2 - the date of the tweet (Sat May 16 23:58:44 UTC 2009)
<p>3 - the query (lyx). If there is no query, then this value is NO_QUERY.
<p>4 - the user that tweeted (robotickilldozr)
<p>5 - the text of the tweet (Lyx is cool)

## Report

1. **Preprocessing the Text:**

   a. Tokenization: Split the text into individual words or tokens.
      column_to_tokenize=['text','selected_text']
      array_1[column_to_tokenize]=array_1[column_to_tokenize].applymap(lambda x:''.join(word_tokenize(x)))
   
   b. Lowercasing: Convert all words to lowercase to ensure consistent analysis.
   
   c. Removing Punctuation: Remove punctuation marks that don't contribute to sentiment.
   
   d. Removing Stopwords: Remove common words (e.g., "and", "the", "is") that may not carry sentiment.
   
   e. Stemming or Lemmatization: Reduce words to their base or root form (e.g., "running" to "run").

2. **Loading Pretrained Sentiment Analysis Models:**

   Many NLP libraries provide pretrained models specifically for sentiment analysis. Libraries like NLTK, spaCy, and Hugging Face Transformers have prebuilt models you can use.

3. **Analyzing Sentiment:**

   a. Use the pretrained model to analyze the sentiment of the text. The model will predict whether the sentiment is positive, negative, or neutral.
   
   b. Different models may provide probabilities or scores indicating the strength of the sentiment. You can set a threshold to classify the sentiment into positive, negative, or neutral categories.

4. **Postprocessing and Visualization:**

   a. Once you have sentiment scores or labels for each text, you can perform further analysis.
   
   b. Visualize the sentiment distribution using histograms, bar charts, or pie charts.
   
   c. Calculate summary statistics such as the average sentiment score, percentage of positive/negative/neutral sentiments, etc.
