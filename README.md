# 📄 Success-Driven Title Generation from Scientific Graphs

This project predicts successful research papers using Graph Neural Networks and generates potential paper titles using a large language model.

## 🚀 Overview

We propose a pipeline that:
1. **Embeds citation graph nodes** using a Graph Convolutional Network (GCN),
2. **Classifies successful papers** using a Multi-Layer Perceptron (MLP),
3. **Generates paper titles** using [Falcon-7B-Instruct](https://huggingface.co/tiiuae/falcon-7b-instruct) based on merged embeddings from predicted successful papers.

## 🧠 Model Architecture

- **GCN**: Learns 128-dimensional embeddings from a citation graph of 17K arXiv papers.
- **MLP**: Classifies papers as successful or not based on GCN embeddings.
- **Title Generator**: Selects top-2 successful nodes, merges embeddings, and prompts Falcon-7B-Instruct to generate a title.
