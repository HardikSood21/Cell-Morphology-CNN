# Automated Cell Morphology Classification using CNNs

## Project Overview
This project implements a **Convolutional Neural Network (CNN)** to automate the classification of White Blood Cells (WBCs) into four distinct subtypes: Eosinophil, Lymphocyte, Monocyte, and Neutrophil. This work addresses the need for rapid, automated differential blood counting in high-throughput screening environments.

## Technical Architecture
- **Framework:** PyTorch
- **Model:** Custom 3-layer Convolutional Neural Network
- **Input:** 128x128 RGB Images
- **Regularization:** Dropout (0.5) and Image Augmentation (Rotation, Flipping)

## Workflow
1. **Preprocessing:** Raw images from the BCCD dataset were resized and normalized.
2. **Augmentation:** To handle class imbalance, random affine transformations were applied during training.
3. **Training:** The model was trained using CrossEntropyLoss and the Adam optimizer.
4. **Validation:** Achieved ~92% accuracy on the validation set.

## Dependencies
- Python 3.x
- PyTorch
- OpenCV
- NumPy
