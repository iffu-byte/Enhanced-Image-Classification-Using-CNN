# CIFAR-10 Image Classification Project

This project implements and compares multiple Deep Learning models using TensorFlow and Keras to classify images from the **CIFAR-10 dataset** into 10 distinct classes:
- Airplane, Automobile, Bird, Cat, Deer, Dog, Frog, Horse, Ship, Truck

## Project Architecture & Experiments

We designed, trained, and evaluated three core modeling architectures:

1. **Basic CNN**:
   - Simple Sequential architecture with two Convolutional layers and Max-Pooling.
   - Used as our baseline model.

2. **Enhanced CNN**:
   - Deeper Sequential model featuring `BatchNormalization`, customized `Dropout` rates for regularization, and padding to preserve spatial dimensions.
   - Utilized learning rate schedules via `ReduceLROnPlateau` and `EarlyStopping` callbacks.
   - **Performance:** Achieved the highest validation and test accuracy (~80.64%).

3. **Transfer Learning (MobileNetV2)**:
   - Leveraged weights pretrained on ImageNet.
   - Resized CIFAR-10 inputs (32x32) up to 96x96 to match the pretrained model requirements.
   - Includes a fine-tuning stage where the top 30 layers were unfrozen and optimized with a small learning rate (1e-5).

## Web Interface Demo
- The project integrates a user-friendly web interface powered by **Gradio**.
- Users can upload any image to instantly obtain classification predictions and confidence scores.

INTERN ID:CITS9576
