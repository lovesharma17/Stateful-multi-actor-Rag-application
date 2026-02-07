# Multi-Agent RAG Application

**Advanced multi-agent Retrieval-Augmented Generation (RAG) system** that intelligently decomposes queries, retrieves relevant information from multiple sources, and generates accurate, context-rich responses using collaborative AI agents.

Built with modern GenAI stack — perfect for research, Q&A bots, knowledge assistants, or any application requiring up-to-date and grounded reasoning.

## 🌟 Key Features

- **Multi-Agent Architecture** — Specialized agents collaborate to plan, retrieve, reason, and synthesize answers
- **Lightning-fast LLM** — Powered by Meta's **Llama-3.1-8B-Instruct** via **Groq** inference ( blazing inference speed! ⚡)
- **Vector Database** — **Astra DB** (serverless Cassandra-based vector store) for scalable, production-ready embeddings storage
- **High-quality Embeddings** — **Hugging Face Sentence Transformers** (`all-MiniLM-L6-v2` or similar — fast & effective)
- **External Knowledge Tools**:
  - **Web-based loader** — Fetch and process real-time content from URLs
  - **Wikipedia Scraper** — Pull structured, reliable information from Wikipedia
- **Production-ready patterns** — Modular design, error handling, retry logic, and easy extensibility

## 🛠️ Tech Stack

- **LLM**                  : Llama-3.1-8B-Instant (Groq API)
- **Orchestration**       : LangChain / LangGraph (multi-agent workflows)
- **Vector Store**        : Astra DB
- **Embeddings**          : sentence-transformers (Hugging Face)
- **Document Loaders**    : Web loader + Custom Wikipedia scraper
- **Python**              : 3.10+

## 🚀 Quick Start

```bash
# 1. Clone the repo
git clone https://github.com/YOUR-USERNAME/multi-agent-rag-app.git
cd multi-agent-rag-app

# 2. Install dependencies
pip install -r requirements.txt

# 3. Set environment variables (create .env file)
GROQ_API_KEY=your_groq_key
ASTRA_TOKEN=your_astra_token
ASTRA_DB_ID=your_db_id
ASTRA_COLLECTION=your_collection_name

# 4. Run the app / demo
python main.py --query "What is the latest on quantum computing breakthroughs?"
# or
streamlit run app.py    # if you have a Streamlit UI
