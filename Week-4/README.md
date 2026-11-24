# Week 4 – Tokenizer Comparison

## Aim

To understand and compare different tokenization techniques used in Large Language Models (LLMs), including BPE, WordPiece and SentencePiece, using multilingual text.

## Introduction

Tokenization is the process of breaking text into smaller units called tokens. These tokens can be words, subwords or individual characters.

Large Language Models use tokenizers to convert text into numerical representations that models can process.

In this experiment, I explored three popular tokenization approaches:

1. **BPE (Byte Pair Encoding):** Builds subword units by repeatedly merging frequently occurring pairs of symbols.
2. **WordPiece:** Uses subword tokenization to divide words into meaningful smaller units.
3. **SentencePiece:** Provides a language-independent tokenization approach that can work directly with raw text.

The experiment compares how these tokenization methods process text in English, Telugu and Hindi.

## Technologies Used

| Technology | Purpose |
|---|---|
| Python | Main programming language |
| Hugging Face Transformers | Provides pretrained tokenizer implementations |
| SentencePiece | Supports SentencePiece tokenization |
| BPE | Subword tokenization approach |
| WordPiece | Subword tokenization approach |

## Files Included

- `tokenizer_comparison.py` – Contains the implementation for comparing tokenizers.
- `requirements.txt` – Lists the required Python packages.
- `.gitignore` – Prevents unnecessary files from being tracked by Git.

## Implementation

### 1. Tokenizer Selection

Selected three tokenization approaches: BPE, WordPiece and SentencePiece.

### 2. Multilingual Text Input

Used sample text in three languages:

- English
- Telugu
- Hindi

### 3. Tokenization Process

Each tokenizer processes the input text and converts it into smaller token units.

### 4. Comparison

Compared the tokenization results to understand how different tokenizers divide text into tokens, particularly across different languages.

### 5. Token Analysis

Observed the generated tokens, token IDs and token counts to understand the differences between tokenization approaches.

## Execution

Install the required packages:

```bash
pip install -r requirements.txt
```

Run the Python program:

```bash
python tokenizer_comparison.py
```

## Expected Results

The program displays the tokenization results for the selected text using BPE, WordPiece and SentencePiece.

The results help demonstrate:

- How each tokenizer divides text into smaller units.
- How token IDs represent the generated tokens.
- Differences in token counts across tokenizers.
- How multilingual text is handled by different tokenization methods.

*Note: Actual tokenization results depend on the selected pretrained tokenizer models and input text.*

## Learning Outcomes

- Understood the concept and importance of tokenization in LLMs.
- Learned about BPE, WordPiece and SentencePiece.
- Explored multilingual tokenization using English, Telugu and Hindi.
- Understood how text is converted into tokens and token IDs.
- Compared token counts and tokenization patterns.
- Learned how tokenization affects text processing in Large Language Models.