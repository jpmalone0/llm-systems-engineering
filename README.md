# LLM Systems Engineering Portfolio

A collection of practical implementations demonstrating different LLM system architectures: Retrieval-Augmented Generation (RAG), Fine-Tuning (PEFT/LoRA), and Agentic Workflows.

## Project Structure

| Project | Type | Description |
| :--- | :--- | :--- |
| **Chess RAG** | Retrieval-Augmented Generation | A RAG system that answers questions about chess openings using a vector database (FAISS) and Semantic Search. |
| **DialogSum LoRA** | Fine-Tuning (QLoRA) | Parameter-Efficient Fine-Tuning of a generic LLM (TinyLlama) to perform dialogue summarization using the DialogSum dataset. |
| **Weather Agent** | Agentic Workflow | An autonomous agent capable of tool calling (function calling) to fetch real-time weather data and reason about it. |

## Tech Stack

* **Language:** Python 3.11
* **Manager:** uv
* **Core Libraries:** torch, transformers, peft, bitsandbytes, langchain, google-generativeai

## Quick Start

This project uses **uv** for dependency management to ensure a reproducible environment.

### 1. Clone & Setup

```bash
# Clone the repository
git clone https://github.com/jpmalone0/llm-systems-engineering.git
cd llm-systems-engineering
# Install dependencies (creates .venv automatically)
uv sync
```

### 2. Configure Environment

Create a `.env` file in the root directory to store your API keys:

```bash
touch .env
```

Add your keys to `.env`:

```Ini,TOML
GOOGLE_API_KEY=your_gemini_api_key_here
HF_TOKEN=your_huggingface_token_here
```
### 3. Run the Notebooks

Open the notebooks in VS Code or Jupyter Lab. Ensure you select the kernel named "Python (llm-systems-engineering)" or point to the .venv folder.

RAG: rag/chess_rag.ipynb

Fine-Tuning: fine-tuning-qlora/lora-dialogsum.ipynb

Agent: agentic-workflow/weather-agent.ipynb
