# Automated Cell Morphology Classification using CNNs

![PyTorch](https://img.shields.io/badge/PyTorch-Deep_Learning-red)
![OpenCV](https://img.shields.io/badge/OpenCV-Computer_Vision-green)
![Accuracy](https://img.shields.io/badge/Validation_Accuracy-92%25-blue)

## 📌 Project Overview
This project implements a **Convolutional Neural Network (CNN)** to automate the classification of blood cell subtypes. Using the **BCCD Dataset**, the model distinguishes between four distinct types of white blood cells: **Eosinophils, Lymphocytes, Monocytes, and Neutrophils**.

The goal was to replicate **High-Throughput Screening** workflows used in pharmaceutical engineering, where automated image analysis replaces manual microscopy.

## 🔬 The Data
**Dataset:** BCCD (Blood Cell Count and Detection)
* **Classes:** 4 (Eosinophil, Lymphocyte, Monocyte, Neutrophil)
* **Preprocessing:**
    * Resizing to 224x224 (Standard Input)
    * **Data Augmentation:** Random rotations (+/- 20°), horizontal flips, and scaling were applied to handle class imbalance and prevent overfitting.
    * Normalization using ImageNet standards.

## 🧠 Model Architecture
I built a custom CNN using **PyTorch** with the following structure:
1.  **3 Convolutional Layers:** To extract spatial features (edges, textures, cell shapes).
2.  **Max Pooling:** To reduce dimensionality and retain the most prominent features.
3.  **ReLU Activation:** To introduce non-linearity.
4.  **Fully Connected Layers:** To map extracted features to the 4 output classes.

## 📊 Results
* **Training Accuracy:** ~95%
* **Validation Accuracy:** 92%
* **Key Metric:** The model successfully generalized to unseen test images, proving robust against variations in cell orientation and staining intensity.

## 🛠️ Tech Stack
* **Framework:** PyTorch
* **Image Processing:** OpenCV, Torchvision
* **Visualization:** Matplotlib, Seaborn

## 🚀 How to Run
1.  Clone the repository.
2.  Install dependencies: `pip install torch torchvision opencv-python matplotlib scikit-learn`
3.  Run `Blood_Cell_Classification.ipynb`.
