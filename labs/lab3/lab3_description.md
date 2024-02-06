# Lab 3 - Stemming, Lemmatization, TF-IDF, and part-of-speech tagging

This time, we will do more manipulation of language through stemming/lemmatization and then move on to TF-IDF (term frequency-inverse document frequency) and part-of-speech (POS) tagging.

## Libraries

We continue to use NLTK, but we are now adding spaCy, which can be used to explore POS tags and much more. See <https://spacy.io/>. Feel free to experiment more with the many features of spaCy! They have recently started adding support for LLM applications as well.

## Installation

```bash
pip install -U spacy
python -m spacy download en_core_web_sm
```

## Reading material

Some previous chapters (in Kochmar) were set up as suggested reading in Lab 2 to prepare you for this one, namely the concepts around stemming, lemmatization, and TF-IDF. You should skim through chapters 4, 5 and 6 to follow along with the book. Chapter 4 shows good practical examples of spaCy for POS tagging and lemmatization. Chapters 5 and 6 are more focused on the machine-learning aspects of this course.

Chapters 2 and 3 of the NLTK book are still relevant. Chapter 4 explains some suggested programming styles with Python. Chapter 5 is an excellent introduction to part-of-speech tagging. Chapter 6 starts with the basic foundations of supervised learning.

___

### Text Normalization

Text normalization deals with a large set of techniques, but most commonly:

- Dealing with unwanted characters and symbols (e.g., keeping only alphanumeric characters)
- Lower/uppercasing
- Stopword filtering
- Stemming and lemmatization

The last point is the task of converting text to its standard form. While stemming is a simpler process of reducing words to a common core (*stem*), often by removing suffixes, lemmatization will use dictionaries and definitions to convert words to their base form:

| Word | Stemming | Lemmatization |
| - | - | - |
| information | inform | information |
| informative | inform | informative |
| computers | comput | computer |
| feet | feet | foot |

In chapter 3, Kochmar motivated the use of these concepts by an example:

> "Imagine you wanted to know what *sung* meant. Your best strategy would be to look up sing. Similarly, the search algorithm would benefit from mapping sing, sang, and sung to the same word form, by default the most basic one - sing.

This property is helpful for information search and extraction, especially when dealing with morphologically rich languages.

TF-IDF and POS-tagging are topics covered well by the course book(s) and the lectures.