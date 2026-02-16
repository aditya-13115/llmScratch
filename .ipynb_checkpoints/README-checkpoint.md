***

# LLM Pre-Training — JupyterLab Directory

This folder contains resources and code samples for core tasks involved in pre-training large language models. Below is an overview of the notebooks in this directory:

## 📓 Notebooks Overview

1. **Attention Mechanism.ipynb**
   - Implements a simple variant of *Self-Attention* from scratch, **without trainable weights**.
   - Great for understanding the basic math and logic behind transformer attention layers.

2. **data_cleaning_and_preprocessing.ipynb**
   - **Creating Tokens:** Shows step-by-step text preprocessing and basic tokenization using regular expressions.
   - Examples include splitting text, removing whitespaces, handling punctuation for custom tokenizers.
   - Explains design decisions (e.g., when to remove or keep whitespaces for applications like code vs prose).

3. **tokenEmbeddings.ipynb**
   - Demonstrates loading and working with **pretrained Word2Vec embeddings** for converting tokens to vectors.
   - Useful for linking tokenization outputs with real numbers and prepping data for models.

***

## How To Use

- Start with `data_cleaning_and_preprocessing.ipynb` to learn token creation and text cleaning.
- Move to `tokenEmbeddings.ipynb` to see how tokens are transformed into embedding vectors using popular pretrained models.
- Dive into `Attention Mechanism.ipynb` for a hands-on implementation of the self-attention building block, which forms the heart of modern transformer architectures.

These notebooks will help you master the **pre-training pipeline for LLMs:** from raw text to tokens, vectors, and attention mechanisms![1]

***
