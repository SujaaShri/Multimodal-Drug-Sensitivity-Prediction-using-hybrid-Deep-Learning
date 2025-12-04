This project implements a multimodal deep learning framework for predicting the natural logarithm of IC50 (drug sensitivity) across cancer cell lines. The system integrates drug molecular structure and cell-line multi-omics information using an end-to-end trainable architecture.

# Key Components
## 1. Drug Representation

Molecular Graph Encoder

Uses GINEConv (Graph Isomorphism Network with Edge features)

Captures atomic features and bond-level interactions

SMILES Sequence Encoder

Uses a Bidirectional GRU (BiGRU)

Learns sequential chemical patterns from SMILES strings

## 2. Cell-line Multi-omics Encoder

Deep Neural Network (DNN)

Inputs: gene expression, mutation, and methylation profiles

Outputs a compact cell-line embedding

## 3. Multimodal Fusion

Multi-Head Attention Fusion (MHAF)

Learns dynamic relationships between graph, SMILES, and omics modalities

Produces a unified representation for prediction

## 4. IC50 Regression Head

Lightweight feed-forward predictor

Outputs continuous log-IC50 value

# Training Details

Optimizer: AdamW

Learning rate schedule: Cosine annealing

Loss: Mean Squared Error (MSE)

Regularization: Dropout

Early stopping based on: Pearson Correlation Coefficient (PCC)
