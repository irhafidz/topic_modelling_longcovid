# Comparative Topic Modelling on Long COVID Twitter Discourse

![License: CC BY-NC-ND 4.0](https://img.shields.io/badge/License-CC%20BY--NC--ND%204.0-lightgrey.svg)

## 📑 About the Project
This Github repo is the pages for our ISICO 2015 paper:

**“A Comparative Analysis of Topic Modelling Methods on Twitter Data Related to Long COVID”**  
Authors: Nathanael Putra Ganata, Irmasari Hafidz, Faizal Johan Atletiko  
Affiliation: Department of Information Systems, Institut Teknologi Sepuluh Nopember (ITS), Indonesia

We compare five topic modeling methods—**LDA**, **LSA**, **NMF**, **Top2Vec**, and **BERTopic**—on a corpus of 500,000 English tweets tagged with `#longcovid` collected in 2022 from Hafidz [1]. The study evaluates each method's performance using automatic metrics (coherence, diversity), human ratings, and large language model (LLM) assessments.

[1] Hafidz, I. (2022) "Data collection longcovid 2022." Available https://doi.org/10.5281/zenodo.14227098 

## 🚀 Key Findings

- **BERTopic** achieved the highest **coherence (0.6924)** and **diversity (0.7955)** scores, ideal for granular health discourse analysis.
- **LDA** was preferred by human evaluators for **interpretability** and **relevance**, making it more suitable for stakeholder-facing summaries.
- **No single model** universally outperformed the others, reinforcing the need for method selection based on analytical goals.

## 🛠️ Methods Compared

| Model     | Type                | Library Used       |
|-----------|---------------------|--------------------|
| LDA       | Probabilistic       | Gensim             |
| LSA       | Matrix Decomposition | Scikit-learn       |
| NMF       | Parts-Based Decomp. | Scikit-learn       |
| Top2Vec   | Embedding + Clustering | Top2Vec library |
| BERTopic  | BERT + c-TF-IDF     | BERTopic           |

## 📈 Evaluation Metrics

- **Coherence**: Measures semantic consistency of topic words
- **Diversity**: Measures uniqueness among top-n topic terms
- **Interpretability & Relevance**: Evaluated by both humans and LLMs

## 📊 Results Summary

| Model     | Coherence | Top-10 Diversity | Human Interpretability | LLM Relevance |
|-----------|-----------|------------------|------------------------|---------------|
| BERTopic  | **0.6924** | **0.7955**       | 3.65                   | **4.13**      |
| LDA       | 0.5814    | 0.7866           | **4.11**               | 3.93          |
| NMF       | 0.5875    | 0.7563           | 3.88                   | 3.67          |
| LSA       | 0.4534    | 0.4667           | 3.60                   | 3.47          |
| Top2Vec   | 0.4002    | 0.7167           | 3.89                   | 2.87          |

## 📂 Repository Structure

