# E-Commerce-AI-Support-Bot

An AI-powered customer support assistant for e-commerce platforms built with Python, Flask, LangChain, Hugging Face, and FAISS. It handles natural language queries about products, orders, and policies, delivering context-aware responses through semantic search and retrieval-augmented generation.

## Project Overview

This project implements an intelligent customer support assistant using:

- **LLM**: Flan-T5-Base (HuggingFace)
- **RAG**: FAISS vector store with sentence-transformer embeddings
- **Backend**: Flask + LangChain
- **Frontend**: Interactive HTML5 chat widget

## Features

### Core Capabilities

- Order tracking with status updates
- Return/exchange request processing
- Refund policy explanations
- Payment issue resolution
- Product and delivery information via RAG
- Intent classification and routing
- Conversation memory (multi-turn)
- Escalation to human agents

### Safety & Quality

- Input validation and sanitization
- Sensitive data protection
- Hallucination prevention
- Clear fallback handling
- Conversation logging for evaluation

## Installation

### Prerequisites

- Python 3.9.13
- pip
- Virtual environment (recommended)

### Setup

`git clone <your-repo-url>`
`cd ecommerce-assistant`

### Create virtual environment

`conda create -n myenvname python=3.9.13`
`conda activate ecommerce-genai`

### Install dependencies

`pip install -r requirements.txt`

### Run the application

`python -m backend.app`
`The bot will be available at: `http://localhost:5000`

### RAG Pipeline

1. **Documents**: 50+ e-commerce FAQs and policies
2. **Embeddings**: Sentence-BERT (all-MiniLM-L6-v2)
3. **Vector Store**: FAISS (in-memory)
4. **Retrieval**: Top-5 documents per query
5. **Generation**: Flan-T5-Base with system prompt

### Example Queries to Demo in Presentation

- **Greetings & help**

  - `Hi`
  - `Help`
  - `What can you do?`

- **Order tracking**

  - `Where is my order ORD123?`
  - `Track my order ORD456`
  - `Order status for ORD789`

- **Returns & refunds**

  - `I want to return order ORD789`
  - `Can I exchange my order ORD456?`
  - `Tell me about your refund policy`

- **Payments**

  - `My payment failed`
  - `I was charged twice for my order`
  - `UPI payment issue while placing order`

- **Discounts & products**

  - `Tell me about discounts and offers`
  - `Help me find a product`
  - `Do you have wireless headphones in stock?` (if product availability logic is added)

- **Escalation / critical issues**
  - `My order was delivered but items are missing`
  - `I'm very frustrated with your service`
  - `Courier is not responding for my delivery`

### 6.3 Interacting with the Bot

Open a browser and go to `http://127.0.0.1:5000`.  
Use the chat widget to try prompts like:

- `Hi`
- `Where is my order ORD123?`
- `I want to return order ORD789 because it arrived damaged`
- `Tell me your refund policy`
- `My payment failed but money was deducted`
- `I was charged twice for my order`
- `Tell me about discounts and offers`
- `I think courier is not responding and my items are missing`

## Conclusion

This project implements a complete **E‑Commerce AI Support Bot** using modern NLP tools and a RAG architecture. It demonstrates how a combination of:

- Rule‑based intent routing,
- Mock transactional tools, and
- Retrieval‑based QA over a curated knowledge base

can deliver a practical, extensible customer support assistant.  
The solution is suitable as a capstone project, showcasing both software engineering discipline and applied AI capabilities in a realistic e‑commerce scenario.

## Author

Abhilash
