KuaiSearch

KuaiSearch provides an e-commerce search dataset and baseline implementations for recall, ranking, and relevance judgment.

Installation

Requirements: Python 3.8+ and CUDA 11.7+.

pip install -r requirements.txt

Data Preparation

Place the dataset in ./data/ and update the data and model paths in the scripts as needed. Run all commands from the repository root.

Recall

# Preprocess data
bash scripts/recall_data_process.sh

# BM25
bash scripts/recall_bm25_eval.sh

# DocT5Query
bash scripts/recall_doc2query.sh
bash scripts/recall_docT5query_eval.sh

# Dense retrieval
bash scripts/recall_dpr.sh

# Generative retrieval
bash scripts/recall_gr.sh

Ranking

# Preprocess data
bash scripts/ranking_data_process.sh

# Train a ranking model (default: DCNv1)
bash scripts/ranking_train.sh

Relevance Judgment

# Preprocess data
bash scripts/relevance_data_process.sh

# Cross-encoder
bash scripts/relevance_crossencoder.sh

# Bi-encoder
bash scripts/relevance_embedding.sh

# LLM-based classification
bash scripts/relevance_gr.sh
