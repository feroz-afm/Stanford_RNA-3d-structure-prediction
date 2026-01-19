# Stanford_RNA-3d-structure-prediction
Machine learning based project for predicting RNA three dimensional structures directly from nucleotide sequences, developed for the Stanford RNA 3D Folding Kaggle competition. The work focuses on sequence to structure modeling, deep learning techniques, multiple structure sampling, and TM score based evaluation for accurate RNA folding prediction.


# Stanford RNA 3D Folding – Kaggle Competition

Predicting the three-dimensional (3D) structure of RNA molecules from their nucleotide sequences using machine learning.

This repository contains my solution and experiments for the **Stanford RNA 3D Folding** Kaggle competition, which focuses on advancing RNA structure prediction and its applications in biology and medicine.

---

##  Competition Overview

RNA plays a critical role in essential biological processes, yet predicting its 3D structure remains a major challenge. Unlike proteins, RNA structure prediction suffers from limited experimental data and complex folding behavior.

This competition builds on recent advances such as **RibonanzaNet** and challenges participants to predict full RNA 3D structures using only sequence information.

**Competition Link:**  
https://www.kaggle.com/competitions/stanford-rna-3d-folding

---

##  Objective

Given an RNA sequence, predict the **3D coordinates of the C1' atom** for each residue.

For every RNA sequence:
- Predict **5 possible 3D structures**
- Final score is the **average of best-of-5 TM-scores**

---

## Evaluation Metric

Submissions are evaluated using **TM-score (Template Modeling Score)**:

- Range: **0.0 – 1.0** (higher is better)
- Alignment is sequence-independent
- Structures are aligned using **US-align**
- Best TM-score among the 5 predictions is selected per target

---

##  Dataset Description

- **train/**: RNA sequences with known 3D structures
- **test_sequences.csv**: RNA sequences without structures (used for inference)
- **submission.csv**: Predicted C1' atom coordinates

**Submission Format:**
```csv
ID,resname,resid,x_1,y_1,z_1,...,x_5,y_5,z_5
R1107_1,G,1,-7.561,9.392,9.361,...,-7.301,9.023,8.932
