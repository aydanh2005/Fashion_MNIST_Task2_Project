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

````markdown
```bash
pip install -r requirements.txt

````
## Final Results

| Model | Training Accuracy | Test Accuracy | Training Time |
|---|---:|---:|---:|
| CNN | 93.18% | 90.47% | 88.40 seconds |
| Random Forest | 100.00% | 87.53% | 14.48 seconds |

The Random Forest achieved perfect training accuracy but lower test accuracy, indicating stronger overfitting. The CNN achieved higher test accuracy and better generalization.

## Selected Visual Results

### Fashion-MNIST Sample Images

![Fashion-MNIST sample images](results/fashion_mnist_examples.png)

### CNN Test Confusion Matrix

![CNN test confusion matrix](results/cnn_test_confusion_matrix.png)

### Random Forest Test Confusion Matrix

![Random Forest test confusion matrix](results/rf_test_confusion_matrix.png)

### CNN Training and Validation Accuracy

![CNN training and validation accuracy](results/cnn_training_validation_accuracy.png)

The complete confusion matrices, precision and recall tables, and supporting outputs are available in the [`results`](results) folder.
