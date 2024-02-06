# Lab 2: Tokenization, word vectors and language modeling

After the first lab, you've gone through an intensive introduction to LLMs and surrounding topics. In this lab, we'll go through some of the basics of computational linguistics.

Three topics will be covered in this lab:

1. Tokenization
2. Language modeling
3. Word representations

You will find the exercises in [`lab2_exercises`](lab2_exercises.ipynb). Tokenization and language modeling are explained through examples in the exercises themselves. A note on word representations are covered in the reading material below.

## Reading material

I highly suggest you to read through Chapter 1: *Introduction*, although Chapters 2 and 3 will cover the main concepts.

- NLTK book, Chapter 2 and 3
  - Accessing Text Corpora <https://www.nltk.org/book/ch02.html>
  - Processing Raw Text <https://www.nltk.org/book/ch03.html>
- Chapter 2: *Your first NLP example*
- Chapter 3: *Introduction to information search*


## Word representations
When we talk about word *representations*, this usually means assigning some numerical value or a vector of values to a word. We can also call this *vectorization*.

A word vector can be thought of as a mapping between words and their vectors as values:

```python
word_vector_map = {
    "cat": [0.1, 0.2, 0.3, 0.4],
    "dog": [0.2, 0.3, 0.4, 0.5],
    "mouse": [0.3, 0.4, 0.5, 0.6],
    ...
}
```

These kind of vectors and embeddings show up in the majority of NLP applications in some form, and are essential to the implementations of the latest models.

One of the simplest forms of vectorization is a *one-hot vector*. This is a vector of zeros, with a single one at the index of the word in the vocabulary.
If we have a vocabulary of 3 words: cat, dog and mouse, this would be initialized as `[0, 0, 0]`. Thus, we get the vectors:

$vec_{cat} = [1, 0, 0]$

$vec_{dog} = [0, 1, 0]$

$vec_{mouse} = [0, 0, 1]$.

As you can probably imagine, this is an extremely sparse representation when we grow our vocabulary to thousands of words. For real-world applications, dense representations are more suitable, and this is where word embeddings come in. Word embeddings, typically trained on large corpora with neural networks, are able to capture both semantic and syntactic information about words by looking at the context in which they appear (overly simplified). This is an effect of the *distributional hypothesis*:

> You shall know a word by the company it keeps (Firth, 1957)

These embeddings allow us to perform mathematical operations on words, reducing their dimensions through techniques such as PCA (covered later in the course. Check the playground for a demo). This allows us to visualize the embeddings in 2D/3D space for an intuitive understanding of the relationships between words:

![](https://editor.analyticsvidhya.com/uploads/450121_sAJdxEsDjsPMioHyzlN3_A.png)

