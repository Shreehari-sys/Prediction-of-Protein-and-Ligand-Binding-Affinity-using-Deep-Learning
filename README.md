# Prediction-of-Protein-and-Ligand-Binding-Affinity-using-Graph-Attention-Networks

## Overview

This project implements a GAT-based model to predict binding affinities between proteins and ligands. The workflow includes:
- Data preprocessing (SMILES to graph, pocket sequence encoding)
- Model training with K-Fold cross-validation and Optuna hyperparameter tuning
- Evaluation using MSE, MAE, R²
- Visualization of results and error analysis

## Data

- `train_dataset.csv` and `val_dataset.csv` contain SMILES strings, pocket sequences, and binding affinity labels.
- Data is preprocessed in the notebook to create graph representations for GNN input.


- **Graph Attention Network (GAT):**  
  3 layers with batch normalization, dropout, and skip connections.
- **Input:**  
  - Molecular graphs (from SMILES)
  - Protein pocket features (amino acid frequency vectors)
- **Output:**  
  - Regression prediction of binding affinity

## Requirements

- Python 3.8+
- PyTorch
- PyTorch Geometric
- RDKit
- scikit-learn
- pandas, numpy, matplotlib, seaborn, optuna
