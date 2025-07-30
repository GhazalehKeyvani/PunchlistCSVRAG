
# README.md

# Punch List RAG System

This repository implements a Retrieval-Augmented Generation (RAG) workflow for managing and querying punch list data in electrical construction projects. It ingests an Excel punch list (`punchList.xlsx`), builds a vector index, and lets you ask natural-language questions to retrieve relevant items.

---

## Features

- Load punch list entries from an Excel file  
- Generate embeddings with Sentence-Transformers  
- Store and query vectors using ChromaDB  
- Integrate with OpenAI or local Ollama models for RAG  
- Multi-language support via Google Translate  
- Example Jupyter notebook demonstrates end-to-end flow  

---

## Prerequisites

- Python 3.8 or later  
- Jupyter Notebook or JupyterLab  

---

## Installation

1. Clone the repository  
2. Create and activate a virtual environment  
3. Install dependencies:

   ```bash
   pip install --upgrade pip
   pip install pandas openpyxl numpy \
               langchain langchain-community \
               sentence-transformers transformers torch \
               faiss-cpu chromadb \
               googletrans==4.0.0rc1 rank-bm25 \
               ollama groq
   ```

---

## Usage

1. Place your punch list spreadsheet in the project root:

   ```
   punchList.csv
   ```

2. Open **Electrical_CSVRAG.ipynb** in Jupyter  
3. Follow the cells in order:

   1. Install and import libraries  
   2. Load and preview Excel data  
   3. Build vector index  
   4. Run RAG queries against the index  

4. Configure model backend:
   - Set `GROQ_API_KEY` for GROQ  
   - Or point to a local Ollama server  

---

## Project Structure

- **punchList.xlsx** – Excel file with punch list entries  
- **Electrical_CSVRAG.ipynb** – Jupyter notebook implementation  
- **README.md** – This guide  

---

## Contributing

Contributions are welcome. Please open issues or submit pull requests for:

- Support for additional file formats (CSV, JSON)  
- Dockerization for easy deployment  
- Web UI integration  

---
