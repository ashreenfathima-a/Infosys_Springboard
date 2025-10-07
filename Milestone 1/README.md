# Infosys CodeGenie Project – Milestone 1: Code Explainer

## Project Overview

This milestone is part of the **Infosys CodeGenie – AI Explainer and Code Generator Project**. The objective of this stage is to build a **Code Explainer pipeline** that can analyze Python code snippets, extract their structure, and generate meaningful embeddings using advanced NLP models.

This milestone forms the foundation for a larger system that will later use **Retrieval-Augmented Generation (RAG)** to provide context-aware explanations for entire codebases.

---

## Objective

The goals of this milestone are:

* Prepare a set of Python code snippets for analysis.
* Parse each snippet using **Abstract Syntax Tree (AST)** to understand its components and hierarchy.
* Tokenize the code for model-based analysis.
* Generate embeddings using three pretrained transformer models:

  * MiniLM
  * DistilRoBERTa
  * CodeBERT
* Compare the models by visualizing similarities using **heatmaps** and **t-SNE plots**.

---

## Problem Statement

Existing AI-based code assistants are capable of understanding general programming concepts, but they often fail to provide accurate explanations for specific project-level code.

* **Limitation:** These models lack awareness of the local codebase and often provide generic or incorrect explanations.
* **Solution:** Develop an AI system capable of understanding the context of a specific project.

This milestone focuses on **parsing, embedding, and visualizing code semantics** to lay the groundwork for a context-aware code explainer.

---

## Methodology

### Step 1: Code Collection

* Prepared a set of **10 Python code snippets**.
* Snippets include **mathematical operations, activation functions, recursion, and loops**.
* Ensures diverse coverage of **syntax and structure**.

### Step 2: Code Parsing using AST

* Used Python’s built-in **`ast`** library to parse each snippet.
* Extracted components include:

  * Function and class names
  * Variable assignments
  * Loops and conditional statements
  * Import statements

Parsing through AST captures **code logic and structure**, not just textual content.

### Step 3: Tokenization

* Used Python’s **`tokenize`** and **`io`** libraries to break code into individual tokens.
* Tokenization converts code into **meaningful components** for embedding models.

### Step 4: Embedding Generation

Each tokenized snippet was passed through three pretrained transformer models:

| Model                  | Description                                                                                 |
| ---------------------- | ------------------------------------------------------------------------------------------- |
| **MiniLM-L6-v2**       | Lightweight, general-purpose NLP model.                                                     |
| **DistilRoBERTa-base** | Optimized for sentence-level representations and semantic understanding.                    |
| **CodeBERT-base**      | Code-specific model trained on large GitHub repositories; understands syntax and semantics. |

### Step 5: Visualization

Two types of visualizations were created to interpret model performance:

1. **Heatmap:**

   * Displays **pairwise cosine similarity** between embeddings.
   * Shows how closely related snippets are.

2. **t-SNE Plot:**

   * Reduces **high-dimensional embeddings to 2D**.
   * Provides an intuitive view of clustering patterns.

---

## Results and Observations

* **MiniLM** and **DistilRoBERTa** embeddings showed weak semantic relationships since they are primarily trained on **natural language data**.
* **CodeBERT** embeddings produced **more meaningful similarity values**, grouping conceptually similar snippets together in heatmaps and t-SNE visualizations.
* The t-SNE plot clearly separated **unrelated snippets** and clustered **functionally similar snippets**.
* This validates that **code-specific models outperform general NLP models** in understanding programming code.

---

## Key Insights

* **AST parsing** captures the logical structure of code, beyond mere text.
* **Tokenization** enables model-friendly representation of code syntax.
* **CodeBERT** embeddings are better suited for code-based tasks than general NLP models.
* **Visualizations** like heatmaps and t-SNE plots provide a clear understanding of model behavior.
* The pipeline serves as a **baseline for integrating RAG** in future milestones.

---

## Conclusion

This milestone demonstrates how transformer models interpret programming code.

By combining:

* AST parsing
* Tokenization
* Embedding comparison

we have created a foundation for the **next phase of CodeGenie**: a context-aware code explainer powered by **RAG**.

This approach will allow the AI to deliver **project-specific, accurate, and context-rich code explanations** in future milestones.

---

## Tools and Technologies Used

* **Language:** Python
* **Platform:** Google Colaboratory
* **Libraries:**  ast, tokenize, io, transformers, sentence-transformers, scikit-learn, matplotlib, seaborn
* **Models:** MiniLM-L6-v2, DistilRoBERTa-base, CodeBERT-base
* **Visualization:** Heatmap (Seaborn), t-SNE (Scikit-learn)
