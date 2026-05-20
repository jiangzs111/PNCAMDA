# PNCAMDA

## Introduction

In this repo, we implement the method **PNCAMDA: a reliability-aware matrix completion framework for miRNA-disease association prediction**. PNCAMDA integrates association-aware feature enhancement, positive-unlabeled weighted matrix completion, and neighborhood consensus reranking to predict potential miRNA-disease associations.



## Requirements

The code is implemented in Python and can be run on CPU. No GPU or CUDA environment is required.

- Python >= 3.8
- NumPy >= 1.21
- pandas >= 1.3
- scikit-learn >= 1.0
- openpyxl >= 3.0
- PyTorch >= 1.6
- CUDA >= 10.1

## Data

The benchmark datasets should be placed in the `dataset` folder. The current implementation supports HMDD v2.0, HMDD v3.2, and HMDD v4.0.

```text
─ HMDD v2.0/
─ HMDD v3.2/
─ HMDD v4.0/
```

The dataset folders contain miRNA-disease association data, disease names, miRNA names, and similarity information.

- HMDD v2.0: known miRNA-disease associations, disease semantic similarity matrices, miRNA functional similarity matrix, and name files.
- HMDD v3.2: miRNA-disease association matrix, disease semantic similarity, miRNA semantic similarity, miRNA sequence similarity, miRNA functional similarity, and name files.
- HMDD v4.0: HMDD v4.0 association data, disease and miRNA name files.


## Main Files

```text
main.py                  Entry point
config.py                Parameter settings
data_loader.py           Dataset loading
similarity.py            Similarity calculation
feature_enhancement.py   Association-aware feature enhancement
matrix_completion.py     Weighted matrix completion
pu_ncr.py                PU weighting and neighborhood consensus reranking
model.py                 PNCAMDA prediction pipeline
evaluation.py            Cross-validation evaluation
metrics.py               Evaluation metrics
utils.py                 Utility functions
```
