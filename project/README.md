# The Price is Right - Autonomous Deal Hunting Agent Framework

This project implements a production-ready autonomous agent framework that collaborates to find and analyze online deals. The system combines a proprietary fine-tuned LLM deployed on Modal with a RAG pipeline using frontier models and Chroma for vector storage.

## Project Structure

### Agents (`/agents`)

Production-level agents that work together in the deal hunting framework:

- **Planning Agent** (`planning_agent.py`): Orchestrates the overall strategy and coordinates other agents
- **Messaging Agent** (`messaging_agent.py`): Handles communication and notifications between agents
- **Scanner Agent** (`scanner_agent.py`): Specializes in scanning and analyzing online deals
- **Specialist Agent** (`specialist_agent.py`): Provides domain-specific expertise for deal evaluation
- **ML-based Agents**:
  - Random Forest Agent (`random_forest_agent.py`): Implements ML-based price prediction
  - Ensemble Agent (`ensemble_agent.py`): Combines multiple prediction models
- **Frontier Agent** (`frontier_agent.py`): Integrates with cutting-edge LLM models
- **Base Agent** (`agent.py`): Core agent implementation and interfaces

### Sample Applications (`/sample`)

Example applications and implementations:

- **Pricer** (`pricer.py`): Sample price prediction implementation
- **Ollama Integration** (`ollama.py`): Example of Ollama model integration
- **Hello World** (`hello.py`): Basic application template

### Utilities (`/utils`)

Supporting utilities for the framework:

- **Keep Warm** (`keep_warm.py`): Utility for maintaining service availability
- **Testing** (`testing.py`): Testing utilities and helpers

### Core Components

- **Framework** (`deal_agent_framework.py`): Custom framework for agent collaboration and orchestration
- **Entry Points**:
  - `main.py`: Initial implementation with basic Gradio interface
  - `main_final.py`: Enhanced production version with logging and visualization

### Data Storage

- **Vector Store** (`products_vectorstore/`): Chroma-based storage for product embeddings
- **Model Files**:
  - `ensemble_model.pkl`: Serialized ensemble model
  - `random_forest_model.pkl`: Serialized random forest model
  - `train.pkl`, `test.pkl`: Training and testing datasets

## Entry Points Comparison

| Feature          | `main.py`   | `main_final.py`                      |
| ---------------- | ----------- | ------------------------------------ |
| UI Framework     | Gradio      | Gradio                               |
| Auto-refresh     | 60 seconds  | 300 seconds                          |
| Logging          | Basic       | Advanced with queue-based logging    |
| Visualization    | None        | 3D scatter plot of vector embeddings |
| Error Handling   | Basic       | Enhanced with threading              |
| State Management | Simple      | Advanced with state persistence      |
| UI Elements      | Basic table | Enhanced table with logs and plots   |
| Performance      | Standard    | Optimized with background processing |

## Learning Journey

The `infra.ipynb` notebook documents the development journey and implementation details of the project, including:

- System architecture design
- Agent framework development
- Model integration strategies
- Performance optimization
- Deployment considerations

## Getting Started

1. Install dependencies:

```bash
pip install -r requirements.txt
```

2. Run the application:

```bash
python main_final.py
```

3. Access the web interface at `http://localhost:7860`

## Requirements

- Python 3.8+
- Gradio
- ChromaDB
- Plotly
- Various ML libraries (requirements vary by component)

## License

This project is licensed under the MIT License - see the LICENSE file for details.
