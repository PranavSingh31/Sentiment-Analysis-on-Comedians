# Sentiment-Analysis-on-Comedians

## Part 1
### 1. Getting the Data

The transcript used here are web-scrapped from the website [Scraps From The Loft](http://scrapsfromtheloft.com) using Beautiful Soup. 

![image](https://user-images.githubusercontent.com/76558062/235884933-57fefcd2-6039-494e-b41d-ab9fcaeaf9c0.png)

**Beautiful Soup** *is a Python library used for web scraping. It provides a set of tools for parsing HTML and XML documents, extracting data from them, and navigating their structure. With Beautiful Soup, a developer can easily extract specific pieces of information from a webpage, such as links, text, images, tables, and more. It works by taking in raw HTML and parsing it into a structured tree-like representation, which can then be searched and navigated using Python code. One of the key features of Beautiful Soup is its ability to handle poorly formatted HTML code, which is common on the web. It can automatically correct errors and make sense of unstructured HTML, making it a valuable tool for web scraping. Overall, Beautiful Soup simplifies the process of web scraping and data extraction, making it easier for developers to gather and analyze data from the web. It is widely used in various applications, including data mining, content aggregation, and web automation.*

### 2. Cleaning the Data

For data cleaning, I have 
+ made all the texts in lowercase 
+ removed punctuations
+ removed numerical values
+ removed common non-sensical texts,
+ have tokenized words
+ removed stop-words.

Two rounds of cleaning has been done to ensure for a more accurate data.

### 3. Organising the Data

The Data has been organised in two formats: 
+ **Corpus** : *In natural language processing, a corpus refers to a large and structured set of texts, typically stored in a digital format, that is used for linguistic analysis and study. A corpus can be made up of various types of text, such as written documents, transcriptions of spoken language, and social media posts. It is often created with a specific research question or application in mind and can be tailored to include a particular language, genre, time period, or topic. Corpora are essential for developing and evaluating natural language processing algorithms and machine learning models that can process and analyze large volumes of text. They can also be used to study language use and change over time, and to create resources such as dictionaries, language models, and machine translation systems.*
+ **Document-Term Matrix** : *A document-term matrix is a mathematical representation of a collection of documents that is commonly used in natural language processing and information retrieval. It is a matrix that maps the frequency of occurrence of words in a set of documents. Each row in the matrix represents a document, and each column represents a word or term that occurs in at least one of the documents. The entries in the matrix are typically counts of how many times each word or term appears in each document. The document-term matrix is a useful tool for analyzing and comparing collections of documents. It can be used to identify important terms and topics in a corpus, as well as to measure the similarity between documents.*

Now for DTM, the most common tokenization technique is to break down text into words. We can do this using scikit-learn's CountVectorizer, where every row will represent a different document and every column will represent a different word. CountVectorizer has many parameters such as encoding, strip_accent, stop_words, token_pattern, ngram_range ...... etc. More could be found on [Documentation - Count Vectorizer](https://scikit-learn.org/stable/modules/generated/sklearn.feature_extraction.text.CountVectorizer.html) official documentation for same

## Part 2
