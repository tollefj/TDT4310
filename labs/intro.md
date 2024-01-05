# Introductory exercise: Large language models and the latest developments
Due to the immense impact of LLMs since the introduction of ChatGPT in November 2022, we encourage students to delve into these topics before going into the basics of computational linguistics. Thus, we will start with exercises challenging you to study the main ideas behind large language models. Some suggested material is listed below, but you are expected to find reliable information from other sources as well to cover the questions.

This exercise will consist of theoretical questions, where the answers should be around one sentence in length. Future exercises, or *labs*, will be more practical and hands-on.

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

### GPT 
[GPT (Generative Pre-trained Transformer)](https://cdn.openai.com/research-covers/language-unsupervised/language_understanding_paper.pdf) is essentially an autoregressive language model. It learns to predict the next token given an existing series of tokens (e.g. predicting the next word in a sentence), left to right. This token is selected from a probability distribution of next tokens from its vocabulary. 

Computer science students love to ___ 
```
Code 0.90 
Study 0.09 
Cook 0.01 
```

## Suggested material
- [Andrej Karpathy on LLMs](https://www.youtube.com/watch?v=zjkBMFhNj_g)
- [ChatGPT basics](https://www.assemblyai.com/blog/how-chatgpt-actually-works/)


# Questions

**1. A language model (LM) is...**
**2. A large language model (LLM) is...**
**3. A pre-trained base/foundation model is... **
**4. What do we mean by fine-tuned language models, and what does the *head* mean in this context?**
**5. Which one is more suitable for a chatbot: a pretrained model or a fine-tuned model?**
**6. What do we mean by knowledge cutoff in models like ChatGPT?**
**7. What do we mean when we talk about confabulations/hallucinations of LLMs? ***
**8. The context length (e.g. 4096) of a GPT-based model is...**
**9. Why is it problematic to increase the context/sequence length for transformer-based models?**
**10. Parameters are used to describe the model size of LLMs (such as 7B, 13B, …). What do these parameters represent, and what makes LLMs difficult to interpret**
**11. Quantization (e.g. through techniques like LoRa, GPTQ, AWQ) is typically used to reduce the size of LLMs allow them to be run on consumer-grade hardware - even laptops! A common approach is to reduce the precision of the model weights. What does this mean**
**12. LLMs need vast training data. The size of training data is typically referred to as tokens. What is a token and what happens to unknown words outside of the models' vocabulary?**
**13. What is the difference between model training and model inference?**
**14.  Why are GPUs (graphics processing units) ideal for training larger transformer-based models?**
**15.  What is the biggest technical limitation with respect to GPUs for training LLMs?**
**16. LLMs aimed towards human interactions should be *aligned*. What does this mean?**
**17. RLHF (reinforcement learning from human feedback) is used in models like ChatGPT. While you are not expected to learn about reinforcement learning (RL), explain the following terms in context of LLMs (1 sentence each):**
    - SFT (supervised fine-tuning)**
    - Reward model**
    - Policy model**
**18. For the above procedures, we require data, ideally labeled by humans. This is called data annotation. In this context, what is inter-annotator agreement, and why is it important for model creation?**
**19. Do you believe LLM projects should be open-sourced? Why**
**20. Why is it important to consider the ethical implications of LLMs**