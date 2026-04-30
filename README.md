# PNCAMDA

PNCAMDA is a reliability-aware positive-unlabeled matrix completion framework with neighborhood consensus for miRNA–disease association prediction.

The framework contains three main components:

1. Association-Aware Feature Enhancement (AAFE)
2. Positive-Unlabeled Weighted Matrix Completion (PUWMC)
3. Neighborhood Consensus Reranking (NCR)

This repository provides the Python implementation of PNCAMDA and the ablation experiment used to evaluate the contribution of AAFE, PUWMC and NCR.

## Overview

PNCAMDA is designed for prioritizing potential miRNA–disease associations from known association matrices and disease/miRNA similarity information.

The main workflow is:

1. Load HMDD miRNA–disease association data.
2. Construct a disease × miRNA binary interaction matrix.
3. Reconstruct fold-wise Gaussian interaction profile similarities.
4. Enhance disease and miRNA similarities using association-aware profile information.
5. Estimate positive-unlabeled confidence weights for unknown pairs.
6. Perform weighted low-rank matrix completion.
7. Refine high-confidence candidates using neighborhood consensus reranking.
8. Evaluate prediction scores using AUC, AUPR, Accuracy, Precision, Recall, F1-score, Specificity and MCC.

## Main file

```text
PNCAMDA.py# PNCAMDA
