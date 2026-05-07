Handwritten Digit Recognition — CNN with Real-World Image Prediction

![Python](https://img.shields.io/badge/Python-3.x-blue)  ![Framework](https://img.shields.io/badge/Framework-TensorFlow%20%2F%20Keras-blue)  ![Task](https://img.shields.io/badge/Task-Image%20Classification-blue)  ![Dataset](https://img.shields.io/badge/Dataset-MNIST-blue)  
## Overview
Builds a Convolutional Neural Network (CNN) to classify handwritten digits (0-9) on the MNIST dataset and extends the model to classify real-world handwritten digit images using OpenCV for preprocessing. Demonstrates the full pipeline from training a deep learning model to deploying it on new real-world data.
## Problem Statement
Recognise handwritten digits from images — a foundational computer vision task with applications in postal services, cheque processing, and form digitisation. This project goes beyond the standard benchmark by applying the trained model to photographs of real handwritten digits.

## Dataset
- **Name:** MNIST Handwritten Digits Dataset
- **Source:** Built into Keras — loaded automatically via
  `keras.datasets.mnist.load_data()` — no download needed
- **Training Samples:** 60,000 greyscale images
- **Test Samples:** 10,000 greyscale images
- **Image Size:** 28×28 pixels, single channel (greyscale)
- **Classes:** 10 digits — `0, 1, 2, 3, 4, 5, 6, 7, 8, 9`
- **Format:** NumPy arrays loaded directly from Keras
- **Pixel Value Range:** 0–255 (normalised to 0.0–1.0 
  before training)

> No dataset download required. Running the notebook will 
> automatically download MNIST on the first run.

## Approach
-	Loaded and normalised MNIST dataset (60,000 training, 10,000 test images of 28x28 pixels).
-	Designed a multi-layer CNN architecture with Conv2D, MaxPooling, Dropout, Flatten, and Dense layers.
-	Trained using Adam optimiser and sparse categorical cross-entropy loss.
-	Evaluated with accuracy metrics, confusion matrix, and classification report.
-	Extended to real-world images: loaded external digit photos using OpenCV, converted to greyscale, resized to 28x28, normalised, and predicted using the trained model.
-	Visualised predictions by overlaying predicted labels on test images.
## Results

| Property         | Details                                                         |
| ---------------- | --------------------------------------------------------------- |
| **Dataset**      | MNIST (Modified National Institute of Standards and Technology) |
| **Training Set** | 60,000 grayscale images                                         |
| **Test Set**     | 10,000 grayscale images                                         |
| **Image Size**   | 28 × 28 pixels                                                  |
| **Classes**      | 10 digits (0–9)                                                 |


## Technologies
Python, TensorFlow, Keras, NumPy, OpenCV, Matplotlib, Scikit-Learn
## How to Run

```bash
git clone https://github.com/OyelolaIbrahim/handwritten-digit-recognition-cnn.git
cd handwritten-digit-recognition-cnn
pip install tensorflow opencv-python numpy matplotlib scikit-learn
jupyter notebook handwritten_digit_cnn.ipynb
```


