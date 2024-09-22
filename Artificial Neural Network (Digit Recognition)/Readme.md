# Neural Network from Scratch with Backpropagation

This repository contains a custom implementation of a simple Artificial Neural Network (ANN) built from scratch using Python and NumPy. The network is designed with one hidden layer and utilizes the backpropagation algorithm for training. This implementation features manual weight initialization, forward propagation, backpropagation, and model evaluation.

## Overview

### 1. **Architecture**
The neural network is composed of:
- **Input Layer**: The number of input neurons corresponds to the size of the input features.
- **Hidden Layer**: A customizable hidden layer with user-defined size. 
- **Output Layer**: The number of neurons in the output layer corresponds to the number of output classes.

The network uses the **sigmoid** activation function for both the hidden and output layers.

### 2. **Backpropagation Algorithm**
The model is trained using the backpropagation algorithm, which consists of:
- **Forward Pass**: The input data is propagated through the network to compute the output.
- **Backward Pass**: The error is computed as the difference between the predicted and actual output. This error is then backpropagated through the network to update the weights using gradient descent.

### 3. **Key Features**
- **Manual Initialization**: Weights and biases are manually initialized to random values between -0.5 and 0.5.
- **Training with Epochs**: The model is trained over multiple epochs to minimize the error.
- **Learning Rate**: A configurable learning rate is used for weight updates during training.
- **Accuracy Calculation**: The accuracy of the model is evaluated on test data after each epoch.

## Code Structure

### 1. **Neural Network Class**
- **Initialization**: The class constructor initializes the layer sizes, learning rate, weights, and biases.
- **Sigmoid Activation**: The sigmoid activation function is used for non-linearity in both forward and backward propagation.
- **Forward Propagation**: The `forward()` method performs the forward pass by computing weighted sums and applying the sigmoid activation function.
- **Backward Propagation**: The `backward()` method calculates the error and updates the weights using the backpropagation algorithm.
- **Training**: The `train()` method trains the model over a given number of epochs, printing accuracy and error after each epoch.
- **Evaluation**: The `evaluate()` method tests the model on unseen data, providing the accuracy.

### 2. **Training Process**
For each epoch:
1. **Forward Pass**: The input is passed through the layers of the network, computing the outputs.
2. **Backward Pass**: The difference between the predicted output and the actual output is used to compute gradients, which are used to update the weights.
3. **Accuracy Check**: The model is evaluated on test data, and accuracy is printed after each epoch.

### 3. **Dataset**

The EMNIST dataset is an extension of the classic MNIST dataset and contains handwritten character data. In this project, the **EMNIST Letters and digits** subset is used, which includes grayscale images of handwritten letters and digits. Each image is 28x28 pixels in size.


The objective is to classify these images into one of the 26 English letters or one of the 10 digits.


