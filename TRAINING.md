# Training

This document describes the training procedure used for the proposed multimodal brain tumor detection framework.

---

## Overview

The proposed framework performs multimodal brain tumor classification using paired **Computed Tomography (CT)** and **Magnetic Resonance Imaging (MRI)** images. Feature extraction is performed independently for each modality using dedicated **Vision Mamba** encoders, followed by shared representation learning, prototype-guided feature refinement, and final classification.

---

## Dataset

The framework was trained and evaluated using the publicly available CT–MRI datasets described in **DATASET.md**.

Each dataset was used **independently** for model training and evaluation.

---

## Training Strategy

The model is trained using **5-fold cross-validation**, where four folds are used for training and one fold is reserved for validation during each iteration. The reported performance corresponds to the average across all five folds, providing a robust estimate of the model's generalization capability.

The framework is designed to support **large-scale multimodal medical imaging datasets**, making it suitable for reliable evaluation across diverse data distributions.

---

## Hardware Environment

The experiments were conducted using the following environment:

| Component | Specification                |
| --------- | ---------------------------- |
| Platform  | Google Colab                 |
| GPU       | NVIDIA Tesla T4 (16 GB VRAM) |
| Python    | 3.11                         |
| PyTorch   | 2.x                          |
| CUDA      | 12.x                         |

---

## Model Checkpoints

The best-performing model is automatically saved during training based on validation performance and is subsequently used for evaluation and inference.

---

## Reproducibility

To reproduce the training procedure:

1. Download the datasets described in **DATASET.md**.
2. Install the required packages listed in **requirements.txt**.
3. Follow the setup instructions in **INSTALL.md**.
4. Execute the notebook:

```text
notebooks/Multimodal_Brain_Tumor_Detection.ipynb
```

The notebook contains the complete training and evaluation pipeline.
