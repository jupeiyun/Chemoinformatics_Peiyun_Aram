# Chemoinformatics_Peiyun_Aram
**Peiyun Ju and Aram’s Project for the Chemoinformatics Course**

---

## 🧬 Overview
This repository contains the full code and documentation for two chemoinformatics projects:

1. **Protein–Ligand Binding Affinity Prediction** (Regression, *PDBbind v.2015*)
2. **Drug Toxicity and Approval Prediction** (Classification, *ClinTox* from MoleculeNet)

Both projects explore how molecular descriptors and graph-based features can be used to predict biologically relevant outcomes using RDKit, DeepChem, and scikit-learn.

---

## ⚗️ Regression Task – PDBbind 2015

**Objective:**  
Predict protein–ligand binding affinities (*pKd*) from the *PDBbind v.2015* refined and core subsets.

**Approaches:**
- **Random Forest (RF):** Descriptor-based regression using physicochemical features from RDKit  
  *(MolWt, MolLogP, TPSA, NumHDonors, NumHAcceptors, NumRotatableBonds)*
- **Graph Convolutional Network (GCN):** Graph-based regression using molecular graphs (atoms = nodes, bonds = edges) implemented in DeepChem  

**Evaluation Metrics:** `R²`, `RMSE`, `MAE`

**Files:**
- `chemo_RF_V3.ipynb` — Random Forest regression workflow  
- `chemo_GCN_V3.ipynb` — Graph Convolutional Network implementation

---

## 💊 Classification Task – ClinTox

**Objective:**  
Classify compounds as FDA-approved or clinically toxic using the *ClinTox* dataset from MoleculeNet.

**Approaches:**
- **Random Forest (RF):** Multi-output classifier with balanced class weights and Optuna hyperparameter optimization  
- **Feedforward Neural Network (FFNN):** Descriptor-based deep learning model built with Keras  
- **Graph Convolutional Network (GCN):** Graph-based toxicity prediction implemented with DeepChem  

**Evaluation Metrics:** `ROC–AUC`, `Macro-F1`, `Accuracy`, `Confusion Matrix`

**Files:**
- `chemo_RF_ClinTox.ipynb` — Random Forest classification workflow  
- `chemo_FFNN_ClinTox.ipynb` — Feedforward Neural Network  
- `chemo_GCN_ClinTox.ipynb` — GCN toxicity prediction

---

## ⚙️ Environment
- **macOS (Apple Silicon, Python 3.10)** — for RF models  
- **Google Colab (Python 3.9, GPU runtime)** — for GCN and FFNN models  

---

## 📚 Data Sources
- **PDBbind v.2015:** Protein–ligand binding affinities and structures  
  - Source: [https://moleculenet.org/datasets-1](https://moleculenet.org/datasets-1)  
  - Citation: Liu, Z. et al., *Bioinformatics*, 2015, 31(3), 405–412.  

- **ClinTox:** Drug toxicity and FDA approval dataset  
  - Source: [https://moleculenet.org/datasets-1](https://moleculenet.org/datasets-1)  
  - Citation: Wu, Z. et al., *Chemical Science*, 2018, 9(2), 513–530.  

---

## 🔍 Declaration
ChatGPT was used to refine code readability, rephrase text for clarity, and check formatting consistency.  
All conceptual design, data analysis, and interpretation were developed by the project authors.

---

## 🔗 Repository Link
**GitHub:** [https://github.com/jupeiyun/Chemoinformatics_Peiyun_Aram](https://github.com/jupeiyun/Chemoinformatics_Peiyun_Aram)
