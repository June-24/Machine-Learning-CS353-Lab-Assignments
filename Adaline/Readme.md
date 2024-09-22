# ADALINE Learning for XNOR, OR, and AND Gates

This repository contains an implementation of the ADALINE (Adaptive Linear Neuron) algorithm to solve logic gate problems, specifically the XNOR, OR, and AND gates.

## Overview

### 1. **ADALINE Model**
ADALINE is a type of artificial neuron that uses a linear activation function. It is different from the basic perceptron in that it updates weights based on a continuous-valued output, rather than binary outputs. It uses gradient descent to minimize the error between the predicted and actual output, making it suitable for solving both linearly separable and non-linearly separable problems.

### 2. **Logic Gates Solved**
- **XNOR Gate**: The XNOR gate is non-linearly separable and requires the ADALINE model to correctly classify it.
- **OR Gate**: The OR gate is linearly separable and can be easily solved by the ADALINE model.
- **AND Gate**: The AND gate is also linearly separable and can be solved using ADALINE.

## How It Works
1. **Model Training**: The ADALINE model is trained on the truth table of each gate using gradient descent to minimize the mean squared error between the predicted and actual outputs.
2. **Weights Update**: During training, the model updates its weights based on the error using the ADALINE learning rule, which is a continuous-valued counterpart of the perceptron learning rule.


## Results
The ADALINE model successfully learns to solve the XNOR, OR, and AND gates. The final weights after training allow the model to correctly classify all inputs for these gates.

## Usage
To run the model and train it on the XNOR, OR, and AND gates:
- Ensure you have Python 3 installed.
- Install the required packages (NumPy).
- Execute the code to train the ADALINE model on the respective gate's truth table and observe the results.

## Requirements
- Python 3
- NumPy


