# Fashion-MNIST Classification: CNN vs Random Forest

## Project Overview

This project compares two machine learning approaches for classifying fashion product images from the Fashion-MNIST dataset:

1. Convolutional Neural Network (CNN)
2. Random Forest Classifier

The project was developed for **DLBAIPCV01 – Project: Computer Vision, Task 2: Classifying Fashion Products**. The objective is to evaluate both models using accuracy, training time, confusion matrices, precision, recall, and worst-performing class analysis.

## Research Question

Which model is more suitable for automatic fashion product classification: a Convolutional Neural Network or a Random Forest classifier?

## Dataset

Fashion-MNIST contains 70,000 grayscale images of fashion products:

- 60,000 training images
- 10,000 test images
- 10 classes
- Image size: 28 × 28 pixels
- Pixel values: 0–255 before normalization

The 10 classes are:

1. T-shirt/top
2. Trouser
3. Pullover
4. Dress
5. Coat
6. Sandal
7. Shirt
8. Sneaker
9. Bag
10. Ankle boot

## Methods

### CNN

The CNN uses convolutional layers, max-pooling layers, dense layers, dropout, and a softmax output layer. Images were normalized and reshaped to 28 × 28 × 1.

### Random Forest

The Random Forest classifier was trained on flattened 784-dimensional pixel vectors. It was used as a classical machine learning baseline for comparison with the CNN.

## Evaluation Metrics

The models were evaluated using:

- Training accuracy
- Test accuracy
- Training time
- Confusion matrices for train and test sets
- Precision and recall for train and test sets
- Worst-performing category analysis

## Key Results

The CNN achieved better generalization performance than the Random Forest classifier. The Random Forest reached perfect training accuracy but lower test accuracy, indicating stronger overfitting. Both models struggled most with visually similar upper-body clothing categories such as Shirt, Pullover, T-shirt/top, and Coat.

## Production Recommendation

The CNN is recommended for production use because it is better suited to image data and can learn spatial features such as edges, shapes, and local textures. The Random Forest classifier is useful as a baseline model but is less appropriate as the final production model because it relies on flattened pixel vectors.

## Repository Contents

- `Fashion_MNIST_Task2_Project.ipynb` — full notebook with code, outputs, figures, and analysis
- `requirements.txt` — Python dependencies
- `README.md` — project documentation
- result figures and CSV tables — confusion matrices, precision/recall tables, model comparison, and final summary

## How to Run

1. Clone or download the repository.
2. Create a Python environment.
3. Install dependencies:

```bash
pip install -r requirements.txt
