# Checkers Game with LMS Rule Implementation

## Introduction

This repository contains the code for a 10x10 checkers game implemented using the **Least Mean Squares (LMS)** rule as described in Tom Mitchell's book *"Machine Learning"*. The LMS rule is used to train a model to predict moves in the game based on experience, adjusting weights to minimize prediction errors.

## LMS Rule Overview

The **Least Mean Squares (LMS)** rule is a method used to adjust weights in a linear model to minimize the error between predicted and actual outputs. In the context of this checkers game, LMS is used to improve the model's predictions of good moves based on game states.

### LMS Update Formula

The LMS rule adjusts weights as follows:

```
w_i(t+1) = w_i(t) + η × (d(t) - o(t)) × x_i(t)
```

Where:
- `w_i(t+1)` represents the updated weight at time `t+1`
- `w_i(t)` represents the weight at time `t`
- `η` represents the learning rate
- `d(t)` represents the desired output at time `t`
- `o(t)` represents the predicted output at time `t`
- `x_i(t)` represents the input at time `t`


The goal of LMS is to minimize this error by adjusting the weights based on the observed error during the game.

### Feature Representation

Each board state in the checkers game is represented by a set of features. For instance:
- Number of pieces each player has.
- Number of kings on the board.
- Number of available moves.

The model learns the weight of each feature to predict better moves over time.

## Checkers Game Rules

The checkers game is played on a 10x10 board with two players:
- **Black** and **White**. 
- Each player starts with 20 pieces.
- The objective is to capture all of the opponent's pieces or block them so they cannot move.

### Game Setup

- The pieces are placed on alternating dark squares of the first four rows for each player.
- **Black** moves first.

### Move Rules

- Pieces move diagonally forward to an empty square.
- A piece can capture an opponent's piece by jumping over it diagonally into an empty square.

### Kings

- When a piece reaches the opponent's last row, it is crowned a **King** and can move both forward and backward diagonally.

## Future Updates

- Implementation of more advanced features such as advanced reinforcement learning for enhanced move prediction.

- Visualization of the learning process by tracking weight changes over multiple games.



