# Recurrent Neural Network (RNN) Forward Propagation

This README provides an overview of the Python code that implements the forward propagation of a recurrent neural network (RNN). The RNN consists of a sequence of RNN cells, each performing a single forward step.

## Course Information

This project was done as an exercise in the Coursera course: [Sequence Models](https://www.coursera.org/learn/nlp-sequence-models).

## Table of Contents
- [Introduction](#introduction)
- [Functions](#functions)
  - [softmax](#softmax)
  - [rnn_cell_forward](#rnn_cell_forward)
  - [rnn_forward](#rnn_forward)

## Introduction
The code provided implements the forward propagation of an RNN using numpy. It includes three main functions: `softmax`, `rnn_cell_forward`, and `rnn_forward`. The RNN is designed to process sequences of input data through multiple time steps.

## Functions

### softmax
The `softmax` function computes the softmax activation of input values. It applies the exponentiation and normalization operations to convert a vector of real numbers into a probability distribution.

### rnn_cell_forward
The `rnn_cell_forward` function performs a single forward step of the RNN cell. Given an input data point at a specific time step, a previous hidden state, and the RNN cell's parameters, it calculates the next hidden state and the prediction for that time step. The calculations involve matrix multiplications and activation functions.

### rnn_forward
The `rnn_forward` function implements the forward propagation of the entire RNN. It takes a sequence of input data, an initial hidden state, and the RNN parameters as inputs. The function iterates over all time steps, invoking the `rnn_cell_forward` function at each step. The hidden states and predictions for each time step are stored and returned.

The code is organized as follows:
- The `rnn_forward` function initializes the necessary variables and loops over time steps.
- For each time step, the `rnn_cell_forward` function is called to compute the next hidden state and prediction.
- The hidden states and predictions are stored in arrays, and the caches containing intermediate values are collected.
- The final output includes the hidden states, predictions, and caches.

Please note that the code assumes that `numpy` is imported and properly configured for matrix operations.

For more details about the code implementation and usage, refer to the comments within the code itself.

---
