# Context-Aware-RAG

# 🧠 Conversational RAG — Context-Aware Retrieval-Augmented Generation

[![Python](https://img.shields.io/badge/python-3.11-blue.svg)](https://www.python.org/)
[![LangChain](https://img.shields.io/badge/langchain-%F0%9F%A4%96-green)](https://docs.langchain.com/)
[![OpenAI](https://img.shields.io/badge/OpenAI-GPT--3.5/4-blueviolet)](https://openai.com/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

> A LangChain-powered framework to build multi-turn, memory-enhanced conversational agents using Retrieval-Augmented Generation (RAG).

---

## 🎯 Project Objective

Traditional RAG systems treat each user query as independent. **Conversational RAG** takes it further by integrating **memory**, **contextual input rephrasing**, and **session persistence**, enabling your AI assistant to understand follow-ups and maintain coherent conversations.

---

## 🧩 Features

- ✅ **Basic RAG Setup** — Vector store (Chroma), LLM (OpenAI), prompt template
- 🤖 **Chat History Awareness** — Understands and reformulates follow-up questions using chat memory
- 🔄 **Contextual Retrieval** — Uses `create_history_aware_retriever` to fetch better context
- 🧠 **Session Memory** — Tracks and persists conversations across user sessions using LangChain’s `RunnableWithMessageHistory`
- 💾 **.env Config** — Secure and flexible API key storage using `python-dotenv`

---

## 🛠️ Tech Stack

- Python 3.11.4 (`pyenv`, `poetry`)
- [LangChain](https://github.com/langchain-ai/langchain)
- [ChromaDB](https://www.trychroma.com/) for vector storage
- [OpenAI](https://platform.openai.com/) models (GPT-3.5/4)
- Jupyter Lab / VS Code
- `python-dotenv` for environment variables

---

## 📁 Project Structure

├── data/
│ └── be-good.txt # Sample text file to index and query
├── .env.example # Environment variables template
├── 001-conversational-rag.py # Full RAG implementation script
├── notebooks/
│ └── tutorial.ipynb # Jupyter notebook walkthrough
├── README.md # This file
└── requirements.txt / pyproject.toml





---

## ⚙️ Setup Instructions

### 🐍 Python Environment

```bash
git clone https://github.com/yourusername/conversational-rag.git
cd conversational-rag
pyenv local 3.11.4
poetry install
poetry shell


🔐 API Keys
Rename .env.example to .env

Add the following keys:

OPENAI_API_KEY=your_openai_api_key
LANGCHAIN_TRACING_V2=true
LANGCHAIN_ENDPOINT=https://api.smith.langchain.com
LANGCHAIN_API_KEY=your_langchain_api_key
LANGCHAIN_PROJECT=001-conversational-rag



🚀 Running the Project
▶️ From Notebook
bash
Copy code
jupyter lab
Open the tutorial notebook and run step-by-step.

▶️ From VS Code / Terminal
bash
Copy code
python 001-conversational-rag.py
🧠 How It Works
Step 1: Basic RAG — Use OpenAI + ChromaDB to answer questions from documents.

Step 2: Contextual Prompt — Create a ChatPromptTemplate that rewrites ambiguous user queries.

Step 3: History-Aware Retriever — Build a retriever that factors in previous chat turns.

Step 4: Conversational RAG Chain — Integrate chat memory using MessagesPlaceholder.

Step 5: Persistence — Use RunnableWithMessageHistory to track sessions (like session_id = "001").

💡 Use Cases
Chatbots that understand follow-up queries

Context-aware customer support

Conversational document Q&A

AI agents with long-term memory

📜 License
This project is licensed under the MIT License - see the LICENSE file for details.

🙌 Acknowledgements
Built using:

LangChain

OpenAI

Chroma Vector Store

📬 Contact
For suggestions, questions, or feedback: your-email@example.com

vbnet
Copy code

Let me know if you’d like me to:
- Add Markdown rendering of architecture diagrams.
- Create a walkthrough GIF/demo.
- Publish it to HuggingFace Spaces or Streamlit.

Just drop the project folder name and GitHub repo name if you'd like it cu
