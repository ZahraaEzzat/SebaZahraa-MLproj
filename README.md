# SebaZahraa-MLproj
project for intro to machine learning course.

# Comparing ResNet and Plain CNN for Image Classification on CIFAR-10

This project compares **ResNet-18** and a **Plain CNN-18** on the **CIFAR-10** dataset to study whether residual shortcut connections improve image classification performance.

## Project Goal
The main goal is to compare:
- **ResNet-18**
- **Plain CNN-18**

using the following evaluation metrics:
- Accuracy
- Precision
- Recall
- F1-score
- Confusion Matrix

## Tools Used
- Python
- PyTorch
- TorchVision
- scikit-learn
- Matplotlib
- Google Colab

## Dataset
We use the **CIFAR-10** dataset, which contains 60,000 color images divided into 10 classes:
- airplane
- automobile
- bird
- cat
- deer
- dog
- frog
- horse
- ship
- truck

The dataset is split into:
- 50,000 training images
- 10,000 test images

## Models
### 1. Plain CNN-18
A custom 18-layer plain convolutional neural network built in PyTorch without residual shortcut connections.

### 2. ResNet-18
A TorchVision ResNet-18 model adapted for CIFAR-10 by:
- changing the first convolution layer
- removing the early max-pooling layer
- changing the final fully connected layer to output 10 classes

Both models were trained from scratch with no pretrained weights.

## Repository Structure
```text
.
├── SZ_ML_proj.ipynb
├── results/p3
│   ├── training_loss.png
│   ├── test_accuracy.png
│   ├── confusion_matrix_plain.png
│   └── confusion_matrix_resnet.png
└── README.md
