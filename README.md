# BytePairEncoding
To implement the Byte Pair Encoding (BPE) algorithm for tokenization and assess its performance using a NLTK dataset, with a focus on books. Additionally, creating a reference tokenization using NLTK's punkt tokenizer for comparative analysis.

# BPE Tokenizer Implementation and Evaluation

This repository contains an implementation of the Byte Pair Encoding (BPE) tokenization algorithm in Python. It includes code for training the tokenizer, analyzing its vocabulary, and evaluating its performance against reference tokenizations.

## Table of Contents

- [Introduction](#introduction)
- [BPE Algorithm](#bpe-algorithm)
- [Implementation Details](#implementation-details)
- [Usage](#usage)
    - [Training](#training)
    - [Tokenization](#tokenization)
    - [Evaluation](#evaluation)
- [Visualization](#visualization)
- [Results](#results)
- [Dependencies](#dependencies)
- [License](#license)

## Introduction

Byte Pair Encoding (BPE) is a data compression algorithm that can be adapted for tokenization in natural language processing. It iteratively merges the most frequent pair of characters or tokens into a single token, building a vocabulary of subword units.

This project demonstrates a basic implementation of BPE and evaluates its performance on text from the Gutenberg corpus.

## BPE Algorithm

The BPE algorithm works as follows:

1. Initialize the vocabulary with individual characters.
2. Iteratively:
    - Count the frequencies of all adjacent character pairs.
    - Merge the most frequent pair into a new token.
    - Update the vocabulary with the new token.
3. Repeat until a desired vocabulary size is reached.

## Implementation Details

The code provides a `BPETokenizer` class that handles the training and tokenization processes. It includes methods for:

- `fit`: Trains the tokenizer on a list of texts.
- `tokenize`: Tokenizes a given text using the learned merge rules.
- `encode`: Tokenizes a list of texts.

The implementation also includes functions for:

- Preprocessing text from the Gutenberg corpus.
- Evaluating tokenization performance using metrics like precision, recall, and F1-score.
- Visualizing token length distribution and vocabulary growth.

## Usage

### Training

1. Load and preprocess your training texts.
2. Initialize a `BPETokenizer` object with the desired vocabulary size.
3. Call the `fit` method to train the tokenizer.

### Tokenization

1. Use the `tokenize` method to tokenize a text string.

### Evaluation

1. Load and preprocess your test texts.
2. Obtain reference tokenizations using a standard tokenizer (e.g., NLTK).
3. Use the `evaluate_tokenization` function to compare the BPE tokenization to the reference.

## Visualization

The code also provides functions for visualizing the learning process of the BPE tokenizer, including:

- Vocabulary growth over merge operations.
- Frequency of merged pairs.
- Distribution of token lengths.

## Results

The evaluation results are presented in tables and plots, showing the performance of the BPE tokenizer on various test books.

## Dependencies

- Python 3.x
- NLTK
- Matplotlib
- scikit-learn
- tabulate

To install the required libraries, run: 
!pip install nltk==3.8.1 matplotlib==3.7.1 scikit-learn==1.2.2 tabulate==0.8.10

You'll also need to download the NLTK resources:
import nltk 
nltk.download('gutenberg')
nltk.download('punkt')

## License

[MIT License](https://opensource.org/licenses/MIT)
