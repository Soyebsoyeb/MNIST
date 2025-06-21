MNIST (Modified National Institute of Standards and Technology database) is the most famous benchmark dataset in computer vision and machine learning, consisting of handwritten digit images.

Key Characteristics:
Content: 70,000 grayscale images of handwritten digits (0-9)
60,000 training examples
10,000 test examples

Image Format:
28×28 pixel resolution (784 dimensions)
Grayscale (single channel) with pixel values 0-255
Classes: 10 (digits 0 through 9)
Difficulty: Considered a "solved" problem with modern techniques achieving >99% accuracy



A convolutional neural network (CNN) implementation for classifying handwritten digits from the MNIST dataset using Deep Learning

## Overview
This project implements a CNN model that achieves ~99% accuracy on the MNIST dataset. The MNIST dataset contains 60,000 training images and 10,000 test images of handwritten digits (0-9).


## Features
- Simple and clean implementation using TensorFlow/Keras
- Data loading and preprocessing pipeline
- CNN model with:
  - Two convolutional layers
  - Max pooling layers
  - Fully connected layers
- Training visualization
- Model evaluation on test set



Results

The model typically achieves:
Training accuracy: ~99%
Validation accuracy: ~98-99%
Test accuracy: ~98-99%





Model Architecture

Model: "sequential"
_________________________________________________________________
 Layer (type)                Output Shape              Param #   
=================================================================
 conv2d (Conv2D)             (None, 26, 26, 32)        320       
                                                                 
 max_pooling2d (MaxPooling2D  (None, 13, 13, 32)       0         
 )                                                               
                                                                 
 conv2d_1 (Conv2D)           (None, 11, 11, 64)        18496     
                                                                 
 max_pooling2d_1 (MaxPooling  (None, 5, 5, 64)         0         
 2D)                                                             
                                                                 
 flatten (Flatten)           (None, 1600)              0         
                                                                 
 dense (Dense)               (None, 128)               204928    
                                                                 
 dense_1 (Dense)             (None, 10)                1290      
                                                                 
=================================================================
Total params: 225,034
Trainable params: 225,034
Non-trainable params: 0
_________________________________________________________________



Primary Source (Used in this Project)
Source: Built-in Keras Datasets
Method: Automatically downloaded when using keras.datasets.mnist.load_data()
Download Location: ~/.keras/datasets/mnist.npz on your local machine
Features:

Already split into training (60,000) and test (10,000) sets
Pre-formatted as NumPy arrays
Automatically handles download and caching








