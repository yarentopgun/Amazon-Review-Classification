# Amazon-Review-Classification

This project focuses on classifying **Amazon product reviews** as positive, negative, or neutral using **Natural Language Processing (NLP)** techniques. The dataset contains **72,500 reviews** with titles, review texts, and star ratings (1–5).

📂 Dataset can be downloaded from the following link:  
[Download dataset (Google Drive)](https://drive.google.com/drive/folders/1SML0SjQKEsUjRRhrkr6J1T8P_4tCQ6tC?usp=sharing)

The notebook: **`amazon-reviews.ipynb`**

---

## Project Overview
The project implements a **Naïve Bayes text classifier from scratch** using the **Bag of Words (BoW)** methodology. Reviews are processed into unigrams, bigrams (and optionally trigrams) for classification.

- **Classification Strategy:**
  - 1–2 stars → Negative  
  - 4–5 stars → Positive  
  - 3 stars → Neutral or optionally dismissed (depending on approach, reasoning explained in notebook).  
  - Weighting applied: stronger negativity for 1-star reviews and stronger positivity for 5-star reviews.  
  - Titles and contents considered separately or together with appropriate weighting.

- **Algorithms and Features:**  
  - Bag of Words dictionary (custom implementation).  
  - Naïve Bayes classifier (custom implementation).  
  - Logarithmic probabilities to avoid underflow.  
  - Laplace smoothing and unknown word handling.  

- **Evaluation metrics:**  
  - Accuracy  
  - Precision  
  - Recall  
  - F1-score  
  - Confusion Matrix  

- **Validation:**  
  - 80/20 train-test split   

---

## Bonus Section
As an extension, additional models can be compared:  
- **Word Embeddings + Logistic Regression** (Word2Vec, GloVe).  
- **NLTK-based BoW + Naïve Bayes** (for benchmarking only).  
- Results compared with the custom Naïve Bayes classifier.  

---

## Dataset
- **Samples:** 72,500 reviews, evenly distributed across star ratings.  
- **Features:**  
  - Title  
  - Content (review text)  
  - Star rating (1–5)  

---

## Installation
```bash
# Python 3.9+ recommended
python -m venv .venv
# Windows: .venv\Scripts\activate
source .venv/bin/activate
pip install -U pip
pip install -r requirements.txt
