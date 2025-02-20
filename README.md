# Oral Cancer Detection

This project implements a deep learning pipeline for detecting Oral Squamous Cell Carcinoma (OSCC) using multiple deep learning models, including EfficientNetB3 and custom CNN architectures. The pipeline covers data preprocessing, augmentation, model training, evaluation, and inference.

## Prerequisites

``` bash
pip install -r requirements.txt
```

## Dataset

The dataset consists of two classes:

- Normal (Healthy Cell)
- OSCC (Oral Squamous Cell Carcinoma)

Images undergo preprocessing, including normalization, resizing (128x128), and augmentation (random flips, rotations, sharpening, and Gaussian filters). Class balancing techniques such as weighted loss functions are used to handle class imbalance.

## Model Architectures

Multiple models are implemented, including:

- EfficientNetB3 (pre-trained on ImageNet with custom layers)
- Custom CNN (built using PyTorch with BatchNorm and Dropout for regularization)

## Key Features

- **Image Augmentation:** General augmentations (flips, rotations) and advanced methods (Gaussian filters).
- **Optimizers & Learning Rate Schedulers:** Adam optimizer (lr=1e-4) with step-based and cosine annealing schedulers.
- **Loss Handling:** Uses class weighting to manage dataset imbalance.
- **Callbacks & Checkpoints:** Early stopping, model checkpointing, and learning rate adjustments.
- **Evaluation Metrics:** Accuracy, precision, recall, F1-score, and confusion matrix.

## Customization

- **Data Augmentation:** Modify the augmentation pipeline if needed.
- **Model Hyperparameters:** Adjust layers, dropout rates, and learning rate to experiment with performance.
- **Inference Pipeline:** Update inference pipeline to handle batch predictions.

## Evaluation

After training, the model is evaluated on the test set, and metrics like accuracy, confusion matrix, and classification report are generated.

## Results

The final performance metrics will be:
- Confusion matrix (heatmap)
- Classification report (precision, recall, F1-score)