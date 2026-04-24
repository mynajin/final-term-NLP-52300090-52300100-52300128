# final-term-NLP-52300090-52300100-52300128
# Vietnamese Question Answering System using RAG and Fine-tuned LLM
# 1. Introduction

This project aims to develop a Vietnamese Question Answering (QA) system within a specific knowledge domain by combining Retrieval-Augmented Generation (RAG) and fine-tuning techniques on a Large Language Model (LLM).

The system is designed to answer user queries based on a predefined knowledge base, ensuring both factual accuracy and contextual relevance.

# 2. Problem Description

Given a natural language question in Vietnamese, the system retrieves relevant information from a knowledge base and generates an appropriate answer.

The core objectives include:

Enhancing answer accuracy through retrieval mechanisms
Improving language generation quality via fine-tuning
Comparing system performance across multiple configurations
# 3. Dataset Construction

3.1 Domain Selection

A specific domain is selected (e.g., education regulations, healthcare, public administration, or traffic laws) to ensure consistency and relevance of the knowledge base.

3.2 Knowledge Base
Collection of documents and textual resources related to the chosen domain
Preprocessing includes cleaning, segmentation, and normalization
3.3 Question-Answer Pairs
At least 300 QA pairs are constructed for training
At least 50 QA pairs are manually created for testing
The dataset is divided into training and evaluation sets

# 4. Methodology

4.1 Fine-tuning Large Language Model

A pretrained LLM (1B–7B parameters) is fine-tuned using parameter-efficient techniques such as:

LoRA (Low-Rank Adaptation)
QLoRA

The fine-tuning process is conducted on limited computational resources (e.g., Google Colab Free).

4.2 Retrieval-Augmented Generation (RAG) Pipeline

The RAG pipeline consists of the following components:

Chunking: Splitting documents into smaller segments
Embedding: Converting text into dense vector representations
Vector Store: Storing embeddings using tools such as FAISS or Chroma
Retriever: Retrieving top-k relevant chunks based on similarity
Prompt Engineering: Constructing prompts that combine retrieved context and user queries

# 5. Experimental Setup

Four configurations are evaluated to analyze the impact of fine-tuning and retrieval:

Configuration	Fine-tuning	RAG
A	No	No
B	No	Yes
C	Yes	No
D	Yes	Yes

This comparison highlights the contribution of each component to overall system performance.

# 6. Evaluation

6.1 Automatic Metrics

BLEU
ROUGE-L
BERTScore

6.2 Retrieval Evaluation

Recall@5 to measure the effectiveness of the retrieval module

6.3 Human Evaluation

Manual evaluation on 50 test questions
Criteria include correctness, fluency, and relevance
