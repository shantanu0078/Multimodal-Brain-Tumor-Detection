# Multimodal-Brain-Tumor-Detection

A multimodal deep learning framework for brain tumor detection using CT–MRI fusion, Vision Mamba, prototype cross-attention, and explainable AI.

## Proposed Approach

The proposed framework utilizes paired **CT and MRI** images to exploit complementary anatomical information from both imaging modalities. Each modality is processed independently through a dedicated **Vision Mamba** encoder, enabling the extraction of modality-specific spatial features while preserving the intrinsic characteristics of CT and MRI scans. The extracted features are subsequently mapped into a common latent space through a **Shared Projection Head**, producing a unified **2D spatial feature sequence** for subsequent representation learning.

To improve feature discrimination, the projected embeddings are globally pooled and optimized using **Supervised Contrastive Learning**, encouraging samples belonging to the same tumor class to form compact clusters while increasing the separation between different classes. The spatial feature sequence is then refined using a **Prototype Cross-Attention** module, where the image features interact with a set of **learnable class prototypes** to obtain prototype-guided feature representations.

Finally, the refined representation is compared with the learned prototypes through an **L2 Distance Classifier**, producing the final clinical prediction. To improve model interpretability, an integrated **Explainable AI (XAI)** module utilizes intermediate feature maps, prototype attention outputs, and prediction results to generate **Grad-CAM++ visualizations, attention maps, UMAP embeddings, and prototype similarity scores**, providing clinically meaningful explanations for the model's predictions.
