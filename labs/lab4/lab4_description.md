# Lab 4 - POS chunking, dependency parsing, and WordNet

A brief description of each topic and some motivation is given below.

## POS Chunking

POS chunking allows us to group words based on their POS tags. This is useful for finding meaningful groups of words, such as noun phrases (NP) or verb phrases (VP). 

## Dependency Parsing

Dependency parsing can be used to extract the grammatical structure of a sentence. A particularly useful feature is to fetch the subject/objects and the root of a sentence.

## WordNet and SentiWordNet

These are both lexical resources that can be used to extract more information from a word than what is available in the text itself. Wordnet is a lexical database for the English language, which can be used to find synonyms, definitions and more. Sentiwordnet is a lexical database for words and their associated opinionated values.

## Machine Learning task: Sentiment Analysis

Early sentiment models relied on rule-based approaches, e.g. with SentiWordNet. Since then, the field has moved on to machine learning.
After this relatively simplistic (but valuable!) modeling of sentiment, you will develop a NaiveBayes classifier using TF-IDF vectorization. This is done using Scikit-Learn.

## Installation

- NLTK (POS chunking, Wordnet, Sentiwordnet)
- spaCy (dependency parsing)
- scikit-learn (training a classifier) [**NEW**]
- datasets (for the sentiment analysis task) [**NEW**]

```bash
pip install -U spacy
python -m spacy download en_core_web_sm
pip install -U scikit-learn
pip install -U datasets
```

```python
import nltk
nltk.download("universal_tagset")
nltk.download("wordnet")
nltk.download("sentiwordnet")
```

## Reading material

This lab will now be using common data science tools like pandas and scikit-learn. They will not be requiring explicit reading material, but if you have not used these libraries before, you might want to look up some tutorials.

- NLTK chapters 6, 7, 8
- Kochmar, chapters 7, 8
- <https://scikit-learn.org/stable/tutorial/text_analytics/working_with_text_data.html>
