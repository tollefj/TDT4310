# Introductory exercise: Large language models (LLMs) and the latest developments
### Published: Monday, Jan. 8, 2024
### Deadline: Tuesday, Jan. 16, 2024

Due to the immense impact of LLMs since the introduction of ChatGPT in November 2022, we encourage students to delve into topics related to LLMs before going into the basics of computational linguistics. Some suggested material is listed below, but you are expected to find reliable information from other sources as well to cover the questions.

This exercise will consist of theoretical questions, where the answers should be around one sentence in length. Future exercises, or *labs*, will be more practical and hands-on. You will find the questions in the [`lab0_exercises`](lab0_exercises.ipynb) notebook. Please submit your answers in the very same notebook and upload it to Blackboard by the deadline. All labs will be provided as jupyter notebooks, so this is an easy transition to get used to the format.

If you want to explore the use of these models, there's an added [`playground file`](lab0_playground.ipynb).

## Background: the transformer
The transformer architecture is behind most of the advanced NLP models since its introduction in 2017 in the paper [Attention Is All You Need](https://proceedings.neurips.cc/paper_files/paper/2017/file/3f5ee243547dee91fbd053c1c4a845aa-Paper.pdf). It introduced parallelized self-attention mechanisms, allowing it to efficiently capture long-range dependencies in sequences, unlike RNNs (Recurrent Neural Networks) and LSTMs (Long Short-Term Memory networks). Two popular models based on the transformer architecture are BERT and GPT.

### BERT 
[**BERT (Bidirectional Encoder Representations from Transformers)**](https://aclanthology.org/N19-1423.pdf) quickly gained popularity as a pre-trained model. BERT is trained for two main tasks: 

1. **Masked Language Model (MLM):** 
   - In the MLM task, BERT learns to predict masked tokens. For example: 
     - Original: "The student is [MASK] about a new topic." 
     - Prediction: "The student is curious about a new topic." 

2. **Next Sentence Prediction (NSP):** 
   - BERT is also trained to predict whether a randomly selected sentence logically follows another sentence in a document. For instance: 
     - Sentence 1: "The cat is on the mat." 
     - Sentence 2: "It is a comfortable spot for a nap." 
     - Random Sentence: "The student loves reading." 
   - BERT learns that the random sentence is less likely to follow Sentence 1 or Sentence 2 in the document. 

A key feature of BERT is that it is bidirectional, meaning that it can use the context of a sentence to predict a masked token. Further, by fine-tuning it towards specific data, to be used for tasks like question answering and sentiment analysis.

### GPT 
[GPT (Generative Pre-trained Transformer)](https://cdn.openai.com/research-covers/language-unsupervised/language_understanding_paper.pdf) is essentially an autoregressive, decoder-only, language model. It learns to predict the next token given an existing series of tokens (e.g. predicting the next word in a sentence), left to right. This token is selected from a probability distribution of next tokens from its vocabulary. 

```
Computer science students love to ___ 
- Code 0.90 
- Study 0.09 
- Cook 0.01 
```

## Suggested material
- [Andrej Karpathy, 1hr talk on LLMs](https://www.youtube.com/watch?v=zjkBMFhNj_g)
- [About ChatGPT](https://www.assemblyai.com/blog/how-chatgpt-actually-works/)
- [Fine-tuning LLMs](https://www.analyticsvidhya.com/blog/2023/08/fine-tuning-large-language-models/)
- Familiarize yourself with HuggingFace, a popular NLP library and model repository. They also host a [great blog](https://huggingface.co/blog) with many interesting articles on NLP.