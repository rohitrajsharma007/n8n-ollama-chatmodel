# 🤖 n8n + Ollama Local AI Chatbot

This project demonstrates how to run **n8n** locally and connect it with **Ollama** to use **local LLM models** (like TinyLlama / Llama3) for AI chat workflows.

No cloud. No API keys. Fully local 🚀

---

## 🧩 Architecture Overview



User → n8n Workflow → Ollama (Local LLM)


- **n8n** → Automation & workflow engine  
- **Ollama** → Runs AI models locally  
- **HTTP / AI Agent Node** → Connects n8n with Ollama  

---

## ✅ Prerequisites

- Windows 10 / 11  
- Node.js (v18 or later)  
- npm  
- Internet (only for first-time installs)

---

## 🔹 Step 1: Install Ollama (Windows)

Download and install Ollama:

👉 https://ollama.com/download/windows

Verify installation:
```bash
ollama --version


Pull a model (example: TinyLlama):

ollama pull tinyllama


Test model:

ollama run tinyllama


Ollama runs on:

http://localhost:11434

🔹 Step 2: Install n8n Locally

Install n8n globally using npm:

npm install -g n8n


Verify installation:

n8n --version


Start n8n:

n8n


Open n8n in browser:

http://localhost:5678

🔹 Step 3: Create n8n Workflow

Open n8n UI

Click Create Workflow

Add Chat Trigger (or Webhook for API-based chat)

Add AI Agent node

Add Ollama Chat Model

🔹 Step 4: Configure Ollama Chat Model
Connection Settings

Base URL:

http://localhost:11434


(Use http://host.docker.internal:11434 if n8n runs in Docker)

Model Name:

tinyllama


or

llama3

🔹 Step 5: Connect AI Agent

Attach Chat Trigger → AI Agent

Select Ollama Chat Model inside AI Agent

Set system prompt (optional):

You are a helpful AI assistant.

🔹 Step 6: Test the Workflow

Click Chat

Ask a question:

Explain n8n like I am 10 years old


You should receive a response from the local AI 🎉


Check Ollama is running:

ollama list


Verify port:

11434

🧠 Supported Models

tinyllama

llama3

mistral

codellama

phi

(Any model supported by Ollama)

🚀 Use Cases

Local ChatGPT-style chatbot

AI-powered automation

Internal company AI assistant

Privacy-first GenAI workflows

RAG pipelines (future)

📌 Status

✅ Ollama installed
✅ n8n installed
✅ Workflow created
✅ AI Agent connected
🚧 Advanced features in progress (RAG, memory, tools)

👨‍💻 Author

Rohit Sharma
GenAI | Automation | Backend
