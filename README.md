🧑‍⚖️ Road Sathi (Motor Vehicles Act, India)
An AI-powered legal assistant built using n8n + Pinecone + Gemini/OpenAI + Telegram, designed to provide real-time, situation-based legal guidance using Retrieval-Augmented Generation (RAG).

🚀 Overview

This project creates a Telegram-based legal chatbot that:
Answers user queries related to the Motor Vehicles Act, 1988
Uses Pinecone vector database to retrieve legal context
Provides practical, actionable legal guidance (not textbook answers)
Adapts response length based on user situation

🧠 Architecture

🔹 User Flow
User sends message via Telegram
AI agent processes query
Relevant legal context retrieved from Pinecone
LLM generates answer using {context}
Response sent back to Telegram

🔹 Workflow Components
1. Telegram Trigger
Captures incoming user messages
Extracts user query

2. Question & Answer Chain
Core AI brain
Uses:
Gemini Chat Model
Vector Retriever
Injects {context} from Pinecone

3. Vector Store Retriever
Fetches relevant legal chunks

4. Pinecone Vector Store
Stores embedded legal documents

5. Embeddings (OpenAI)
Converts documents into vectors

6. Telegram Output
Sends final response to user

📂 Document Ingestion Pipeline

Automated pipeline to update legal knowledge:
Upload file to Google Drive folder
Trigger activates automatically
File downloaded
Converted into embeddings
Stored in Pinecone

⚙️ Tech Stack

n8n – Workflow automation
Telegram API – Chat interface
Google Gemini / OpenAI – LLM
Pinecone – Vector database
OpenAI Embeddings – Text vectorization
Google Drive – Document storage

🎯 Key Features

✅ Real-time legal Q&A
✅ Context-aware answers using RAG
✅ Short, situation-based responses
✅ No hallucination (context-first approach)
✅ Auto document indexing pipeline
✅ Telegram chatbot interface

🧩 Prompt Design (Core Intelligence)

The AI is designed to:
Act like a professional lawyer
Give direct, actionable solutions
Avoid long structured answers
Use {context} as source of truth

If no context found:
"I searched the available legal information but could not find specific details on this."

🛑 Safety & Constraints

No hallucinated legal sections
No guaranteed outcomes
No absolute legal advice
Always includes:
"This is general legal guidance—consult a lawyer for your specific case."

🔧 Setup Instructions

Import workflow into n8n
Connect credentials:
Telegram API
OpenAI API
Pinecone API
Google Drive API
Create Pinecone index (legal-doc-1)
Upload legal documents (Motor Vehicles Act PDFs)
Activate workflow
Test via Telegram

📌 Example Queries

"My licence expired yesterday, can I drive?"
"Accident ho gaya, what should I do?"
"Fine for driving without helmet?"
"How to claim insurance after accident?"

📈 Future Improvements

🔁 Multi-agent system (Legal + FIR + Compensation)
📊 Compensation calculator
🧾 FIR / complaint generator
🧠 Conversation memory
🌐 Web dashboard
📎 Workflow File

You can find the full n8n workflow here:


🧑⚖️ Ai legal assistant agent —…

⚠️ Disclaimer

This system provides general legal information only and is not a substitute for professional legal advice.
