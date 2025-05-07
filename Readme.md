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
%%{init: {'theme': 'base', 'themeVariables': { 'primaryColor': '#ffd8d8', 'edgeLabelBackground':'#ffffff'}}}%%
flowchart TD
    A[User Input] --> B{Document Preprocessing}
    B -->|Clean Text| C[Chain-of-Thought Analysis]
    B -->|Edge Case Detected| Z[Handle Edge Case]
    C --> C1[Identify Document Type]
    C --> C2[Extract Key Sections]
    C --> C3[Analyze Clause Implications]
    C1 --> D[Few-Shot Learning Application]
    C2 --> D
    C3 --> D
    D --> D1[Apply Learned Examples]
    D --> D2[Generate Formatted Output]
    D --> D3[Enforce JSON Structure]
    D --> E[Red Flag Detection]
    E --> E1[Unusual Terms]
    E --> E2[One-Sided Clauses]
    E --> E3[Regulatory Risks]
    E --> F[Report Generation]
    F --> F1[Executive Summary]
    F --> F2[Risk Assessment]
    F --> F3[Recommended Actions]
    F --> G[User Output]
    G --> G1[Markdown Report]
    G --> G2[Term Explanations]
    G --> G3[Red Flag Alerts]
    
    %% Style Definitions
    classDef user fill:#e1f5fe,stroke:#039be5;
    classDef process fill:#e8f5e9,stroke:#43a047;
    classDef analysis fill:#fff3e0,stroke:#fb8c00;
    classDef output fill:#f3e5f5,stroke:#8e24aa;
    class A,G1,G2,G3 user;
    class B,Z,D,E,F process;
    class C,C1,C2,C3,D1,D2,D3,E1,E2,E3 analysis;
    class F1,F2,F3 output;
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

