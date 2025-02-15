# Oral Cancer Detection

This project implements a pipeline for detecting oral cancer using an EfficientNetB3 deep learning model. The pipeline includes data preprocessing, model training, and evaluation, designed for a dataset with two classes: "normal" and "OSCC" (Oral Squamous Cell Carcinoma).

## Prerequisites

1. Python 3.7 or later
2. Install required Python packages:

```bash
pip install tensorflow numpy pandas matplotlib scikit-learn
```

## Model Architecture

The model is based on the EfficientNetB3 architecture, pre-trained on ImageNet, with the following modifications:
- Flatten layer
- Dense layers with ReLU activation
- Dropout for regularization
- Output layer with softmax activation for classification

## Training

The script uses the following training pipeline:
- Data generators for efficient data loading
- Adam optimizer with a learning rate of `1e-4`
- Early stopping to prevent overfitting
- Model checkpointing to save the best model

### Evaluation
After training, the model is evaluated on the test set, and metrics like accuracy, confusion matrix, and classification report are generated.

## Results

The final performance metrics will be printed to the console and visualized using:
- Confusion matrix (heatmap)
- Classification report (precision, recall, F1-score)

## Customization

- **Data Augmentation**: Adjust the `ImageDataGenerator` settings for additional augmentations if needed.
- **Model Parameters**: Modify the architecture, optimizer, or hyperparameters to experiment with performance.