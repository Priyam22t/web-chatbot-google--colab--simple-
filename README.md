# RAG Chatbot using LangChain, Pinecone & HuggingFace

This project is a full end-to-end Retrieval-Augmented Generation (RAG) chatbot that allows users to chat with their own data. It uses Pinecone as a vector database, LangChain for orchestration, and HuggingFace open-source models for embeddings and text generation. The project is designed to run smoothly on Google Colab and is fully GitHub-ready.

---

## 🚀 Features

- Load data directly from URLs  
- Intelligent text chunking with overlap  
- Semantic embeddings using Sentence Transformers  
- Vector storage using Pinecone (serverless compatible)  
- Similarity search for relevant context retrieval  
- Retrieval-Augmented Generation (RAG) chatbot  
- Uses open-source LLMs (no OpenAI required)  
- Google Colab compatible  
- Clean, production-style code  

---

## 🧱 Architecture Overview

1. Data Ingestion – Load web content using UnstructuredURLLoader  
2. Text Splitting – Break content into overlapping chunks  
3. Embeddings – Convert text into 1024-dimensional vectors  
4. Vector Database – Store vectors in Pinecone  
5. Retrieval – Fetch top-k relevant chunks for a query  
6. Generation – Use an LLM to answer based on retrieved context  

---

## 📦 Tech Stack

- Python  
- LangChain (community)  
- Pinecone (Vector Database)  
- HuggingFace Transformers  
- Sentence-Transformers  
- TinyLlama / other open-source LLMs  
- Google Colab  

---

## ⚙️ Setup Instructions (Google Colab)

1. Open Google Colab  
2. Upload `full_rag_pinecone_colab.ipynb`  
3. Run the dependency installation cell  
4. Paste your Pinecone API key and index host  
5. Run all cells in order  

---

## 🔐 Required Configuration

Inside the notebook, update:

```python
os.environ["PINECONE_API_KEY"] = "YOUR_API_KEY"
INDEX_HOST = "YOUR_INDEX_HOST"
⚠️ Never commit API keys to public repositories.

💬 How to Use
After running all cells, start chatting with your data:

vbnet
Copy code
You: What is Pinecone?
Bot: Pinecone is a vector database used for storing embeddings...
Type exit to stop the chatbot.

📁 Recommended Repository Structure
Copy code
rag-chatbot/
├── full_rag_pinecone_colab.ipynb
├── README.md
└── requirements.txt
🧠 Use Cases
Chat with website content

Knowledge base assistants

AI-powered documentation bots

Research assistants

Educational chatbots

🛠️ Future Improvements
Streamlit or Web UI

PDF upload support

Chat history and memory

FastAPI backend

Cloud deployment (AWS, GCP, Render)

