# 📚 Topic Modelling ArXiv Abstracts Using BERTopic

This project analyzes 2.7M arXiv research papers by clustering their abstracts using BERTopic to uncover hidden thematic trends, while leveraging categories as labels for validation. The goal is to map the evolution of scientific topics and identify interdisciplinary connections in large-scale academic literature.

## 🚀 Overview

We utilize **BERTopic**, which integrates Transformer-based sentence embeddings, dimensionality reduction (UMAP), density-based clustering (HDBSCAN), and modern topic representation models (GPT-4o-mini, KeyBERT, and MMR) to produce interpretable and scalable topic models.

This project was built as part of our final submission for CS 5660: Advanced Artificial Intelligence.

## 📊 Results

Our model identified 121 distinct topics from the ArXiv abstracts with the following metrics:
- **Number of topics found**: 121
- **Documents per topic (avg)**: 455.5
- **Topic diversity score**: 0.7322 (higher is better)

### Top 5 largest topics:
- **Topic 0** (Count: 6818): image, to, learning, and, our, methods, on, data, training, performance
- **Topic 1** (Count: 5824): spin, magnetic, temperature, the, phase, in, graphene, electron, of, electronic
- **Topic 2** (Count: 1437): robot, policy, learning, reinforcement, rl, robots, control, agent, tasks, planning
- **Topic 3** (Count: 1326): graphs, graph, vertices, vertex, edge, number, edges, every, if, coloring

Topic size distribution: min=100, max=6818, ratio=0.0147

## ✨ Key Features

- 🧠 Semantic embeddings with `BAAI/bge-small-en` via SentenceTransformers
- 📉 UMAP for dimensionality reduction
- 📌 HDBSCAN for unsupervised clustering (no need to pre-define number of topics)
- 🧾 Topic labeling using:
  - GPT-4o-mini (via OpenAI API)
  - KeyBERT + Maximal Marginal Relevance (MMR)
- 📊 Visualizations of topic clusters and top keywords
- 📈 Scalable to millions of documents

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

## 📂 Repository Structure

```bash
├── dataset/                          # Data directory
│   ├── preprocessed/                 # Preprocessed datasets
│   │   └── arxiv_processed_100000.csv
│   └── raw/sample/                   # Raw and sampled data
│       └── arxiv_sampled_dataset.json
├── notebooks/                        # Jupyter notebooks
│   ├── Data_Cleaning/                # Data preprocessing
│   │   └── Arxiv_datacleaning.ipynb
│   ├── Model_Building_Final/         # Model implementation
│   │   └── Arxiv_BERTopic_Modelling_100,000samples.ipynb
│   └── visualizations/               # Results visualization
│       └── Arxiv_Data_Visualizations.ipynb
├── README.md                         # Project documentation
└── requirements.txt                  # Environment dependencies
```

## 🛠️ Getting Started

### Prerequisites
- Python 3.10 or higher
- Pip package manager

### Installation

1. Clone the repository
```bash
git clone https://github.com/yourusername/arxiv-topic-modeling.git
cd arxiv-topic-modeling
```

2. Install required packages
```bash
pip install -r requirements.txt
```

3. Run the notebooks in the following order:
   - First, data cleaning: `notebooks/Data_Cleaning/Arxiv_datacleaning.ipynb`
   - Then, model building: `notebooks/Model_Building_Final/Arxiv_BERTopic_Modelling_100,000samples.ipynb`
   - Finally, visualizations: `notebooks/visualizations/Arxiv_Data_Visualizations.ipynb`


## 🤝 Contributing

Contributions, issues, and feature requests are welcome! Feel free to check the [issues page](https://github.com/yourusername/arxiv-topic-modeling/issues).

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.
