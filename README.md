# TextMining-NLP
project Name: TextMining and Feature Engineering in R

Description: 

Natural Language Processing (NLP) or Text mining helps computers to understand human language. It involves a set of techniques which automates text processing to derive useful insights from unstructured data. These techniques helps to transform messy text data sets into a structured form which can be used into machine learning.

Predict the popularity of apartment rental listing based on given features. Algorithms such as naive bayes, glmnet, deep learning tend to work well on text data.  

Table of Contents:

What is Text Mining (or Natural Language Processing ) ?

Natural Language Processing (NLP) or Text mining helps computers to understand human language. It involves a set of techniques which automates text processing to derive useful insights from unstructured data. These techniques helps to transform messy text data sets into a structured form which can be used into machine learning.

The resultant structured data sets are high dimensional i.e. large rows and columns. 

What are the steps involved in Text Mining ?

Corpus Creation - It involves creating a matrix comprising of documents and terms (or tokens). A document can be understood as each row having product description and each column having terms.

What are the feature engineering techniques used in Text Mining ?

Text Cleaning - It involves cleaning the text in following ways:
Remove words - If the data is extracted using web scraping, you might want to remove html tags.
Remove stop words - Stop words are a set of words which helps in sentence construction and don't have any real information. Words such as a, an, the, they, where etc. are categorized as stop words.
Convert to lower - To maintain a standarization across all text and get rid of case differences and convert the entire text to lower.
Remove punctuation - We remove punctuation since they don't deliver any information.
Remove number - Similarly, we remove numerical figures from text
Remove whitespaces - Then, we remove the used spaces in the text.
Stemming & Lemmatization - Finally, we convert the terms into their root form. For example: Words like playing, played, plays gets converted to the root word 'play'. It helps in capturing the intent of terms precisely.

Text Mining Practical - Predict the interest level

Model Building:

Naive Bayes is popularly known to deliver high accuracy on text data. In addition, deep neural network models also perform fairly well.

Below is the list of popular feature engineering methods used: I worked on TF-IDF technique in this project

1. n-grams : In the document corpus, 1 word (such as baby, play, drink) is known as 1-gram. Similarly, we can have 2-gram (baby toy, play station, diamond ring), 3-gram etc. The idea behind this technique is to explore the chances that when one or two or more words occurs together gives more information to the model.

2. TF - IDF : It is also known as Term Frequency - Inverse Document Frequency. This technique believes that, from a document corpus, a learning algorithm gets more information from the rarely occurring terms than frequently occurring terms.  Using a weighted scheme, this technique helps to score the importance of terms. The terms occurring frequently are weighted lower and the terms occurring rarely get weighted higher. * TF is be calculated as: frequency of a term in a document / all the terms in the document. * IDF is calculated as: ratio of log (total documents in the corpus / number of documents with the 'term' in the corpus) * Finally, TF-IDF is calculated as: TF X IDF. Fortunately, R has packages which can do these calculations effort

3. Cosine Similarity - This measure helps to find similar documents. It's one of the commonly used distance metric used in text analysis. For a given 2 vectors A and B of length n each, cosine similarity can be calculated as a dot product of two unit vectors:

 4.Jaccard Similarity - This is another distance metric used in text analysis. For a given two vectors (A and B), it can be calculated as ratio of (terms which are available in both vectors / terms which are available in either of the vectors). It's formula is: (A ∩ B)/(A U B). To create features using distance metrics, first we'll create cluster of similar documents and assign a unique label to each document in a new column.

5. Levenshtein Distance - We can also use levenshtein distance to create a new feature based on distance between two strings. We won't go into its complicated formula, but understand what it does: it finds the shorter string in longer texts and returns the maximum value as 1 if both the shorter string is found. For example: Calculating levenshtein distance for string "Alps Street 41" and "1st Block, Alps Street 41" will result in 1.

6. Feature Hashing - This technique implements the 'hashing trick' which helps in reducing the dimension of document matrix (lesser columns). It doesn't use the actual data, instead it uses the indexes[i,j] of the data, thus it processes data only when needed. And, that's why it takes lesser memory in computation. In addition, there are more techniques which we'll discover while modeling text data in the next section.  

Installation: 1. download R it is opensource 2. open R studio and upload imbalancedproject folder.

Prerequisites: An Intel-compatible platform running Windows 2000, XP/2003/Vista/7/8/2012 Server/8.1/10.

At least 32 MB of RAM, a mouse, and enough disk space for recovered files, image files, etc. The administrative privileges are required to install and run R-Studio utilities under Windows 2000/XP/2003/Vista/7/8/2012 Server/8.1/10. A network connection for data recovering over network.

Installing R under Windows:

The bin/windows directory of a CRAN site contains binaries for a base distribution and a large number of add-on packages from CRAN to run on 32- or 64-bit Windows (Windows 7 and later are tested; XP is known to fail some tests) on ‘ix86’ and ‘x86_64’ CPUs.

Your file system must allow long file names (as is likely except perhaps for some network-mounted systems). If it doesn’t also support conversion to short name equivalents (a.k.a. DOS 8.3 names), then R must be installed in a path that does not contain spaces.

Installation is via the installer R-3.4.3-win.exe. Just double-click on the icon and follow the instructions. When installing on a 64-bit version of Windows the options will include 32- or 64-bit versions of R (and the default is to install both). You can uninstall R from the Control Panel.

Note that you will be asked to choose a language for installation, and that choice applies to both installation and un-installation but not to running R itself.

