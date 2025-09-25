Graphene TEM Segmentation with U-Net + ResNet

🔬 Project Goal

* Automated segmentation of graphene flakes and carbon holes in TEM images.
* Replaces time-consuming, subjective manual annotation with a scalable deep learning pipeline.

⚙️ Model & Methods

* U-Net with ResNet backbone for hierarchical feature extraction.
* Patch-based training with overlap to handle large TEM images.
* Custom loss functions: Tversky, Dice, and BCE combinations for class balance.
* Threshold tuning to maximize IoU on validation data.

🚀 Training Optimization

* Mixed-precision training (AMP) with gradient scaling → faster GPU training.
* Adaptive learning rate scheduling + early stopping → stable convergence.
* Data augmentations: flips, rotations, Gaussian noise/blur, contrast & brightness jitter, and magnification scaling (200x vs 2000x).

📊 Results & Evaluation

* Metrics: IoU, Dice/F1, precision, recall, specificity.
* Rigorous validation on train / val / test split with per-image overlays and error maps.
* Demonstrates strong generalization across heterogeneous TEM conditions.
* Trained only on 10 images - excellent results.

💻 Tech Stack

* PyTorch, segmentation-models-pytorch, Albumentations, Matplotlib.
* Integrated with Google Cloud Vertex AI for scalable training & deployment.
* Fully reproducible, with structured data preprocessing, augmentation, and evaluation pipelines.
* Transfer learning

🌍 Relevance

Real-world application in materials science & nanotechnology.

Demonstrates best practices in deep learning for image segmentation.

Highly transferable to medical imaging, defect detection, and industrial quality control.
