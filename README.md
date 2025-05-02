# LLM Engineering Journey

This repository contains my journey through LLM engineering, inspired by Ed Donner's [LLM Engineering Course](https://github.com/ed-donner/llm_engineering). The repository is organized into several key components, each representing different aspects of my learning and implementation of LLM technologies.

## Repository Structure

### 1. Pricer Models (`/pricer`)

A comprehensive collection of price prediction models, ranging from frontier models to open-source implementations:

- **Frontier Models** (`frontier-pricers.ipynb`): Implementation of state-of-the-art price prediction models
- **Open Source Models** (`os-pricers.ipynb`): Open-source alternatives for price prediction
- **Fine-tuned Models**:
  - GPT-based fine-tuning (`gpt-fine-tuned-pricers.ipynb`)
  - Open-source fine-tuning (`os-fine-tuned-pricers.ipynb`)
- **Classic Models** (`classic-pricers.ipynb`): Traditional machine learning approaches
- **Data Processing**:
  - Data curation (`data_curator.ipynb`)
  - Data loaders (`loaders.py`)
  - Item definitions (`items.py`)

### 2. Production Project (`/project`)

A production-ready framework featuring collaborative AI agents:

#### Agents Framework

- **Planning Agent** (`planning_agent.py`): Orchestrates and coordinates other agents
- **Messaging Agent** (`messaging_agent.py`): Handles communication between agents
- **Scanner Agent** (`scanner_agent.py`): Specializes in data scanning and analysis
- **Specialist Agent** (`specialist_agent.py`): Provides domain-specific expertise
- **ML-based Agents**:
  - Random Forest Agent (`random_forest_agent.py`)
  - Ensemble Agent (`ensemble_agent.py`)
- **Frontier Agent** (`frontier_agent.py`): Integrates with cutting-edge LLM models

#### Core Components

- **Framework** (`deal_agent_framework.py`): Custom framework for agent collaboration
- **Main Application** (`main.py`, `main_final.py`): Production entry points
- **Infrastructure** (`infra.ipynb`): System architecture and deployment details
- **Vector Store** (`products_vectorstore/`): Storage for product embeddings

### 3. Learning Journey (Notebooks)

A collection of Jupyter notebooks documenting my learning process:

- **Gradio Applications**:

  - Multi-AI Translation System (`gradio_multi_ai_translate.ipynb`)
  - Flight Information System (`gradio_multi_ai_flights.ipynb`)
  - Tool Integration (`gradio_with_tools.ipynb`)
  - Basic Bot Implementation (`gradio_bot.ipynb`)

- **LLM Fundamentals**:

  - Personal RAG Implementation (`Personal_RAG.ipynb`)
  - Transformer Interactions (`talk_to_transformers.ipynb`)
  - Tokenizer Studies (`tokenizers.ipynb`)
  - HuggingFace Pipelines (`hf_pipes.ipynb`)

- **Bot Development**:
  - Multi-Agent Conversations (`talking_bots.ipynb`)
  - Ollama Integration (`ollama.ipynb`)

## Inspiration

This repository is heavily inspired by Ed Donner's [LLM Engineering Course](https://github.com/ed-donner/llm_engineering). The course provided the foundation for understanding and implementing various LLM technologies, from basic concepts to advanced production systems.

## Getting Started

Each component of this repository can be explored independently:

1. For price prediction models, start with the `/pricer` directory
2. For the production agent system, explore the `/project` directory
3. For learning materials, browse through the various Jupyter notebooks

## Requirements

- Python 3.8+
- Jupyter Notebook
- Various ML and LLM libraries (requirements vary by component)

## License

This project is licensed under the MIT License - see the LICENSE file for details.
