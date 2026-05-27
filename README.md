
# Fashion-MNIST Classification Project

## Project Overview

This project compares two machine learning methods for classifying fashion product images from the Fashion-MNIST dataset:

1. Convolutional Neural Network (CNN)
2. Random Forest Classifier

The project was developed for Task 2: Classifying Fashion Products in the Computer Vision project report. The aim is to evaluate both models using accuracy, training time, confusion matrices, precision, recall, and worst-performing class analysis.

## Dataset

Fashion-MNIST contains 70,000 grayscale images of fashion products:

- 60,000 training images
- 10,000 test images
- 10 product categories
- Image size: 28 x 28 pixels
- Color format: grayscale

The classes are:

- T-shirt/top
- Trouser
- Pullover
- Dress
- Coat
- Sandal
- Shirt
- Sneaker
- Bag
- Ankle boot

## Models

### Convolutional Neural Network

The CNN uses convolutional layers, max-pooling layers, dense layers, dropout, and a softmax output layer. It is designed to learn spatial image features directly from the 28 x 28 grayscale images.

### Random Forest Classifier

The Random Forest classifier uses flattened image vectors with 784 pixel features per image. It serves as a classical machine learning baseline for comparison.

## Evaluation

The models were evaluated using:

- Training accuracy
- Test accuracy
- Training time
- Train and test confusion matrices
- Precision, recall, and F1-score
- Worst-performing class analysis

## Main Finding

The CNN showed better generalization performance and is recommended for production use in fashion product image classification. The Random Forest classifier was useful as a baseline model but showed signs of overfitting, with perfect training accuracy and lower test accuracy.

## Project Files

- Fashion_MNIST_Task2_Project.ipynb: full notebook with code, outputs, tables, and figures
- results/: saved confusion matrices, plots, and CSV result tables
- requirements.txt: required Python packages
- README.md: project documentation

## How to Run

1. Create or activate a Python environment.
2. Install the required dependencies listed in requirements.txt.
3. Open Fashion_MNIST_Task2_Project.ipynb in Jupyter Notebook or JupyterLab.
4. Run all cells from top to bottom.

## Author

Prepared as part of a Computer Vision project report.
