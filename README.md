# Enhancing Sentiment Analysis with Transformer Models

### CSC464 — Deep Learning & Natural Language Processing

## 📌 Project Overview

This project explores **sentiment analysis** on movie reviews by comparing a **traditional machine learning approach** with a **modern transformer-based model**.

The goal is to evaluate how well each model classifies text as **positive or negative**, and to highlight the advantages of contextual understanding in Natural Language Processing (NLP).

---

## 🎯 Objectives

* Implement and evaluate:

  * **Logistic Regression + TF-IDF** (baseline)
  * **BERT (Transformer model)**
* Compare performance using standard metrics:

  * Accuracy
  * Precision
  * Recall
  * F1-score
* Analyze the impact of **contextual embeddings** vs **bag-of-words approaches**

---

## 📊 Dataset

* **IMDB Movie Reviews Dataset**
* 50,000 labeled reviews:

  * 25,000 training
  * 25,000 testing
* Binary classification:

  * `1` → Positive
  * `0` → Negative
* Balanced dataset (50/50 split)

A subset of the dataset was used due to computational constraints while preserving class balance 

---

## ⚙️ Preprocessing

* Lowercasing text
* Tokenization:

  * Standard tokenization for Logistic Regression
  * BERT tokenizer for transformer model
* Stopwords:

  * Removed for Logistic Regression (optional)
  * Kept for BERT (important for context)
* TF-IDF vectorization for traditional model

---

## 🧠 Models

### 🔹 Logistic Regression (Baseline)

* Uses **TF-IDF features**
* Fast and efficient
* Treats words independently (no context)
* Serves as a reference model

### 🔹 BERT (Transformer Model)

* Pre-trained **Bidirectional Encoder Representations from Transformers**
* Fine-tuned for sentiment classification
* Captures **context from both directions**
* More accurate but computationally expensive

---

## 🏋️ Training

* Same dataset split used for both models
* Tools:

  * `scikit-learn` (Logistic Regression)
  * `HuggingFace Transformers` (BERT)
* BERT trained for **1 epoch** due to compute limitations
* Subset of dataset used for faster experimentation 

---

## 📈 Evaluation Metrics

* **Accuracy** — overall correctness
* **Precision** — correctness of positive predictions
* **Recall** — ability to find all positives
* **F1-score** — balance between precision and recall
* **Confusion Matrix** — error analysis

---

## 📊 Results

| Model               | Accuracy | F1 Score | Precision | Recall |
| ------------------- | -------- | -------- | --------- | ------ |
| Logistic Regression | 0.85     | 0.86     | —         | —      |
| BERT                | 0.9155   | 0.9162   | 0.9086    | 0.924  |

### 🚀 Key Findings

* BERT achieved:

  * **+7.7% improvement in accuracy**
  * **+6.5% improvement in F1-score**
* Better handling of:

  * Context
  * Negation
  * Complex language patterns 

---

## 🔍 Discussion

* Logistic Regression:

  * Simple and efficient
  * Limited by lack of context
* BERT:

  * Captures semantic meaning using bidirectional attention
  * More accurate and consistent
  * Requires more computational resources

Trade-off:

> **Performance vs Efficiency** — choosing the right model depends on available resources and use case.

---

## ✅ Conclusion

* BERT significantly outperforms traditional methods in sentiment analysis
* Contextual understanding is critical for NLP tasks
* Transformer-based models provide **state-of-the-art performance**
* However, they come with higher computational cost

---

## 🚀 Future Work

* Train on full dataset
* Hyperparameter tuning
* Experiment with lighter models (e.g., DistilBERT)
* Compare with LSTM-based models

---

## 🛠️ Technologies Used

* Python
* Jupyter Notebook
* scikit-learn
* HuggingFace Transformers
* datasets library

---

## 📂 Project Structure

```
project/
│── project.ipynb
│── README.md
```

---

## 👥 Authors

* Rim Serhan
* Mohamad Jawad Allouche

Lebanese American University
CSC464 — Deep Learning & NLP

---

