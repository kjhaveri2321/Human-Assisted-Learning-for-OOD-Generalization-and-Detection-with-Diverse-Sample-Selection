# AHA-Human-Assisted-Out-of-Distribution-Generalization-and-Detection
## Overview
This notebook implements a near-paper reproduction of AHA (Adaptive Human-Assisted OOD Learning)
and introduces a simple extension called AHA-Diverse.

The goal is to study how different sample selection strategies affect:
- generalization under distribution shift (covariate OOD)
- detection of unseen classes (semantic OOD)

We use CIFAR-10 as the base dataset and evaluate robustness on multiple OOD datasets.

The pipeline follows:
1. Pretrain a model on in-distribution data
2. Score unlabeled “wild” data
3. Select samples using different strategies (Top-k, AHA, AHA-Diverse)
4. Finetune using selected samples
5. Evaluate performance using ID accuracy, OOD accuracy, FPR95, and AUROC
