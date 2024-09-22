# Perceptron for Solving AND, OR, and XOR Problems

This repository contains Python implementations of single-layer and multi-layer perceptrons for solving basic logic gate problems (AND, OR, XOR). 

## Overview

### 1. **Single-Layer Perceptron**
The single-layer perceptron is used to solve problems that are linearly separable, such as the AND and OR gates. This model is trained using simple weight adjustments based on a learning rate and number of epochs.

### 2. **Multi-Layer Perceptron (MLP)**
The multi-layer perceptron is used to solve non-linearly separable problems, like XOR. XOR cannot be solved using a single perceptron due to its non-linear nature, so we implement a multi-layer perceptron with multiple steps, breaking down the XOR into simpler linearly separable operations.

## Usage

### AND Gate
The single-layer perceptron is trained with the truth table of an AND gate and predicts the correct output using the trained weights.

### OR Gate
Similarly, the OR gate is implemented using the single-layer perceptron with a separate truth table and weights.

### XOR Gate
The XOR gate is solved using a multi-layer perceptron, which breaks the XOR function into simpler operations:
- `Z1 = A'B`
- `Z2 = AB'`
- The final output is computed as `Z = Z1 + Z2`

The multi-layer model trains three separate perceptrons, one for each sub-operation (Z1, Z2, and Z).

## How It Works
- Each perceptron consists of an activation function that predicts the output based on weighted inputs.
- During training, the perceptron adjusts its weights iteratively based on the prediction error, following the Perceptron Learning Rule.
- The XOR problem is solved by training two sub-perceptrons for intermediate calculations (Z1, Z2), and a final perceptron to combine them into the final XOR output.

## Requirements
- Python 3
- NumPy
