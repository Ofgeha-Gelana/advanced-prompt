# Advanced Prompt Engineering & Model Fine-Tuning Comparison

## Project Overview

This project explores and evaluates two methodologies for leveraging language models in legal document analysis:

1. **Task 1**: An **Advanced Prompt Engineering** system designed for legal clause analysis using chain-of-thought reasoning and few-shot learning techniques.
2. **Task 2**: A **comparative study** of performance between **prompt engineering** and **fine-tuning** approaches for text classification tasks.

---

## Table of Contents
- [Task 1: Advanced Prompt Engineering](#task-1-advanced-prompt-engineering)
- [Task 2: Model Comparison](#task-2-model-comparison)
- [Installation](#installation)
- [Usage](#usage)
- [Results](#results)
- [Deployment Recommendations](#deployment-recommendations)
- [Contributing](#contributing)

---

## Task 1: Advanced Prompt Engineering

### System Architecture

```mermaid
graph TD
    A[User Input] --> B[Document Preprocessing]
    B --> C[Chain-of-Thought Analysis]
    C --> D[Few-Shot Learning]
    D --> E[Red Flag Detection]
    E --> F[Report Generation]
    F --> G[User Output]
```

This pipeline enables modular, interpretable clause-level legal analysis using large language models (LLMs) without the need for model retraining.

---

## Task 2: Model Comparison

### Experimental Design

```mermaid
graph LR
    A[Base Model] --> B[Prompt Engineering]
    A --> C[Fine-tuning]
    B --> D[Prediction]
    C --> E[Prediction]
    D --> F[Comparison]
    E --> F
    F --> G[Analysis]
```

The objective is to empirically evaluate the trade-offs in accuracy, cost, latency, and scalability between prompt-based and fine-tuned model approaches for legal text classification.

---

## Installation

1. Clone the repository:

```bash
git clone https://github.com/Ofgeha-Gelana/advanced-prompt.git
cd advanced-prompt
```

2. Create a virtual environment and install dependencies:

```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
pip install -r requirements.txt
```

3. (Optional) If using GPU support:

```bash
pip install torch torchvision torchaudio --extra-index-url https://download.pytorch.org/whl/cu118
```

---

## Usage

### Run Task 1 (Prompt Engineering):
```bash
python usecase.ipynb and second_usecase.ipynb
```

### Run Task 2 (Model Comparison):
```bash
python finetuned-vs-prompt.ipynb and evaluation.ipynb
```

Results will be saved to the `outputs/` directory.

---

## Results

| Approach          | Accuracy | Inference Time | Model Size | Notes                       |
|-------------------|----------|----------------|------------|-----------------------------|
| Prompt Engineering| 87.5%    | ~300ms         | 500MB      | No training required        |
| Fine-Tuned Model  | 91.2%    | ~120ms         | 420MB      | Requires labeled dataset    |


---

## Deployment Recommendations

- **Prompt Engineering** is recommended for:
  - Rapid prototyping
  - Resource-constrained environments
  - Scenarios with frequent domain shifts

- **Fine-Tuning** is recommended for:
  - High-accuracy production systems
  - Static or narrow legal domains
  - High-throughput inference needs

---

