# RAG Document Q&A with Groq and Llama 3

**A Streamlit-based Retrieval-Augmented Generation (RAG) application for chatting with PDF research papers using Groq's ultra-fast Llama 3 model.**

This project allows users to upload research papers, generate embeddings, store them in a FAISS vector database, and ask questions in natural language. It supports both **OpenAI Embeddings** and **free Hugging Face Embeddings**, giving flexibility between premium and open-source options.

---

## Features

- **PDF Document Ingestion**  
  Automatically loads and processes research papers from a local folder.

- **Text Chunking**  
  Uses LangChain's `RecursiveCharacterTextSplitter` for efficient document splitting.

- **Vector Search with FAISS**  
  Fast similarity search for retrieving relevant document context.

- **Dual Embedding Support**
  - **OpenAI Embeddings** (`main.py`)
  - **Hugging Face Embeddings** (`app_huggingfaceembedding.py`) using `all-MiniLM-L6-v2`

- **Fast LLM Inference**  
  Powered by **Groq Cloud** using `Llama3-8b-8192`.

- **Source Transparency**  
  Displays retrieved source chunks alongside generated answers.

- **Interactive Web Interface**  
  Built with Streamlit for easy document Q&A.

---

## Tech Stack

- Python  
- Streamlit  
- LangChain  
- Groq API  
- Llama 3  
- FAISS  
- OpenAI Embeddings  
- Hugging Face Embeddings  
- PyPDF  
- python-dotenv  

---

## Project Structure

```bash
RAG-Document-QA/
├── research_papers/
├── .env
├── main.py
├── app_huggingfaceembedding.py
└── README.md
```

---

## Installation

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/RAG-Document-QA.git
cd RAG-Document-QA
```

---

### 2. Create Virtual Environment

```bash
python -m venv venv
```

Activate it:

**Windows**
```bash
venv\Scripts\activate
```

**Mac/Linux**
```bash
source venv/bin/activate
```

---

### 3. Install Dependencies

```bash
pip install streamlit langchain langchain-groq langchain-openai langchain-community langchain-huggingface faiss-cpu pypdf python-dotenv
```

---

### 4. Configure Environment Variables

Create a `.env` file and add your API keys:

```env
GROQ_API_KEY=your_groq_api_key_here
OPENAI_API_KEY=your_openai_api_key_here
HF_TOKEN=your_huggingface_token_here
```

**Note:**
- `OPENAI_API_KEY` is required only for `main.py`
- `HF_TOKEN` is required only for `app_huggingfaceembedding.py`

---

## Run the Application

### Step 1: Add Research Papers

Create a folder named `research_papers` and place your PDF files inside:

```bash
mkdir research_papers
```

---

### Step 2: Start Streamlit App

Choose your preferred embedding option.

**Option A: OpenAI Embeddings**

```bash
streamlit run main.py
```

**Option B: Hugging Face Embeddings (Free)**

```bash
streamlit run app_huggingfaceembedding.py
```

---

### Step 3: Use the Application

Open the Streamlit URL (usually):

```bash
http://localhost:8501
```

Then:

1. Click **Document Embedding**
2. Wait for **Vector Database is ready**
3. Enter your question
4. View generated answer and retrieved document context

---

## Example Questions

- Summarize this research paper
- What are the key findings?
- Explain the methodology used
- What conclusions were drawn?

---

## Why This Project Matters

This project demonstrates practical experience in:

- Retrieval-Augmented Generation (RAG)
- Vector Databases (FAISS)
- LLM Integration
- Streamlit App Development
- LangChain Pipelines
- Prompt Engineering

---


