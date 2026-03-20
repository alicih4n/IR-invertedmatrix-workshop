# 🛠️ Inverted Matrix Workshop: Information Retrieval Pipeline

This project implements a complete **Inverted Index** pipeline, which is a foundational structure for many information retrieval and search systems. The goal is to process a collection of text documents and build an efficient indexing mechanism for boolean and phrase queries.

---

## 👥 Project Contributors
- **Ali Cihan Ozdemir** - 9091405

---

## 🎯 Purpose and Goals
The primary objective of this workshop is to understand how an inverted index is built and used to enable fast text searches. In this repository, we:
- Collect and process a text corpus.
- Implement tokenization and normalization techniques.
- Build an inverted index to map unique tokens to document IDs.
- Create a mechanism to handle complex phrase queries through positional-like matching.

---

## 🔧 What Was Done

### 1. Document Collection
- Fetched 20 blog posts from the **Python Software Foundation** RSS feed.
- Cleaned and saved documents as individual `.txt` files in the `sample_docs/` directory.

### 2. Tokenization Implementation
- Developed a robust tokenizer using regular expressions to break raw text into individual lowercase words (tokens).
- Addressed edge cases like punctuation removal and non-alphanumeric filtering.

### 3. Normalization Pipeline
- Implemented a normalization stage using:
  - **NLTK Stop Word Removal**: Filtering out common words (e.g., "in", "the", "a") that add little meaning.
  - **Porter Stemmer**: Applying mechanical suffix-stripping to reduce words to their base forms (e.g., "running" → "run").

### 4. Build and Query Inverted Index
- Multi-step mapping of every normalized term to the documents where it appears.
- Performed statistical analysis on the index (vocabulary size, term frequency, Zipf's Law validation).
- Implemented **Phrase Querying** using a sliding-window sequence matching approach on normalized tokens.

---

## 🚀 How to Run the Project

Follow these steps to set up and run the workshop notebook locally:

### 1. Prerequisite Environments
Ensure you have **Python 3.8+** installed on your system.

### 2. Install Dependencies
Install the required Python libraries using the `requirements.txt` file provided:
```bash
pip install -r requirements.txt
```

### 3. Run the Jupyter Notebook
Open the workshop notebook in your preferred editor (Jupyter, VS Code, or PyCharm):
```bash
jupyter notebook IR_InvertedMatrix_Workshop.ipynb
```

### 4. Note on NLTK Data
The first execution of the code will automatically download necessary NLTK datasets (`stopwords`, `wordnet`, `omw-1.4`). Ensure you have an active internet connection for the initial run.

---

## 🔍 Dataset Description
The dataset consists of the latest 20 blog posts from the [Python Software Foundation Blog](https://pyfound.blogspot.com/). It offers a rich variety of technical vocabulary and real-world RSS content suitable for demonstrating NLP pipelines.
