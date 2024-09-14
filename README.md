# RAG (Retrieval-Augmented Generation) Using Langflow

This repository showcases an implementation of **Retrieval-Augmented Generation (RAG)** using the **Langflow** framework. RAG enhances generative models by incorporating a document retrieval process, enabling more accurate and context-aware outputs.

## Table of Contents
- [Overview](#overview)
- [Features](#features)
- [Architecture](#architecture)
- [Technologies](#technologies)
- [Installation](#installation)
- [Usage](#usage)
- [Customization](#customization)
- [License](#license)

---

## Overview

**RAG (Retrieval-Augmented Generation)** merges the benefits of information retrieval with large language models (LLMs) to generate more informed responses. This project leverages **Langflow** for managing the retrieval and generation pipeline, using external document sources to answer questions and summarize information.

## Features
- **Langflow Integration**: Leverages Langflow’s orchestration to manage RAG workflows.
- **Document Chunking**: Breaks down large documents into manageable chunks for better retrieval and generation.
- **Vector Store Integration**: Supports databases like Astra DB for document retrieval.
- **Efficient Generative Models**: Utilizes Large Language Models (LLMs) to generate contextually-aware text.
- **OpenAPI LLM Support**: Integrates with OpenAPI-based LLMs to enhance the retrieval and generation pipeline.

## Architecture

The project is divided into two main components:

1. **Document Retrieval**: This module retrieves relevant documents based on a user query, leveraging a vector store like **Astra DB**.
2. **Generative Response**: The retrieved documents are passed to a Large Language Model (LLM) via **Langflow**, which generates a coherent and informative answer.

![RAG Architecture](path-to-architecture-diagram.png)

---

## Technologies

- **Langflow**: Orchestrates the RAG pipeline, managing retrieval and generation.
- **Python**: Core language used for development.
- **Vector Databases**: Utilizes databases like Astra DB for document storage and retrieval.
- **LLM (Large Language Models)**: GPT-based models for text generation.


---

## Installation

### Prerequisites
- **Python 3.10+**
- **Langflow**
- **Vector Database** (e.g., Astra DB or any other supported vector database)
- **LLM API Key** (Optional for integrating external language models)

### Steps
1. **Clone the repository**:
    ```bash
    git clone https://github.com/yourusername/rag-langflow.git
    cd rag-langflow
    ```

2. **Install the required dependencies**:
    ```bash
    pip install -r requirements.txt
    ```

3. **Configure the API_keys And Tokens**:
    ```bash
    ASTRA_DB_TOKEN=<your_astra_db_token>
    LLM_API_KEY=<your_llm_api_key>
    ```

4. **Run the Langflow pipeline**:
    ```bash
    python run_pipeline.py
    ```

---

## Usage

To use this system, send a query related to your document collection. The system will retrieve relevant documents, pass them through the LLM, and generate a response.

## Customization

### Adding Your Own Documents
1. Place your documents in a folder.
2. Update the Langflow configuration to point to your new data source.
3. Re-run the pipeline to regenerate vector embeddings for document retrieval.

### Adjusting Chunk Size
You can modify the document chunking size by changing the `chunk_size` parameter in the pipeline configuration to optimize retrieval based on your document length.

---

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.
