# Questions

1. A language model (LM) is... 
- A model that outputs the probability distribution for a word given an existing sequence of words.
- Next word prediction: how likely is a word/sentence based on context.

2. A large language model (LLM) is... 
- Essentially just any language model trained on massive amounts of data 
- These models follow some observed scaling laws that results in much better language understanding 

3. A pre-trained base/foundation model is...  
- A generalized model that is trained to perform a range of tasks. 
- The source data is typically internet snapshots, books, and any other accessible data. 

4. What do we mean by fine-tuned language models, and what does the head mean in this context? 
- Typically, we fine-tune (supervised) on a specific task (with annotated data) by adapting the head of the model, that is, layers on top of the feed-forward network 
- The head of the transformer model. A transformer model can have multiple heads (multi-head attention). The final head is the merged output of all of them. 
    - Examples are classification heads, regression heads and seq2seq heads. 

5. Which one is more suitable for a chatbot: a pretrained model or a fine-tuned model? 

- A fine-tuned model. A pre-trained model will simply return the most likely word, with no idea of formatting or alignments to human chatting experiences. 
- A common approach is instruction tuning to get the model to return appropriate formats 

6. What do we mean by knowledge cutoff in models like ChatGPT? 
- The data the model has seen during pre-training. This means it is not updated as you would expect from a google search on current news and events. Many people mistakenly assume it has this knowledge! 

7. What do we mean when we talk about hallucinations of LLMs? 
- That the model produces outputs it states as true, even if it is not. This is a direct consequence of what language models inherently are: probability distributions. 
- This is especially crucial to consider when dealing with citations and authorship. 

8. The context length (e.g. 4096) of a GPT-based model is the... 
- Number of tokens used for the autoregressive next-word prediction. 
- The larger the context size, the longer text we can input to perform operations on, such as retrieving parts of the input, summarization and more. 

9. Why is it not a trivial task to increase the context/sequence length for transformer-based models? 
- The complexity of transformers is quadratic (O(N^2)) 

10. Parameters are used to describe the model size of LLMs (such as 7B, 13B, …). What do these parameters represent, and what makes LLMs difficult to interpret? 
- The number of “features” or “attributes” the model should discover during training. Technically, this is the weights and biases of the neural net. These parameters contain the language understanding, such as grammar, dependencies, and more... 
- We don’t really know what each parameter refers to, as this could be anything, e.g. “the number of e’s in a word”, “the position of o”, “next word is _the_”. Anything! 

11. Quantization (e.g. through techniques like GPTQ and AWQ) is typically used to reduce the size of LLMs allow them to be run on consumer-grade hardware - even laptops! Explain the main idea behind quantization: 
- To reduce the precision of the model weights (parameters), e.g. from single-precision fp-32 to fp-8. This will arguably reduce performance, but we’ve seen that a quantized model with more parameters outperforms lower-parameter models in full precision. 

12. LLMs need vast training data. The size of training data is typically referred to as tokens. What is a token and what happens to unknown words outside of the models’ vocabulary? 
- A unit of text that is processed by a tokenizer. Words will be split into their subword tokens until each part is in the vocabulary. This causes words for other languages than English to be split into more tokens than one would expect and will as a result reduce the effective context length. 

13. What is the difference between model training and model inference? 
- Training: updating weights. Inference: generate predictions. 

14. Why are GPUs (graphics processing units) ideal for training larger transformer-based models? 
- GPUs are ideal for parallel operations like matrix multiplications, which occur frequently in transformer models. 

15. What is the biggest technical limitation with respect to GPUs for training LLMs? 
- VRAM. A model of 70 B parameters will require ~512 GB of VRAM in single-precision. An example of that would be 7xA100 80GB GPUs, retailing for around $200.000 each. 

16. LLMs aimed towards human interactions should be “aligned”. What does this mean? 
- To be “aligned” with human expectations and values.
- Bias, stereotypes and so forth should be avoidable of possible, and so forth.
- Also includes how the output format should be

17. RLHF (reinforcement learning from human feedback) is used in models like ChatGPT. While you are not expected to learn about reinforcement learning (RL), explain the following terms in context of LLMs (1 sentence each): 
- SFT is the resulting language model after being fine-tuned on a carefully selected, high-quality data source 
- A reward model determines the quality of answers from the SFT model, essentially consisting of preferences towards specific answers 
- A policy model uses the reward model to further improve upon the SFT model. By creating a new answer, the reward model presents it with some idea of how good that answer was. 

18. For the above procedures, we require data, ideally labeled by humans. This is called data annotation. In this context, what is inter-annotator agreement, and why is it important for model creation? 
- Expect an answer on a very general level about data annotation. Ideally including some socio-political aspects like gender bias and preferences towards specific people (such as state leaders). Also mention that this depends highly on who trained the model.

19. Do you believe LLM projects should be open-sourced? Why? 
- No real answer here! 

20. Why is it important to consider the ethical implications of LLMs? 
- They can be used for a wide range of malicious applications, and can represent biases we do not want to spread uncontrollably throughout the internet and media. Relying on automatically generated content to reflect human intuitions and judgments is naive and problematic on far too many levels! 

21. *Smaller* language models ($\leq 100M$ parameters) will likely be important in the days to come. What are some motivations for smaller models? 
- Deploying LLMs on consumer-grade hardware (laptops, phones), reduce the environmental footprint. There’s lots of resulting effects by scaling down, such as faster models (although possibly much worse). Infinite trade-offs, infinite possibilities. 
- Accessible and affordable, meaning they can be run (in inference mode) on limited resource regimes (such as laptops and/or small GPUs). 
- Cheaper to develop and pretrain — these models only require a relatively small number of GPUs. 
- Easier to customize for target tasks — small models can typically be fine-tuned on just a single GPU. 
- More energy-efficient — this is an important consideration given concerns about the environmental impact of training and running large-scale AI models. 
- Valuable for educational purposes — they are more manageable and thus easier to understand and tweak. 

 