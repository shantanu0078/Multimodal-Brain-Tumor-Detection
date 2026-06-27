# Inference

This document describes how to perform inference using the trained multimodal brain tumor detection framework.

---

## Overview

The proposed framework performs brain tumor classification using paired **Computed Tomography (CT)** and **Magnetic Resonance Imaging (MRI)** images. During inference, the trained Vision Mamba-based model extracts multimodal feature representations and produces the final prediction through prototype-guided classification.

---

## Requirements

Before running inference:

* Download the datasets described in **DATASET.md**.
* Install the required dependencies listed in **requirements.txt**.
* Follow the setup instructions provided in **INSTALL.md**.
* Ensure that the trained model checkpoint is available.

---

## Running Inference

Open the notebook:

```text
notebooks/Multimodal_Brain_Tumor_Detection.ipynb
```

Execute the inference cells to:

* Load the trained model checkpoint.
* Process paired CT and MRI images.
* Generate classification predictions.
* Produce Explainable AI (XAI) visualizations.

---

## Output

The inference pipeline generates:

* Brain tumor classification predictions.
* Prediction confidence scores.
* Grad-CAM++ visualizations.
* Prototype similarity analysis.
* UMAP feature embeddings (when enabled).

---

## Notes

The inference pipeline is compatible with any CUDA-enabled GPU that provides sufficient memory. The experiments presented in this repository were performed using **Google Colab** with an **NVIDIA Tesla T4 GPU (16 GB VRAM)**.
