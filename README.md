# CAIRLab Federated Learning Competition - TechChampions

This repository contains the submission code, defense pipeline, and exported model artifacts for the CAIRLab federated learning competition.

## Approach Overview
* **Track:** Advanced (Adversarial Defense against Model Poisoning)
* **Defense Strategy:** Robust clipping combined with server-side holdout verification.
* **Result:** Successfully neutralizes malicious scaling/label-flip attacks, lifting test F1-score from a collapsed baseline of ~0.05 to a stable **0.7017**.

## Repository Structure
* `notebook.ipynb`: The complete end-to-end pipeline (Data prep, Non-IID Dirichlet partitioning, FL training loop, defense mechanism, and evaluation).
* `model_scripted.pt`: The final TorchScript-exported model used for independent verification.
* `submission.json`: Self-reported metrics and track configuration file.
* `results.json`: Multi-seed validation metrics and comparison details.
* `cover_image.png`: Performance curve visualization (before vs. after defense).

## Setup & Reproduction
1. Install dependencies:
   ```bash
   pip install torch numpy scikit-learn matplotlib pandas
