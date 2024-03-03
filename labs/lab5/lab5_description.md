# Lab 5 - Topic Modeling and Named Entity Recognition

The final lab of the course! By now, you have been introduced to many of the basic concepts of natural language processing. Before moving on to more advanced topics for your graded projects, this lab will cover two important high-level applications: topic modeling and named entity recognition (NER)!

## Topic Modeling

Topic modeling is on a high level a method for discovering latent topics or topic words within documents. It is commonly associated with unsupervised learning, although there are myriad ways to approach the problem both in a supervised and unsupervised context. The first part of this lab will ask you to distingtuish between these two machine learning techniques in context of topic modeling. You will also be asked about metrics and evaluation of topic models, and finally implement an LDA (Latent Dirichlet Allocation) model using the Gensim library. See installation + documentation below.

## Named Entity Recognition

Named entities are words/phrases that refer to specific entities, such as persons, organizations, locations etc., and *NER* is the task of discovering these.
How you implement the NER model is entirely up to you, but an example could be the pre-trained model from spaCy, or from a more advanced transformer-model. If you wish, you can train your model from scratch with a supervised dataset. Contact us if you wish to experiment with this (for tips on datasets and modeling approaches).

## Installation

```bash
pip install -U gensim
```

## Reading material

- Libraries:
  - Gensim <https://radimrehurek.com/gensim/auto_examples/index.html#documentation>

- Kochmar book:
  - Topic analysis
    - Pages 304-308, 325-342
  - Topic Modeling
    - Pages 349-356, 371-377
  - Named Entity Recognition
    - Pages 384-392, 403-415
