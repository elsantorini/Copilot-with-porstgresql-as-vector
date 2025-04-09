# Copilot with PostgreSQL as Vector DB

A full-stack web application to upload documents (CSV, JSON, Word, PowerPoint, Excel, PDF) and perform LLM-based Q&A and vector search. Includes sample code to build your own AI copilot, cache Q&A results for performance, and integrate with Azure services.

## 🚀 Features

- Vector search powered by **Azure PostgreSQL**
- In-database **OpenAI embeddings** using PostgreSQL extensions
- Use **PostgreSQL as a cache** to reduce LLM latency
- Supports data from [ARGUS Accelerator](https://github.com/Azure-Samples/ARGUS)

## 🔧 Requirements

- Python **3.11**
- Azure **OpenAI** account
- Azure **PostgreSQL** with `pgvector` or `diskann`/`hnsw` extension

## ⚙️ Setup

1. **Create and activate virtual environment:**

```bash
python -m venv .venv
.venv\Scripts\activate  # On Windows
# or
source .venv/bin/activate  # On macOS/Linux

2. **Install dependencies:**

```bash
pip install -r requirements.txt

3. **Configure environment:**
- Copy and update example.env with your keys and settings.
- Ensure PostgreSQL has the necessary extensions (diskann or hnsw).
- set the correct OpenAI models:
- One for embeddings (e.g. text-embedding-ada-002)
- One GPT model (e.g. gpt-3.5-turbo or gpt-4)

4. **Run the app:**
```bash
streamlit run pgtest.py

5. **On first login:**

- Enter a username
- Click Create Vector DB to initialize collections.

## 📁 Dataset
Sample documents are provided in the dataset/ folder. 

Enjoy building your copilot! 