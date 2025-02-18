# 🧠 Brain Tumor Segmentation Using an Encoder-Decoder Fully Convolutional Network  


## 📌 Overview  
This repository contains the implementation of **Brain Tumor Segmentation** using an **extension of an encoder-decoder fully convolutional network**. The project utilizes **ensemble deep learning** techniques to enhance segmentation accuracy for **magnetic resonance imaging (MRI)** brain tumor detection.

### ✨ Key Features  
- Trained **U-Net, U-Net Backbone (VGG, ResNet, Inception), and LinkNet** models on the **BRATS 2020 dataset**.  
- Implemented **ensemble learning** using VGG, ResNet, and Inception for enhanced segmentation.  
- Achieved an **IOU score of 61%** and an **accuracy of 97.21%**, outperforming traditional methods.  

---

## 📂 Dataset  
- **Dataset:** [BRATS 2020](https://www.med.upenn.edu/cbica/brats2020/)  
- Contains **371 NiFTI-format folders** with multimodal MRI images:
  - `T1.nii` - Native T1-weighted MRI  
  - `T1CE.nii` - Contrast-enhanced T1-weighted MRI  
  - `T2.nii` - T2-weighted MRI  
  - `FLAIR.nii` - Fluid-attenuated inversion recovery MRI  
  - `seg.nii` - Ground truth segmentation  

---

## 🏗️ Methodology  
### 🔧 Preprocessing  
- Cropping, resizing, and splitting data into **training and validation sets**.  
- Used **Min-Max Scaler** for normalization.  
- Converted images into **multi-channel volumes** (T1, T1CE, T2, FLAIR).  

### 🔍 Models Used  
| Model | Description |
|--------|------------|
| **U-Net** | Baseline model for segmentation |
| **Ensemble Model (VGG, ResNet, Inception)** | Combines multiple architectures to improve performance |
| **LinkNet** | Included for comparison purposes |

### 📊 Evaluation Metrics  
- **Dice Coefficient**
- **Intersection Over Union (IOU) Score**
- **Focal Loss**
- **Accuracy**

---

## 🏆 Results  
| Model | IOU Score | Accuracy |  
|--------|------------|------------|  
| **Ensemble (VGG, ResNet, Inception)** | **61%** | **97.21%** |  
| **U-Net** | 58% | 96.76% |  
| **LinkNet** | 56% | 96.10% |  

📌 **Best Model:** Ensemble (VGG, ResNet, Inception) 🎯  

---

## 🚀 Installation & Usage  
### 🔥 Prerequisites  
Make sure you have the following installed:  
- Python 3.8+  
- TensorFlow / PyTorch  
- NumPy, Pandas, Matplotlib  
- OpenCV, Scikit-learn  

### 📥 Clone Repository  
```bash
git clone https://github.com/your-username/brain-tumor-segmentation.git
cd brain-tumor-segmentation
