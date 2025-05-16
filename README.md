# 📚 Topic Modelling Arxiv Abstracts Using BERTopic
This project analyzes 2.7M arXiv research papers by clustering their abstracts using BERTopic to uncover hidden thematic trends, while leveraging categories as labels for validation. The goal is to map the evolution of scientific topics and identify interdisciplinary connections in large-scale academic literature.
This project applies modern topic modeling techniques to a large-scale collection of arXiv paper abstracts (~2.7 million), with the goal of automatically clustering them into meaningful topics and generating human-readable labels.


## 🚀 Overview

We utilize **BERTopic**, which integrates Transformer-based sentence embeddings, dimensionality reduction (UMAP), density-based clustering (HDBSCAN), and modern topic representation models (GPT-4o-mini, KeyBERT, and MMR) to produce interpretable and scalable topic models.

This project was built as part of our final submission for CS 5660: Advanced Artificial Intelligence.

---

## ✨ Key Features

- 🧠 Semantic embeddings with `BAAI/bge-small-en` via SentenceTransformers
- 📉 UMAP for dimensionality reduction
- 📌 HDBSCAN for unsupervised clustering (no need to pre-define number of topics)
- 🧾 Topic labeling using:
  - GPT-4o-mini (via OpenAI API)
  - KeyBERT + Maximal Marginal Relevance (MMR)
- 📊 Visualizations of topic clusters and top keywords
- 📈 Scalable to millions of documents

---

## 🧰 Tech Stack

| Tool / Library        | Purpose                            |
|-----------------------|-------------------------------------|
| Python 3.10           | Programming language                |
| SentenceTransformers  | Generating document embeddings      |
| UMAP                  | Dimensionality reduction            |
| HDBSCAN               | Density-based clustering            |
| BERTopic              | Topic modeling pipeline             |
| OpenAI API (GPT-4o)   | High-quality topic labeling         |
| KeyBERT + MMR         | Keyword extraction                  |
| Pandas / Numpy        | Data wrangling and stats            |
| Matplotlib / Plotly   | Visualization                       |

---

## 📂 Repository Structure

```bash
├── Final_code_100000.ipynb     # Main notebook for training and topic modeling
├── aiCS5660_FinalProject_Report.docx  # Final project report
├── README.md                   # This file
└── requirements.txt            # Environment dependencies
