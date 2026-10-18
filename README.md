# 3D-Brain-Tumor-Segmentation-from-MRI-Using-3D-U-Net
3D brain tumor segmentation from multimodal MRI using PyTorch, MONAI, and a 3D U-Net. Evaluated on the Medical Segmentation Decathlon BrainTumour dataset.

# 3D Brain Tumor Segmentation from MRI

A deep learning project for multiclass brain tumor segmentation using 3D MRI scans, PyTorch, MONAI, and a 3D U-Net.

## Overview

This project trains a 3D U-Net to segment brain tumor regions from multimodal MRI volumes using the Medical Segmentation Decathlon Task01_BrainTumour dataset. The workflow includes preprocessing, patch-based training, sliding-window inference, and Dice-score evaluation.

## Technologies

- Python
- PyTorch
- MONAI
- NumPy
- Matplotlib
- Google Colab

## Dataset

Medical Segmentation Decathlon — Task01_BrainTumour. Please refer to the dataset's official terms and citation requirements before redistributing any data.

## Model

- Architecture: 3D U-Net
- Input: 4 MRI modalities
- Output: 4 classes (background and three tumor labels)
- Loss: Dice + Cross-Entropy
- Inference: Sliding-window inference

## Validation Results

Evaluated on 78 validation cases.

| Region | Mean Dice |
|---|---:|
| Whole Tumor (WT) | 0.8544 |
| Tumor Core (TC) | 0.7381 |
| Enhancing Tumor (ET) | 0.7282 |
| Mean of regional Dice scores | 0.7736 |

## Limitations

These results are from a validation split and do not establish clinical readiness or performance on independent datasets. This project is for educational and research purposes only and is not intended for clinical diagnosis.

## How to Run

1. Open the notebook in Google Colab.
2. Install the required dependencies.
3. Download or configure access to the dataset.
4. Run preprocessing, training, and evaluation cells.

## Future Improvements

- Evaluate on an independent test dataset.
- Compare against other segmentation architectures.
- Improve reproducibility with fixed seeds and saved configuration files.
- Add qualitative prediction visualizations.
