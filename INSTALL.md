# Installation

This guide describes how to set up the environment required to run the proposed multimodal brain tumor detection framework.

---

## Prerequisites

Ensure the following software is installed before proceeding:

* Python **3.11**
* Git
* NVIDIA GPU with CUDA support (recommended)
* NVIDIA CUDA Toolkit **12.x** (optional for GPU acceleration)

---

## Clone the Repository

Clone the repository to your local machine:

```bash
git clone https://github.com/shantanu0078/Multimodal-Brain-Tumor-Detection.git
cd Multimodal-Brain-Tumor-Detection
```

---

## Create a Virtual Environment (Recommended)

### Windows

```bash
python -m venv venv
venv\Scripts\activate
```

### Linux / macOS

```bash
python3 -m venv venv
source venv/bin/activate
```

---

## Install Dependencies

All required Python packages are listed in the provided `requirements.txt` file.

Install the dependencies using:

```bash
pip install -r requirements.txt
```

---

## Verify the Installation

Verify that PyTorch detects your GPU:

```bash
python -c "import torch; print(torch.cuda.is_available())"
```

If CUDA is installed correctly, the command should return:

```text
True
```

---

## Tested Environment

The framework was developed and evaluated using the following environment:

| Component    | Version                      |
| ------------ | ---------------------------- |
| Python       | 3.11                         |
| PyTorch      | 2.x                          |
| CUDA         | 12.x                         |
| Google Colab | Latest                       |
| GPU          | NVIDIA Tesla T4 (16 GB VRAM) |

The framework was developed and evaluated using **Google Colab** with an **NVIDIA Tesla T4 GPU (16 GB VRAM)**. It can also be executed on any CUDA-compatible GPU with sufficient memory.
