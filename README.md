# 🤖 SmartAgent-QA-Bot

This is a hybrid AI chatbot that intelligently routes user questions to either a custom document vectorstore or Wikipedia search based on the topic. Built using **LangGraph**, **Groq's LLaMA 3**, **AstraDB**, and **Gradio**, it delivers fast, context-aware answers via a clean chatbot UI.

## 🚀 Features

- 🧠 **LangGraph-powered flow** with conditional routing
- 🔎 **RAG-enabled** via AstraDB vectorstore (Cassandra)
- 🌐 **Fallback to Wikipedia** for general knowledge queries
- ⚡ Powered by **Groq's LLaMA 3.3-70B**
- 🎨 Interactive frontend using **Gradio**

## 🛠️ Tech Stack

- `LangGraph` — LLM routing and workflow engine  
- `LangChain` — retrieval, loading, and chaining  
- `Groq` — fast LLaMA-3 based LLMs  
- `AstraDB` — vectorstore for document indexing  
- `Gradio` — chatbot UI  
- `WikipediaAPIWrapper` — external fallback knowledge base  

## 💡 Use Case

This chatbot can be used to:
- Query indexed technical documentation
- Fallback to Wikipedia when questions go beyond the scope
- Build intelligent LLM apps with custom + public knowledge

## 🧪 Live Demo

Check out the live version here on Hugging Face Spaces:  
🔗 [SmartAgent-QA-Bot](https://huggingface.co/spaces/anj12-sh/SmartAgent-QA-Bot)

## 📁 Project Structure

```bash
├── app.py               # Main app logic
├── requirements.txt     # All dependencies
├── .env.example         # Template for your environment variables
└── README.md            # Project documentation (you are here!)



🧠 How It Works

User submits a question.
The router model decides: vectorstore or Wikipedia.
If vectorstore:
Uses AstraDB to retrieve chunks
If Wikipedia:
Uses WikipediaAPIWrapper to search & extract content
A final answer is generated using Groq's LLM.
Displayed in a Gradio chatbot UI.


📜 License
MIT License – Free to use, modify, and share.

