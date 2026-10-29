# Pneumonia Detection from Chest X-Ray Images Using Deep Learning

## Project Overview

Developed an image classification pipeline to distinguish between normal and pneumonia-positive chest X-ray images using deep learning. The project explores a custom Convolutional Neural Network (CNN) and transfer learning with MobileNetV2 to evaluate their effectiveness for medical image classification.

The workflow covers exploratory data analysis, image preprocessing, model development, transfer learning, fine-tuning, and performance evaluation using multiple classification metrics.

## Business Problem

Pneumonia detection from chest X-ray images is an important medical imaging application. This project investigates how deep learning can learn visual patterns from labeled X-ray images and support automated image classification.

The primary objective was to develop and evaluate a binary classification model that distinguishes between:

- **NORMAL:** Chest X-ray images labeled as normal.
- **PNEUMONIA:** Chest X-ray images labeled as pneumonia.

This is an educational machine learning project and is not intended for clinical diagnosis or treatment decisions.

## Technical Approach

### 1. Exploratory Data Analysis
- Analyzed the dataset structure and class distribution.
- Inspected sample images and identified class imbalance.
- Evaluated the data requirements for an image classification workflow.

### 2. Image Preprocessing
- Resized images to a consistent input resolution.
- Prepared image tensors and applied appropriate pixel preprocessing.
- Created training, validation, and test datasets.
- Maintained preprocessing consistency between model training and inference.

### 3. Custom CNN Development
- Built a CNN to learn image features through convolutional and pooling operations.
- Trained and evaluated the model as a baseline deep learning approach.
- Used validation performance to assess model learning.

### 4. Transfer Learning with MobileNetV2
- Initialized MobileNetV2 with ImageNet-pretrained weights.
- Added a custom classification head for binary prediction.
- Froze the pretrained backbone during initial training.
- Fine-tuned selected backbone layers using a low learning rate.

### 5. Model Evaluation
Evaluated the final fine-tuned model using accuracy, precision, recall, ROC-AUC, loss, and a confusion matrix. These metrics provided a broader assessment than accuracy alone, particularly given the imbalance between the two classes.

## Results

The fine-tuned MobileNetV2 model achieved the following results on the held-out test dataset:

| Evaluation Metric | Result |
|---|---:|
| Accuracy | 97.61% |
| Precision | 98.35% |
| Recall | 98.51% |
| ROC-AUC | 98.76% |
| Test Loss | 0.0812 |

The confusion matrix showed 182 correctly classified normal images, 595 correctly classified pneumonia images, 10 normal images incorrectly classified as pneumonia, and 9 pneumonia images incorrectly classified as normal.

These results demonstrate strong classification performance on the evaluated dataset but do not establish clinical validity or generalization to other patient populations.

## Technology Stack

- **Language:** Python
- **Deep Learning Framework:** TensorFlow and Keras
- **Model Architecture:** Custom CNN, MobileNetV2
- **Data Processing:** NumPy
- **Visualization:** Matplotlib
- **Development Environment:** Jupyter Notebook, Visual Studio Code
- **Version Control:** Git and GitHub

## Key Contributions

- Designed an end-to-end workflow for chest X-ray image classification.
- Compared a custom CNN approach with pretrained MobileNetV2.
- Implemented transfer learning and selective fine-tuning.
- Evaluated model performance using multiple classification metrics.
- Prepared an inference workflow for classifying individual X-ray images.
- Organized the project for reproducibility and portfolio demonstration.

## Key Learnings

This project strengthened my understanding of convolutional neural networks, transfer learning, fine-tuning, image preprocessing, binary classification metrics, and model evaluation. It also highlighted the importance of class imbalance, consistent preprocessing, and independent validation when developing machine learning systems.

## Future Enhancements

- Evaluate additional architectures such as EfficientNet and ResNet.
- Add Grad-CAM visualizations to investigate the image regions influencing predictions.
- Assess model calibration and performance on independent datasets.
- Improve experiment tracking and reproducibility.
- Develop an interface for educational inference demonstrations.

## Repository

**GitHub:** https://github.com/ArjunSingh11994/CNN_Pneumonia-Detection

**Author:** Arjun Singh

**Project Category:** Deep Learning | Computer Vision | Medical Image Classification

**Disclaimer:** This project is intended for educational and research purposes only. It is not a clinically validated diagnostic system.
