
# 📘 MistralRAG — Lightweight RAG System with LangChain, Mistral-7B, and Hugging Face

**MistralRAG** is an open-source, end-to-end **Retrieval-Augmented Generation (RAG)** pipeline using **LangChain**, **Hugging Face Transformers**, and **Mistral-7B**, designed for fast, local, and structured document-based Q&A.

Built to process, index, and semantically query **US Census Reports** and other domain-specific PDFs — with 100% open models.

---

## 🚀 Key Features

- 🧠 RAG powered by **Mistral-7B (HF Hub)** + SentenceTransformers
- 📄 **PDF ingestion** using LangChain + PyPDFLoader
- 🧱 **Vector indexing** via FAISS
- 🧮 Custom **RetrievalQA chains** with template prompts
- 📝 Summarization-ready + fine-tune compatible outputs

---

## 🧩 Tech Stack

| Component        | Technology Used                        |
|------------------|-----------------------------------------|
| LLM Backend      | Hugging Face `mistralai/Mistral-7B-Instruct-v0.1` |
| Orchestration    | LangChain                               |
| Vector Search    | FAISS + SentenceTransformers            |
| PDF Loader       | PyPDFLoader                             |
| Chunking Logic   | RecursiveTextSplitter                   |
| Embedding Model  | `sentence-transformers/all-MiniLM-L6-v2`|

---

## 📂 How It Works

1. 📥 **Upload PDF**: US Census documents or any domain PDFs  
2. 📎 **Chunk & Embed**: Documents are split + embedded using SBERT  
3. 🔍 **Vector Search**: Top-k chunks retrieved using FAISS  
4. ✍️ **RAG Prompt**: Mistral-7B invoked with context-aware prompt  
5. 📤 **Answer Output**: Streaming or printed natural language response

---

## 🛠️ Getting Started

### 1. Clone the repo
```bash
git clone https://github.com/arunkatika/mistral-rag.git
cd mistral-rag
````

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Pull the Mistral model

```bash
from transformers import pipeline
pipeline("text-generation", model="mistralai/Mistral-7B-Instruct-v0.1")
```

### 4. Run the RAG chain

```python
from rag_chain import qa_chain
qa_chain.run("What is the purpose of the American Community Survey?")
```

---

## 📎 Example Documents

* `acsbr-015.pdf`
* `acsbr-016.pdf`
* `acsbr-017.pdf`
* `p70-178.pdf`

You can replace these with your own custom PDFs.

---

## 🧪 Use Cases

* 📊 US Census Data Q\&A
* 🏛️ Government or Legal Document Analysis
* 📚 Academic Paper Summarization
* 🧠 Lightweight Local RAG Demos

---

## 🧑‍💻 Author

**Arun Kumar Reddy Katika**
[LinkedIn](https://linkedin.com/in/arunkatika) · [GitHub](https://github.com/arunkatika)

---

