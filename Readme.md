# Advanced Prompt Engineering & Model Fine-Tuning Comparison

## Project Overview
This project implements two approaches to leverage language models for legal document analysis:
1. **Task 1**: Advanced Prompt Engineering System for legal clause analysis
2. **Task 2**: Comparative analysis between fine-tuning and prompt engineering

![Workflow Diagram](placeholder_workflow_diagram.png)
### System Architecture
```mermaid
graph TD
    Z[Model Comparison Workflow] --> A[Base DistilBERT]
    Z --> Y[Raw IMDb Dataset]
    Y --> X[Data Preprocessing]
    X -->|Train/Test Split<br>Tokenization| C[Fine-tuning Process]
    C -->|3 epochs<br>Batch size 8| E[Fine-tuned Model]
    A --> B[Prompt Engineering]
    B -->|Zero-shot<br>Few-shot| D[Base Model Predictions]
    E --> F[Fine-tuned Predictions]
    D --> G[Comparative Analysis]
    F --> G
    G -->|Accuracy/F1 Scores<br>Inference Speed<br>Resource Needs| H[Deployment Scenario]
    
    subgraph " "
    A
    Y
    end
    
    subgraph " "
    B
    C
    end
    
    subgraph " "
    D
    E
    end
    
    subgraph " "
    G
    H
    end
    
    style Z fill:#f5f5f5,stroke:#333,stroke-width:2px
    style H fill:#e6f7ff,stroke:#1890ff
    style G fill:#f6ffed,stroke:#52c41a <!-- Replace with your diagram -->

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
    A[User Input] --> B(Document Preprocessing)
    B --> C[Chain-of-Thought Analysis]
    C --> D[Few-Shot Learning]
    D --> E[Red Flag Detection]
    E --> F[Report Generation]
    F --> G[User Output]