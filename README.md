# Agentic-RAG

This repository contains a full Q&A pipeline using LangChain framework, Pinecone as vector database and Tavily as Agent. The data used are the transcriptions of TEDx Talks. A short description of how Tokenizers and Embeddings work is included.

The main steps taken to build the RAG pipeline can be summarize as follows:

* **Data Ingestion**: load data from csv file

* **Tokenization**: how a tokenizer works

* **Embeddgings**: how a embeddgings works with cosine similarity concept

* **Indexing**: RecursiveCharacterTextSplitter for indexing in chunks

* **Vector Store**: Pinecone with several namespace (multi-tenancy)

* **QA Chain Retrieval**: RetrievalQA with memory and agents

## 👨‍💻 **Tech Stack**

![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![OpenAI](https://img.shields.io/badge/OpenAI-74aa9c?style=for-the-badge&logo=openai&logoColor=white)
![Jupyter Notebook](https://img.shields.io/badge/jupyter-%23FA0F00.svg?style=for-the-badge&logo=jupyter&logoColor=white)
![Git](https://img.shields.io/badge/git-%23F05033.svg?style=for-the-badge&logo=git&logoColor=white)


## 📐 Set Up

In the initial project phase, the documents are loaded using **CSVLoader** and indexed. Indexing is a fundamental process for storing and organizing data from diverse sources into a vector store, a structure essential for efficient storage and retrieval. This process involves the following steps:

- Select a splitting method and its hyperparameters: we will use the **RecursiveCharacterTextSplitter**.

- Select the embeddings model: in our case the **OpenAI**

- Select a Vector Store: **Pinecone**.

Storing text chunks along with their corresponding embedding representations, capturing the semantic meaning of the text. These embeddings facilitate easy retrieval of chunks based on their semantic similarity. 

After indexing, a QA Chain Retrieval Pipeline is set up in order to check the Q&A functioning and performance. Memory and Agents any are included in the process.

