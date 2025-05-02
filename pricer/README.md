# Price Prediction Models

This directory contains various implementations of price prediction models, ranging from frontier models to open-source alternatives, each with different approaches and capabilities.

## Model Implementations

### 1. Frontier Models (`frontier-pricers.ipynb`)

Implementation of state-of-the-art price prediction models using cutting-edge LLMs:

- Uses OpenAI's GPT models
- Implements advanced prompting techniques
- High accuracy but higher cost
- Real-time inference capabilities

### 2. Open Source Models (`os-pricers.ipynb`)

Open-source alternatives for price prediction:

- Implements models like Llama 3.1, Qwen 2.5, and Gemma 2
- Cost-effective solution
- Local deployment options
- Good balance of performance and resource usage

### 3. Fine-tuned Models

Two approaches to fine-tuning:

#### GPT Fine-tuning (`gpt-fine-tuned-pricers.ipynb`)

- Fine-tunes OpenAI models on custom price data
- Uses `fine_tune_train.jsonl` and `fine_tune_validation.jsonl`
- Optimized for specific price prediction tasks
- Requires API access

#### Open Source Fine-tuning (`os-fine-tuned-pricers.ipynb`)

- Fine-tunes open-source models (Llama 3.1, Qwen 2.5, etc.)
- Uses PEFT (Parameter-Efficient Fine-Tuning)
- Local training and deployment
- Cost-effective alternative to GPT fine-tuning

### 4. Classic Models (`classic-pricers.ipynb`)

Traditional machine learning approaches:

- Implements various statistical models
- Uses `train.pkl` and `test.pkl` datasets
- Fast inference times
- Good baseline performance

## Model Comparison

| Feature         | Frontier Models | Open Source Models | GPT Fine-tuned | OS Fine-tuned | Classic Models |
| --------------- | --------------- | ------------------ | -------------- | ------------- | -------------- |
| Model Type      | GPT-4/3.5       | Llama/Qwen/Gemma   | Fine-tuned GPT | Fine-tuned OS | Statistical    |
| Training Data   | General         | General            | Custom         | Custom        | Custom         |
| Inference Speed | Medium          | Fast               | Medium         | Fast          | Very Fast      |
| Accuracy        | High            | Medium-High        | Very High      | High          | Medium         |
| Cost            | High            | Low                | High           | Low           | Very Low       |
| Deployment      | Cloud           | Local/Cloud        | Cloud          | Local/Cloud   | Local          |
| Customization   | Limited         | High               | Medium         | Very High     | High           |
| Real-time       | Yes             | Yes                | Yes            | Yes           | Yes            |
| Resource Usage  | High            | Medium             | High           | Medium        | Low            |

## Supporting Files

### Data Files

- `fine_tune_train.jsonl`: Training data for fine-tuning
- `fine_tune_validation.jsonl`: Validation data for fine-tuning
- `train.pkl`: Training dataset for classic models
- `test.pkl`: Testing dataset for classic models

### Utility Files

- `tester.py`: Testing framework for model evaluation
- `loaders.py`: Data loading utilities
- `items.py`: Item class definitions and utilities
- `data_curator.ipynb`: Data preprocessing and curation notebook

## Getting Started

1. Install dependencies:

```bash
pip install -r requirements.txt
```

2. Prepare data:

```bash
python data_curator.ipynb
```

3. Choose a model implementation based on your needs:

- For highest accuracy: Use frontier models
- For cost-effectiveness: Use open-source models
- For specific domain: Use fine-tuned models
- For fast inference: Use classic models

## Requirements

- Python 3.8+
- PyTorch
- Transformers
- OpenAI API (for frontier models)
- HuggingFace Hub (for open-source models)
- Various ML libraries (requirements vary by model type)

## License

This project is licensed under the MIT License - see the LICENSE file for details.
