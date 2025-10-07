Infosys CodeGenie Project – Milestone 1: Code Explainer
Project Overview

This milestone is part of the Infosys CodeGenie – AI Explainer and Code Generator Project.
The objective of this stage is to build a Code Explainer pipeline that can analyze Python code snippets, extract their structure, and generate meaningful embeddings using advanced NLP models.

This milestone focuses on developing the foundation for a larger system that will later use Retrieval-Augmented Generation (RAG) to provide context-aware explanations for entire codebases.

Objective

The goal of this milestone is to:

Prepare a set of Python code snippets.
Parse each snippet using the Abstract Syntax Tree (AST) to understand its components and hierarchy.
Tokenize the code to prepare it for model-based analysis.
Generate embeddings using three pretrained transformer models: MiniLM, DistilRoBERTa, and CodeBERT.
Compare the models by visualizing similarities through heatmaps and t-SNE plots.
Problem Statement

Existing AI-based code assistants are good at understanding general programming concepts, but they often fail when it comes to specific project-level code understanding.
Because these models lack awareness of the local codebase, their explanations tend to be generic or even inaccurate.

To overcome this limitation, we aim to design an AI system that can understand the context of a particular project.
This milestone represents the first step in that direction — focusing on parsing, embedding, and visualizing code semantics.

Methodology
Step 1: Code Collection

A set of ten Python code snippets was prepared. These included simple functions for mathematical operations, activation functions, and basic algorithms such as recursion and loops. This ensures diverse coverage of syntax and structure.

Step 2: Code Parsing using AST

We used Python’s built-in ast (Abstract Syntax Tree) library to parse each snippet.
This allows the extraction of:

Function and class names
Variable assignments
Loops and conditions
Import statements

Parsing through AST ensures the model captures not just text, but also code logic and structure.

Step 3: Tokenization

The tokenize and io libraries were used to break the code into individual tokens.
Tokenization converts source code into meaningful components, enabling the embedding models to process them effectively.

Step 4: Embedding Generation

Each tokenized snippet was passed into three pretrained transformer models:

MiniLM-L6-v2: General-purpose, lightweight NLP model.
DistilRoBERTa-base: Optimized for sentence-level representations and semantic understanding.
CodeBERT-base: A code-specific model trained on large GitHub repositories that understands syntax and semantics of source code.
Step 5: Visualization

Two types of visualizations were created to interpret model performance:

Heatmap: Displays pairwise cosine similarity between embeddings to show how closely related snippets are.
t-SNE Plot: Reduces high-dimensional embeddings to a two-dimensional space for intuitive visualization of clustering patterns.
Results and Observations
MiniLM and DistilRoBERTa embeddings showed weak semantic relationships because they are trained mainly on natural language data.
CodeBERT generated more meaningful similarity values, grouping conceptually similar snippets closer together in the heatmap and t-SNE visualization.
The t-SNE plot demonstrated clear separation between unrelated snippets and visible clustering among functionally similar ones.
The experiment validated that code-specific models outperform generic NLP models in understanding programming code structure and meaning.
Key Insights
AST parsing helps capture the logical structure of code, not just textual content.
Tokenization enables model-friendly representation of code syntax.
CodeBERT embeddings are better suited for code-based tasks compared to general NLP models.
Visualizations like heatmaps and t-SNE plots help interpret model behavior effectively.
This pipeline serves as a baseline for integrating Retrieval-Augmented Generation (RAG) in future milestones.
Conclusion

This milestone successfully demonstrates how different transformer models interpret programming code.
By combining AST parsing, tokenization, and embedding comparison, we have built a foundation for the next phase of the CodeGenie project — implementing a context-aware code explainer powered by RAG (Retrieval-Augmented Generation).
This approach will allow the AI to deliver project-specific, accurate, and context-rich code explanations in future milestones.

Tools and Technologies Used
Python
Google Colaboratory
Libraries: ast, tokenize, io, transformers, sentence-transformers, scikit-learn, matplotlib, seaborn
Models: MiniLM-L6-v2, DistilRoBERTa-base, CodeBERT-base
Visualization: Heatmap (Seaborn), t-SNE (Scikit-learn)
