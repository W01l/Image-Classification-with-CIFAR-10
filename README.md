# Image-Classification-with-CIFAR-10
A deep learning model built with TensorFlow/Keras to classify images into 100 categories using the CIFAR-100 dataset. The model uses a Convolutional Neural Network (CNN) architecture with batch normalization, dropout regularization, and L2 weight decay to improve generalization. 

## Overview
A deep learning model built with TensorFlow/Keras to classify images into 100 categories using the CIFAR-100 dataset.

## Dataset
- **CIFAR-100** dataset containing 60,000 32x32 color images
- 100 classes with 600 images per class
- Split into 40,000 training, 10,000 validation, and 10,000 test images

## Model Architecture
- 8 Convolutional layers with increasing filters (32 → 64 → 128 → 256)
- Batch Normalization after each convolutional layer
- Max Pooling layers for spatial downsampling
- Dropout regularization (0.2 → 0.3 → 0.4 → 0.5)
- L2 weight decay (0.0001) to prevent overfitting
- Fully connected Dense layer with 100 output classes

## Training
- **Optimizer:** Adam (learning rate: 0.0005)
- **Loss:** Categorical Crossentropy
- **Batch Size:** 64
- **Epochs:** 100 (with early stopping)
- **GPU:** Tesla P100-PCIE-16GB

## Callbacks
- **EarlyStopping:** Stops training if no improvement after 40 epochs
- **ReduceLROnPlateau:** Reduces learning rate by 0.5 if no improvement after 10 epochs

## Data Augmentation
- Random rotation (15°)
- Width and height shifts (10%)
- Horizontal flipping

## Requirements
```bash
pip install tensorflow keras numpy matplotlib scikit-learn kagglehub
```

## Usage
```python
# Load the model
import tensorflow as tf
model = tf.keras.models.load_model('cifar100_model.keras')

# Make a prediction
predictions = model.predict(image)
```

## Results
| Metric | Score |
|--------|-------|
| Training Accuracy | TBD |
| Validation Accuracy | TBD |
| Test Accuracy | TBD |

