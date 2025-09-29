# Infosys_Springboard

## Project Overview
This repository implements **Milestone 1 – Code Explainer** for the Infosys CodeGenie Internship.  
It builds a pipeline to parse and analyze **AI-related Python code snippets** using:
- **AST (Abstract Syntax Tree)** for parsing
- **Tokenization**
- **Pretrained NLP models**: MiniLM, DistilRoBERTa, MPNet

## Code Snippets
10 small **AI/ML-related functions**, including:
- Activation functions (Sigmoid, ReLU, Softmax)
- Loss function (MSE)
- Gradient Descent
- Linear regression prediction
- One-hot encoding

## Pipeline Steps
1. AST Parsing → Extract functions, classes, imports  
2. Tokenization → Prepare code for NLP models  
3. Embeddings → Generate vector representations using MiniLM, DistilRoBERTa, MPNet  
4. Similarity Analysis → Compute pairwise cosine similarities  
5. Visualization → Heatmaps and PCA scatter plots to show functional relationships

## Observations
- **MiniLM** embeddings grouped activation functions closely.  
- **DistilRoBERTa** embeddings had slightly different clustering but maintained functional similarity.  
- **MPNet** embeddings captured semantic similarity best, separating prediction, loss, and encoding functions.  
- NLP models can effectively represent AI code structures and relationships.

## How to Run
1. Open `Ashreen Fathima Milestone 1.ipynb` in Colab  
2. Run all cells  
3. View AST parsing output, similarity heatmaps, PCA plots  

## Files
- `Ashreen Fathima Milestone 1.ipynb` → Colab notebook  
- `snippets_metadata.csv` → Metadata from code parsing  
- `sim_<model>.csv` → Cosine similarity matrices for each model
