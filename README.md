# Neural Network from Scratch

This project implements a neural network from scratch for binary classification using backpropagation.

## Loss Function

The cross-entropy loss with L2 regularization is defined as:


$$
L = -\frac{1}{N} \sum_{i=1}^{N} \log \left( \hat{y}_{i,y_i} \right) + \frac{\lambda}{2} \left( \|W_1\|^2 + \|W_2\|^2 \right)
$$



Where:
- $N$ is the number of examples
- $\hat{y}_{i,y_i}$ is the predicted probability for the correct class
- $\lambda$ is the regularization parameter

## Architecture
- Input Layer
  -  The input to the network is a matrix of shape (n_samples, n_features), where n_samples is the number of data samples, and n_features is the number of input features (attributes) in the data.
- Hidden Layer
  -  The number of neurons in the hidden layer is n_hidden_units. This layer uses the tanh activation function, which transforms the linear sum of inputs to values in the range (-1, 1).
The output from the hidden layer is a matrix of shape (n_samples, n_hidden_units).
- Output Layer
  - The output of the network is a matrix of shape (n_samples, n_classes), where n_classes is the number of classes the model needs to classify. The activation function in this layer is softmax.

