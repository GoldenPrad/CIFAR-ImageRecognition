# CIFAR-10 Image Classification with Convolutional Neural Networks (CNNs)

This repository contains code for building and training a Convolutional Neural Network (CNN) on the CIFAR-10 dataset using TensorFlow and Keras.

## Overview

The CIFAR-10 dataset consists of 60,000 32x32 color images in 10 classes, with 6,000 images per class. The classes are: airplane, automobile, bird, cat, deer, dog, frog, horse, ship, and truck.

### Requirements

- Python 3.x
- TensorFlow 2.x
- Keras
- NumPy
- Matplotlib

## Training the Model

### Preparing the Data
 - Setup: Imports TensorFlow and sets up necessary tools. Defines image dimensions, classes, and labels.
 - Data: Loads CIFAR-10 dataset, creates backups, and preprocesses labels. Checks dataset shapes.
 - Visualization & Normalization: Displays image details, converts to float32, and normalizes pixel values.
 - Label Encoding: Converts labels to one-hot encoding using Keras utilities.

### Building the Network
 - Model Setup: Imports TensorFlow/Keras components, defines epochs and batch_size, and initializes a Sequential model for image classification.
 - Convolutional Layers: Builds multiple Conv2D layers with increasing filter sizes and 'relu' activation, incorporating MaxPooling2D, Dropout, and BatchNormalization for feature extraction.
 - Additional Layers: Continues with more Conv2D, MaxPooling2D, Dropout, and BatchNormalization layers to further refine feature maps.
 - Output Layers: Adds a Flatten layer to reshape data, followed by Dense layers for classification tasks, ending with a softmax activation to predict class probabilities.
 - Summary: Prints a concise summary of the complete model architecture detailing layer types, parameters, and output dimensions.

### Compiling and Training the Model
 - Compile Model: Configures the model with Adam optimizer, categorical crossentropy loss function, and accuracy metric.
 - Training: Trains the model using training data, specified batch size and epochs, with validation data for evaluation, and shuffling enabled.
 - Evaluation: Evaluates the model performance on test data and prints the test accuracy.
 - Saving: Saves the trained model in both HDF5 (.h5) and TensorFlow SavedModel (.keras) formats for future use.

## Testing the Model

### Basic Testing
 - Ensuring the model was working properly against test data set as well as outside images.
   
### Test 1
 - Running a square image of a frog, or an airplane or any of the other classes through the network, and seeing what it returns.

### Test 2
 - Running a randomly generated image through the network to view any bias with what it predicts.

### Test 3
 - Testing the network with some random images from the test_images set. 
