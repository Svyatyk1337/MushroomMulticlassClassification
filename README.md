# Image Classification Using Transfer Learning

This project implements an image classification pipeline leveraging transfer learning with ResNet50. The dataset comprises labeled images for training, validation, and testing. The project processes images, trains a ResNet50 model, and evaluates its performance. Fine-tuning the model was also explored but yielded poorer results compared to transfer learning.

---

## Project Overview

### Key Features:
1. **Dataset Preprocessing**:
   - Images are resized to 224x224 and normalized using ImageNet standards.
   - Training images undergo augmentations like random rotation and horizontal flipping.

2. **Custom Dataset and DataLoader**:
   - Implemented a custom dataset class for efficient data handling.
   - Training, validation, and test datasets are split and loaded using PyTorch's `DataLoader`.

3. **Transfer Learning**:
   - The ResNet50 model pre-trained on ImageNet is fine-tuned by replacing the final fully connected layer to classify into 10 categories.
   - The model is optimized using Adam and trained for 15 epochs.

4. **Model Training and Validation**:
   - Training is monitored using loss and accuracy metrics.
   - Validation is performed after every epoch, with results visualized in loss and accuracy plots.

5. **Fine-Tuning**:
   - Further fine-tuning of all layers was explored by unfreezing ResNet50's layers. However, this approach led to overfitting and worse performance, so it is not recommended.

6. **Performance Visualization**:
   - Training and validation loss and accuracy are plotted for detailed performance analysis.

---

### Key Results:
- **Transfer Learning**: Achieved high training and validation accuracy (~98% and ~89%, respectively).
- **Fine-Tuning**: Performance degraded compared to transfer learning due to overfitting.

---

### Training Example:
Loss and accuracy metrics were logged for each epoch, as shown below:
- **Epoch 1**: Train Accuracy: 66.68%, Validation Accuracy: 81.01%
- **Epoch 15**: Train Accuracy: 98.92%, Validation Accuracy: 89.45%

---

This project demonstrates the power of transfer learning for efficient and effective image classification with limited data.
