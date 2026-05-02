# LLMs-TMU-Spring2026
This is the repository contains HWs and answers of LLM course of TMU (Spring2026)
# Word Embeddings and Text Classification
Word2Vec from Scratch, GloVe, Semantic Analysis, Visualization, and Sentiment Classification


## Overview

This repository contains the implementation and analysis of word embedding models and their application to text classification tasks.
The project focuses on both theoretical understanding and practical implementation of distributed word representations.

The workflow starts with implementing Word2Vec (Skip-gram with Negative Sampling) from scratch, followed by evaluation using pre-trained GloVe embeddings, semantic analogy tests, visualization techniques, and an extrinsic evaluation through sentiment classification.


## Objectives

- Implement Word2Vec (SGNS) from scratch without using pre-built embedding libraries
- Compare custom-trained embeddings with pre-trained GloVe embeddings
- Perform intrinsic evaluation using cosine similarity, nearest neighbors, and word analogies
- Visualize high-dimensional embedding spaces using PCA and t-SNE
- Apply word embeddings to a real-world sentiment analysis task
- Study the effect of out-of-vocabulary (OOV) words and approximate a FastText-like solution


## Part 1: Word2Vec from Scratch

Model: Skip-gram with Negative Sampling  
Corpus: text8 (Wikipedia)  
Vocabulary size: 20,000 (with UNK token)  
Embedding dimension: 100  
Context window size: 2  
Negative samples per positive pair: 5  
Training epochs: 3  

### Training Loss

Epoch 1: 2.2544  
Epoch 2: 2.1703  
Epoch 3: 2.1420  

### Qualitative Evaluation

Nearest neighbors for the word "king":

queen (0.7747)  
elector (0.7511)  
prince (0.7430)  
pope (0.7273)  
patriarch (0.6965)  


## Part 2: Pre-trained GloVe Embeddings

Model: glove.6B.100d  
Vocabulary size: 400,000  
Embedding dimension: 100  
Training corpus: Wikipedia + Gigaword  

Example cosine similarity:

similarity(computer, software) = 0.8373


## Part 3: Semantic Evaluation

### Word Analogy

King - Man + Woman ≈ Queen

### Algorithmic Bias Example

Doctor - Man + Woman ≈ Nurse

This highlights bias learned from training data.


## Part 4: Embedding Visualization

Semantic categories:
animals, countries, jobs, fruits, vehicles

Dimensionality reduction methods:
PCA and t-SNE

t-SNE produces clearer semantic clusters than PCA.


## Part 5: Text Classification (Sentiment Analysis)

Dataset:
IMDB movie reviews  
25,000 training samples  
25,000 test samples  

Sentence representation:
Mean pooling over word embeddings  

Classifier:
MLP with one hidden layer  
Hidden units: 64  
Optimizer: Adam  
Loss: Cross-Entropy  

Final Test Accuracy:
78.02%


## Part 6: Out-of-Vocabulary (OOV) Handling

A simplified FastText-like approach using character trigrams was implemented.

Tested words:
happpppy  
computerrr  
phoneee  


## Technologies Used

Python  
NumPy  
PyTorch  
Gensim  
scikit-learn  
Matplotlib  
LaTeX (XePersian)



## Author

Kiarash Rahmani  
Computer Engineering  
Academic Assignment – Natural Language Processing
