<div align="center">

# 🔮 LangGraph Agentic AI

Learning and prototyping agentic AI workflows with LangGraph — chatbots, graph state, and human-in-the-loop patterns.

</div>

---

## Overview

`langraphagenticai` is a hands-on LangGraph learning project covering:

- Building a basic chatbot with LangGraph's Graph API
- Core LangGraph components — **Nodes**, **Edges**, and **State**
- Human-in-the-loop workflows
- Multi-provider LLM support (Groq, Google Gemini) with Tavily web search and LangSmith tracing

## Project Structure

```
langraphagenticai/
├── 1-BasicChatbot/
│   ├── basicchatbot.ipynb       # Basic chatbot built with the LangGraph Graph API
│   └── humanintheloop.ipynb     # Human-in-the-loop workflow
├── src/
│   └── langraphagenticai/
│       └── __init__.py
├── .env                          # API keys (gitignored)
├── .python-version
├── pyproject.toml
├── requirements.txt
└── uv.lock
```

> The `src/langraphagenticai` package is currently a skeleton — active work lives in the `1-BasicChatbot` notebooks.

## Installation

```bash
git clone https://github.com/DheerajChavan23/langraphagenticai.git
cd langraphagenticai

uv venv
source .venv/bin/activate   # macOS/Linux
.venv\Scripts\activate      # Windows

uv pip install -r requirements.txt
```

Requires Python ≥3.13.

## Environment Variables

Create a `.env` file in the project root:

```
GROQ_API_KEY="your_key"
GOOGLE_API_KEY="your_key"
TAVILY_API_KEY="your_key"
LANGSMITH_API_KEY="your_key"
```

⚠️ Already in `.gitignore` — safe from accidental commits.

## Running

Open the notebooks in Jupyter (via `ipykernel`, already included):

```bash
jupyter notebook 1-BasicChatbot/basicchatbot.ipynb
```

## Basic Chatbot — Core Concepts

The `basicchatbot.ipynb` notebook builds a chatbot using LangGraph's Graph API, structured around three core components:

1. **Nodes** — units of work (e.g. calling the LLM)
2. **Edges** — connections that define the flow between nodes
3. **State** — the shared data passed through the graph as it runs

## Dependencies

`langchain` · `langgraph` · `langsmith` · `langchain-groq` · `langchain-google-genai` · `langchain-tavily` · `python-dotenv` · `ipykernel`

## Roadmap

- [ ] Build out `src/langraphagenticai` into a reusable package
- [ ] Multi-agent workflows
- [ ] Memory-enabled conversational agents
- [ ] FastAPI wrapper for agent endpoints
- [ ] RAG pipeline with FAISS / Chroma
- [ ] CLI interface

## Contributing

Contributions welcome — open an issue for bugs, feature requests, or documentation improvements.

## License

MIT License — free to use, modify, and distribute.
