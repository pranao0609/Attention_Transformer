# Transformer from Scratch for Machine Translation

[](https://opensource.org/licenses/MIT)

This repository contains a from-scratch implementation of the Transformer model from the seminal paper **"Attention Is All You Need"**. The model is trained on a small, curated English-to-French dataset to demonstrate its capabilities for neural machine translation (NMT).

The primary goal of this project is to provide a clear, concise, and well-documented implementation that is easy to follow for educational purposes.

-----

## About the Project

This project demystifies the Transformer architecture by building it step-by-step using Python and PyTorch. Instead of relying on pre-built library functions for the Transformer blocks, each key component—such as Multi-Head Attention, Positional Encodings, and the Encoder-Decoder layers—has been implemented from scratch.

By training on a small dataset, this implementation allows for quick experimentation and serves as a practical guide for anyone looking to understand the inner workings of modern NLP models.

-----

## Key Concepts of the Transformer

The Transformer architecture was revolutionary because it solved the problem of sequence-to-sequence learning without using recurrent networks (RNNs), which were slow and had difficulty with long-range dependencies.

  * **Self-Attention Mechanism**: The core innovation. Instead of processing words one-by-one, the model looks at all words in a sentence simultaneously and weighs the importance of every other word when processing a specific word.
  * **Multi-Head Attention**: An enhancement to self-attention. The model runs the attention mechanism multiple times in parallel from different "perspectives" (heads), allowing it to capture different types of relationships (e.g., grammatical, semantic) between words.
  * **Positional Encodings**: Since the model doesn't have recurrence, it has no inherent sense of word order. Positional encodings are vectors added to the input embeddings to give the model information about the position of each word in the sequence.
  * **Encoder-Decoder Structure**:
      * The **Encoder** reads the entire input sentence and builds a rich contextual representation of it.
      * The **Decoder** takes this representation and generates the output sentence word-by-word, paying attention to the encoder's output at each step.

-----

## Implementation Details

To make this project runnable on standard hardware and to train quickly on a small dataset, this implementation is a "Mini-Transformer" with scaled-down hyperparameters.

### Key Modules Implemented from Scratch:

  * **Token Embeddings & Positional Encoding**
  * **Multi-Head Attention**
  * **Position-wise Feed-Forward Network**
  * **Encoder Layer & Decoder Layer**
  * **Full Encoder & Decoder Stacks**

## Example Results

Here are a few examples of translations produced by the trained Mini-Transformer.

| English Input | Model Output |
| :--- | :--- |
| `i am a student` | `je suis un etudiant` |
| `he is a doctor` | `il est un medecin` |
| `she is a lawyer` | `elle est une avocate` |

-----

## Acknowledgments

  * This project is an implementation of the model described in the paper: [Attention Is All You Need](https://arxiv.org/abs/1706.03762) by Ashish Vaswani, Noam Shazeer, Niki Parmar, Jakob Uszkoreit, Llion Jones, Aidan N. Gomez, Łukasz Kaiser, and Illia Polosukhin.
