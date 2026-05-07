# SebaZahraa-MLproj
project for intro to machine learning course.

# Comparing Plain CNN and ResNet Models at Different Depths for CIFAR-10 Image Classification

This repository contains our Machine Learning course project.  
The project compares **Plain CNN** and **ResNet** models for image classification on the **CIFAR-10** dataset.
The main goal is to test whether **residual/shortcut connections** help more when the network becomes deeper.

using the following evaluation metrics:
- Accuracy
- Precision
- Recall
- F1-score
- Confusion Matrix

In this project, we compare models at two different depths:
- 18 layers
- 56 layers

  ## Models Compared

We trained and evaluated four models:
|    Model      |  Description                                 |
|---------------|----------------------------------------------|
| Plain CNN-18  | A manually built plain CNN with 18 layers    |
| ResNet-18     | TorchVision ResNet-18 adjusted for CIFAR-10  |
| Plain CNN-56  | A manually built plain CNN with 56 layers    |
| ResNet-56     | A manually built CIFAR-style ResNet-56       |


## Tools Used
- Python
- PyTorch
- TorchVision
- scikit-learn
- Matplotlib
- Google Colab
TorchVision was used for loading CIFAR-10 and for the ResNet-18 model.  

## Dataset
We used the **CIFAR-10** dataset.
CIFAR-10 contains:
- 60,000 images total
- 50,000 training images
- 10,000 testing images
- 10 classes: airplane, automobile, bird, cat, deer, dog, frog, horse, ship, and truck


## Training Setup
All models were trained using the same general setup:
- Dataset: CIFAR-10
- Epochs: 20
- Loss function: Cross-Entropy Loss
- Optimizer: Adam
- Evaluation after each epoch using the test set
One epoch means the model goes through the full training set once.  
Since we used 20 epochs, each model saw the full training set 20 times.

## Evaluation Metrics
We evaluated the models using:
- Accuracy
- Precision
- Recall
- F1-score
- Training loss curves
- Test accuracy curves
- Confusion matrices
Accuracy gives the overall performance, while precision, recall, F1-score, and confusion matrices help show class-level behavior and mistakes.


## Final Results
Final results after 20 epochs on CIFAR-10:
|    Model      |  Accuracy  |  Precision  |  Recall  |  F1-score |
|---------------|-----------:|------------:|---------:|----------:|
| Plain CNN-18  | 86.10%     | 86.31%      | 86.10%   | 85.90%    |
| ResNet-18     | 90.96%     | 91.14%      | 90.96%   | 90.97%    |
| Plain CNN-56  | 63.01%     | 64.08%      | 63.01%   | 62.32%    |
| ResNet-56     | 83.80%     | 84.44%      | 83.80%   | 83.22%    |


## Main Findings
The results showed that ResNet performed better than Plain CNN at both depths.
For the 18-layer models, ResNet-18 performed slightly better than Plain CNN-18.
For the 56-layer models, the difference was much larger. Plain CNN-56 struggled during training and achieved much lower accuracy, while ResNet-56 stayed much more stable and accurate.
This supports the main idea from the original ResNet paper: residual connections help deeper networks train more effectively.

## Important Note
ResNet-18 achieved the highest accuracy overall in our experiment.  
This does not mean the 56-layer experiment failed.
The purpose of the 56-layer experiment was not to prove that deeper is always better. The purpose was to test whether residual connections help when the network becomes deeper.
The comparison showed that ResNet-56 performed much better than Plain CNN-56 at the same depth.


## Repository Structure
```text
.
├── SZ_ML_proj -final.ipynb
├── SZ_ML_proj.ipynb
├── seba_zahraa_ML_phase3.pdf
├── seba_zahraa_ML_proj -final.pdf
├── results/p3
│   ├── training_loss.png
│   ├── test_accuracy.png
│   ├── confusion_matrix_plain.png
│   └── confusion_matrix_resnet.png
├── results/p4
└── README.md

