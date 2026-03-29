# Neural Network

## Overview

This project implements a **Neural Network from scratch using only NumPy**, without relying on high-level deep learning frameworks such as TensorFlow or PyTorch.

The goal of this project is to deeply understand how neural networks work internally by building every component manually, including forward propagation, loss calculation, backpropagation, and gradient descent.

---

## Features

*  Built entirely with **NumPy**
*  Manual implementation of:

  * Forward propagation
  * Backpropagation
  * Gradient descent
* Supports:

  * Dense (fully connected) layers
  * Multiple activation functions
  * Binary classification tasks
* Trained on:

  * AND / OR logic gates
  * XOR problem
*  Modular and extendable codebase

---

##  How It Works

### Forward Propagation

```
Z1 = X @ W1 + b1
A1 = activation(Z1)

Z2 = A1 @ W2 + b2
y_hat = activation(Z2)
```

---

### Loss Function (Binary Cross Entropy)

```
L = -1/n * Σ [ y log(y_hat) + (1 - y) log(1 - y_hat) ]
```

---

### Backpropagation

Output layer:

```
dZ2 = y_hat - y
dW2 = (A1.T @ dZ2) / m
db2 = sum(dZ2) / m
```

Hidden layer:

```
dA1 = dZ2 @ W2.T
dZ1 = dA1 * activation_derivative(A1)
dW1 = (X.T @ dZ1) / m
db1 = sum(dZ1) / m
```

---

### Parameter Update

```
W = W - learning_rate * dW
b = b - learning_rate * db
```

---

##  Project Structure

```
neural-network-from-scratch/
│
├── data/
├── notebooks/
│   ├── 01_perceptron_basics.ipynb
│   ├── 02_xor_network.ipynb
│
├── src/
│   ├── activations.py
│   ├── losses.py
│   ├── layers.py
│   ├── network.py
│
├── train_xor.py
├── requirements.txt
└── README.md
```

---

##  Results

### XOR Problem

Expected output:

```
Input    Prediction
[0, 0] → 0
[0, 1] → 1
[1, 0] → 1
[1, 1] → 0
```

The network successfully learns the XOR function, demonstrating the importance of hidden layers.

---

##  Installation

Clone the repository:

```
git clone https://github.com/your-username/neural-network-from-scratch.git
cd neural-network-from-scratch
```

Install dependencies:

```
pip install -r requirements.txt
```

---

##  Usage

Run XOR training:

```
python train_xor.py
```

---

##  Learning Objectives

This project was built to understand:

* How neural networks actually compute outputs
* The mathematics behind backpropagation
* Gradient descent optimization
* Why hidden layers are necessary
* How deep learning frameworks work internally

---

##  Future Improvements

* Add ReLU and Softmax support
* Implement optimizers (Momentum, Adam)
* Add mini-batch training
* Train on MNIST dataset
* Add model saving/loading
* Build a simple web interface

---

##  Key Insight

> This project intentionally avoids high-level frameworks to provide a deeper understanding of neural network fundamentals.

---

##  License

This project is open-source and available under the MIT License.

---

##  Acknowledgements

Built as part of a learning journey into deep learning, computer vision, and AI system design.
