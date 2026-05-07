
# EO-SAR Building Damage Change Detection

## Overview
This project implements binary change detection using a U-Net segmentation model with a ResNet34 encoder for EO-SAR satellite imagery.

## Dataset
Dataset contains:
- Pre-event satellite images
- Post-event satellite images
- Building damage masks

Label remapping:
- 0 -> 0
- 1 -> 0
- 2 -> 1
- 3 -> 1

## Model
- Architecture: U-Net
- Encoder: ResNet34
- Framework: PyTorch

## Training Configuration
- Epochs: 3
- Batch Size: 2
- Learning Rate: 1e-4
- Optimizer: Adam
- Loss Function: BCEWithLogitsLoss

## Validation Metrics
- F1 Score: 0.1245
- IoU: 0.0664
- Precision: 0.0688
- Recall: 0.6553

## Observations
The model achieved moderate recall but suffered from high false positives due to severe class imbalance.

## Future Improvements
- Dice Loss
- Focal Loss
- Attention U-Net
- Transformer segmentation
- Data augmentation

## Hardware
- Google Colab
- Tesla T4 GPU
