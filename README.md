# Infosys_Springboard

## Project Overview

This repository implements Milestone 1 – Code Explainer for the Infosys CodeGenie Internship. It builds a pipeline to parse and analyze AI-related Python code snippets using:

AST (Abstract Syntax Tree) for parsing

Tokenization

Pretrained NLP models: MiniLM, DistilRoBERTa, MPNet

## Code Snippets

10 small AI/ML-related functions, including:

Activation functions (Sigmoid, ReLU, Softmax)

Loss function (MSE)

Gradient Descent

Linear regression prediction

One-hot encoding

## Pipeline Steps

AST Parsing → Extract functions, classes, imports

Tokenization → Prepare code for NLP models

Embeddings → Generate vector representations using MiniLM, DistilRoBERTa, MPNet

Similarity Analysis & Visualization → Heatmaps and PCA scatter plots to show functional relationships

## Observations

MiniLM embeddings grouped activation functions (sigmoid, ReLU, softmax) closely

DistilRoBERTa embeddings showed slightly different clustering but still captured functional similarity

MPNet embeddings captured semantic similarity best, separating prediction, loss, and encoding functions

Overall, pretrained NLP models can effectively represent AI code structures and relationships

## How to Run

Open Ashreen Fathima Milestone 1.ipynb in Colab

Run all cells

View AST parsing output, similarity heatmaps, and PCA plots

## Files in this Repository

Ashreen Fathima Milestone 1.ipynb → Colab notebook containing full implementation

README.md → Project description, methodology, and observations

