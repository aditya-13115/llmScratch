# LLMs from Scratch

*Trying to implement a Large Language Model from scratch :)*

Welcome to the **LLMs from Scratch** repository! This project is a hands-on journey into the inner workings of Large Language Models. Instead of just treating LLMs as a black box, this repository breaks down the "magic" into digestible Jupyter Notebooks.

Here, we build everything from basic text tokenization and self-attention mechanisms to a fully functional GPT architecture. We also cover practical, real-world applications like loading pre-trained weights, classification fine-tuning, and instruction fine-tuning.


## Notebooks Overview

The project is structured sequentially to help you build an understanding from the ground up:

### Phase 1: The Pre-Training Pipeline

* **`data_cleaning_and_preprocessing.ipynb`**
* **Creating Tokens:** Step-by-step text preprocessing and basic tokenization using regular expressions.
* Explains design decisions (e.g., handling whitespaces and punctuation for custom tokenizers).


* **`tokenEmbeddings.ipynb`**
* Loading and working with **pretrained Word2Vec embeddings** to map tokens to vectors.


* **`Attention Mechanism.ipynb`**
* Implements a simple variant of *Self-Attention* from scratch, without trainable weights, to understand the core math of transformer layers.



### Phase 2: Building the Architecture

* **`03_DummyGPT.ipynb`**
* **Building GPT:** Assembles the complete GPT architecture, including Layer Normalization, GELU activations, FeedForward networks, and Multi-Head Attention.
* **Generation & Loss:** Implements text generation, calculates cross-entropy loss, and tracks perplexity.
* **Pre-trained Weights:** Demonstrates how to load actual OpenAI GPT-2 weights into our custom-built architecture.



### Phase 3: Fine-Tuning

* **`04_ClassificationFinetuning.ipynb`**
* **Spam Detection:** Modifies the GPT architecture for a binary classification task using the UCI SMS Spam Collection dataset.
* **Techniques:** Freezing base layers, replacing the output head, and utilizing custom data loaders with padding strategies.


* **`05_InstructionFinetuning.ipynb`**
* **Alpaca Formatting:** Prepares the model to follow instructions using a JSON dataset of instruction-response pairs.
* **Custom Collating:** Handles dynamic padding and masking (`ignore_index=-100`) for efficient training.
* **Automated Evaluation:** Uses a local Llama 3 model (via Ollama) to automatically score and evaluate the fine-tuned model's responses.



---

## Core Concepts Mastered

Throughout these notebooks, several critical deep learning and LLM concepts are explored in depth:

* **LayerNorm vs. BatchNorm:** Understanding why Transformers rely on Layer Normalization.
* **GELU vs. ReLU:** The mathematical and practical benefits of smooth activation functions in deep networks to prevent "dead neurons."
* **Decoding Strategies:** Controlling randomness during text generation using Greedy Decoding, Temperature Scaling, and Top-k Sampling.
* **Weight Tying:** Reusing token embedding weights in the output layer to reduce memory footprint.
* **Padding & Masking:** Safely handling `<|endoftext|>` tokens so padding doesn't skew cross-entropy loss calculations during fine-tuning.

---

## How to Use

1. **Clone the repository:**
```bash
git clone https://github.com/aditya-13115/llmScratch.git
cd llmScratch

```


2. **Install dependencies:**
Ensure you have PyTorch, Tiktoken, Pandas, Matplotlib, and (optionally) TensorFlow installed.
3. **Follow the Journey:**
Start with the data preprocessing notebook and work your way up to instruction fine-tuning. The notebooks are heavily annotated with Markdown blocks to explain the *why* behind the code.

---