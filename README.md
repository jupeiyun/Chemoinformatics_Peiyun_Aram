Chemoinformatics_Peiyun_Aram
Peiyun Ju and Aram’s Project for the Chemoinformatics Course
Overview
This repository contains the complete code, data processing, and model implementations for two chemoinformatics tasks:
Protein–Ligand Binding Affinity Prediction (Regression, PDBbind v.2015)
Drug Toxicity and Approval Prediction (Classification, ClinTox from MoleculeNet)
Both projects explore how molecular features derived from RDKit and graph-based representations in DeepChem can be used to predict biologically relevant outcomes.
1. Regression Task – PDBbind 2015
Objective: Predict protein–ligand binding affinities (pKd) using experimental data from PDBbind v.2015.
Approaches:
Random Forest (RF): Descriptor-based model using physicochemical features from RDKit (MolWt, MolLogP, TPSA, NumHDonors, NumHAcceptors, NumRotatableBonds).
Graph Convolutional Network (GCN): Graph-based model using molecular topology (atoms as nodes, bonds as edges) implemented in DeepChem.
Evaluation: R², RMSE, and MAE for model performance comparison.
Files:
chemo_RF_V3.ipynb – Random Forest regression workflow
chemo_GCN_V3.ipynb – Graph Convolutional Network implementation
2. Classification Task – ClinTox
Objective: Classify compounds as FDA-approved or clinically toxic using molecular fingerprints and descriptors.
Approaches:
Random Forest (RF): Multi-output classifier with balanced class weights and Optuna hyperparameter optimization.
Feedforward Neural Network (FFNN): Descriptor-based deep learning model built with Keras.
Graph Convolutional Network (GCN): Graph-based toxicity prediction using DeepChem.
Evaluation: ROC–AUC, macro-F1, accuracy, and confusion matrices for both labels (FDA_APPROVED, CT_TOX).
Files:
chemo_RF_ClinTox.ipynb – Random Forest classification workflow
chemo_FFNN_ClinTox.ipynb – Feedforward Neural Network implementation
chemo_GCN_ClinTox.ipynb – Graph Convolutional Network for toxicity prediction
Environment
macOS (Apple Silicon, Python 3.10) – RF implementation
Google Colab (Python 3.9, GPU runtime) – GCN and FFNN implementations
Data Sources
PDBbind v.2015: Protein–ligand binding affinities and structures
Source: https://moleculenet.org/datasets-1
Citation: Liu, Z. et al., Bioinformatics, 2015, 31(3), 405–412.
ClinTox: Drug toxicity and FDA approval dataset
Source: https://moleculenet.org/datasets-1
Citation: Wu, Z. et al., Chemical Science, 2018, 9(2), 513–530.
Declaration
ChatGPT was used to refine code readability, rephrase text for clarity, and check formatting consistency. All conceptual design, data analysis, and interpretation were conducted by the project authors.

