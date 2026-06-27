# Multimodal-Brain-Tumor-Detection

A multimodal deep learning framework for brain tumor classification using **Computed Tomography (CT)** and **Magnetic Resonance Imaging (MRI)**. The proposed framework integrates **Vision Mamba**, **Supervised Contrastive Learning**, **Prototype Cross-Attention**, and **Explainable AI (XAI)** to learn robust multimodal representations for brain tumor detection.

---

## Proposed Architecture

<p align="center">
  <img src="architecture/model_architecture.png" width="1000">
</p>

<p align="center">
<b>Figure 1.</b> Overall architecture of the proposed multimodal CT–MRI brain tumor detection framework.
</p>

---

## Proposed Approach

The proposed framework utilizes paired **CT** and **MRI** images to exploit complementary anatomical information from both imaging modalities. Each modality is processed independently through a dedicated **Vision Mamba** encoder, enabling the extraction of modality-specific spatial features while preserving the intrinsic characteristics of CT and MRI scans. The extracted features are subsequently projected into a shared latent space through a **Shared Projection Head**, producing a unified feature representation.

To improve feature discrimination, the projected embeddings are optimized using **Supervised Contrastive Learning**, encouraging compact intra-class representations while increasing inter-class separation. The learned representations are further refined through a **Prototype Cross-Attention** module, where image features interact with learnable class prototypes to obtain prototype-guided feature embeddings.

Finally, the refined representations are classified using an **L2 Distance Classifier**. To improve interpretability, the framework incorporates **Explainable AI (XAI)** through **Grad-CAM++**, prototype similarity analysis, attention visualization, and **UMAP** feature embeddings.

---

## Key Features

* Multimodal CT–MRI brain tumor classification
* Dual Vision Mamba feature extraction
* Shared latent representation learning
* Supervised Contrastive Learning
* Prototype Cross-Attention
* L2 Distance-based classification
* Explainable AI (Grad-CAM++, UMAP, Prototype Similarity Analysis)
* Robust evaluation using **5-fold cross-validation**
* Designed to support large-scale multimodal medical imaging datasets

---

## Environment

| Component | Specification                |
| --------- | ---------------------------- |
| Platform  | Google Colab                 |
| GPU       | NVIDIA Tesla T4 (16 GB VRAM) |
| Python    | 3.11                         |
| PyTorch   | 2.x                          |
| CUDA      | 12.x                         |

The framework is compatible with any CUDA-enabled GPU with sufficient memory.

---

## Documentation

The repository documentation is organized as follows:

| File           | Description                                  |
| -------------- | -------------------------------------------- |
| `DATASET.md`   | Dataset overview and download instructions   |
| `INSTALL.md`   | Environment setup and installation           |
| `TRAINING.md`  | Training methodology and evaluation protocol |
| `INFERENCE.md` | Inference workflow                           |
| `RESULTS.md`   | Evaluation summary and future result updates |

---

## Repository Structure

```text
Multimodal-Brain-Tumor-Detection/
│
├── architecture/
│   └── model_architecture.png
│
├── notebooks/
│   └── Multimodal_Brain_Tumor_Detection.ipynb
│
├── DATASET.md
├── requirements.txt
├── INSTALL.md
├── TRAINING.md
├── INFERENCE.md
├── RESULTS.md
├── LICENSE
├── .gitignore
└── README.md
```

---

## Quick Start

Clone the repository:

```bash
git clone https://github.com/shantanu0078/Multimodal-Brain-Tumor-Detection.git
cd Multimodal-Brain-Tumor-Detection
```

Install the required dependencies:

```bash
pip install -r requirements.txt
```

Open:

```text
notebooks/Multimodal_Brain_Tumor_Detection.ipynb
```

Refer to **INSTALL.md**, **TRAINING.md**, and **INFERENCE.md** for detailed instructions.

---

## Citation

Citation information will be added following publication of the associated research paper.

---

## License

This project is released under the **MIT License**. See the `LICENSE` file for details.
