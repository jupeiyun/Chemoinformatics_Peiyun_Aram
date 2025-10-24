# Chemoinformatics_Peiyun_Aram
Peiyun and Aram's Project on Chemoinformatics Class

# Regression Task
1. Protein–Ligand Binding Affinity Prediction (PDBbind 2015)
This project investigates the prediction of protein–ligand binding affinities (pKd) using the PDBbind v.2015 dataset. Two approaches were implemented and compared: a traditional Random Forest regression model based on molecular descriptors, and a Graph Convolutional Network (GCN) leveraging molecular graph representations.

2. Repository Contents
chemo_RF V3.ipynb – Random Forest regression workflow
chemo_GCN_V3.ipynb – Graph Convolutional Network implementation
README.md – Project documentation and setup instructions

3. Project Overview
The PDBbind database provides experimentally measured binding affinity data (Kd, Ki, IC₅₀) for biomolecular complexes in the Protein Data Bank (PDB).
This dataset includes both protein and ligand structural information, enabling a range of structure-based learning tasks.
Data were obtained via MoleculeNet and filtered to include only high-quality entries (refined and core sets).

Objective:
To predict the pKd values of protein–ligand complexes and compare the performance of descriptor-based and graph-based models.

4. Methodology
1) Random Forest (RF)
Input features: RDKit molecular descriptors
(MolWt, MolLogP, TPSA, NumHDonors, NumHAcceptors, NumRotatableBonds)
Model: RandomForestRegressor from scikit-learn
Evaluation metrics: R², RMSE, MAE

2) Graph Convolutional Network (GCN)
Framework: DeepChem
Input representation: Molecular graphs (atoms as nodes, bonds as edges)
Architecture: Two graph convolutional layers with ReLU activations and dropout
Evaluation metrics: R², RMSE, MAE

Envirnonment
1) macOS (Apple Silicon, ARM, Python 3.10) for RF
2) Google Colab (Python 3.9, GPU Runtime) for GCN

Data Source
PDBbind v.2015 – Binding affinities for biomolecular complexes, including both protein and ligand structures.
Source: https://moleculenet.org/datasets-1
Citation:
Liu, Z. et al. Bioinformatics 2015, 31(3), 405–412.
“PDBbind: A comprehensive collection of binding affinities for biomolecular complexes.”

