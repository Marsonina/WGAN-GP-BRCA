# TCGA-BRCA Synthetic Data Generation via WGAN-GP

## Project Overview

This project focuses on the generation of high-fidelity synthetic gene expression data for Breast Invasive Carcinoma (BRCA). By leveraging the **TCGA-BRCA** dataset and focusing on specific biological signatures, we aim to overcome data scarcity and privacy constraints in cancer research.

## Methodology

### 1. Biologically-Informed Feature Selection

To reduce the high dimensionality of the original TCGA dataset and focus on the most informative signals, we restricted the feature space to two specific gene sets:

* **BRCA1_UP:** Genes identified as significantly up-regulated in breast cancer.
* **BRCA1_DN:** Genes identified as significantly down-regulated.

This targeted approach ensures the model learns the specific transcriptomic "fingerprint" of the disease rather than background noise.

### 2. Generative Architecture: WGAN-GP

We implemented a **Wasserstein GAN with Gradient Penalty (WGAN-GP)**.

## Objectives

* **Data Augmentation:** Provide a robust pipeline to generate synthetic samples for training downstream machine learning classifiers.
* **Biological Fidelity:** Ensure that the synthetic data maintains the correlation structures between up-regulated and down-regulated gene sets.
* **Dimensionality Reduction:** Demonstrate that focusing on established gene signatures (BRCA1_UP/DN) leads to more stable generative modeling than using the full genome.
