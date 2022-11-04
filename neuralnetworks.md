---
layout: page
mathjax: true
permalink: /neural_networks/
---
# Neural networks

## Hyperparameters 
Examples of hyperparameters in a neural network are
- Number of hidden units
- Learning rate
- Batch size (the number of sub samples given to the network after which parameter update happens. A good default for batch size might be 32. Also try 32, 64, 128, 256, and so on.
- Number of epochs (the number of times the whole training data is shown to the network while training)

There are many activation functions, but we will only consider the four most known (non-linear) activation functions
\begin{enumerate}
    \item Sigmoid (logistic):
    \begin{align*}
        \sigma(z) = \frac{1}{1 + e^{-z}}
    \end{align*}
    where the derivative is
    \begin{align*}
        \sigma'(z) = \sigma(z) ( 1 - \sigma(z)).
    \end{align*}
    \item Tanh (hyperbolic)
    \begin{align*}
        \sigma(z) = \text{tanh}(x) = \frac{2}{1 + e^{-2z}} - 1
    \end{align*}
    where the derivative is
    \begin{align*}
        \sigma'(z) = 1 - \sigma^2(z).
    \end{align*}
    \item ReLU is very often used due to its simplicity and fast computation. It takes the form
    \begin{align*}
        \sigma(z) = \max(0,z)
    \end{align*}
    where the derivative is
    \begin{align*}
        \sigma'(z) = 
        \begin{cases}
            0 \quad \text{ for } z < 0\\ 1 \quad \text{ for } z \geq 0
        \end{cases}
    \end{align*}
    The issue with this activation function is that all negative values become zero. To fix this, we can use the Leaky ReLU, which adds a small term 
    \begin{align*}
        -\alpha x,\quad \alpha > 0.
    \end{align*}
    Leaky ReLU can then be written as
    \begin{align*}
        \sigma(z) = \max(-\alpha x, x)
    \end{align*}
    \item \textbf{Softmax} is a special activation function use for output neurons. It normalizes outputs for each class between 0 and 1, and returns the probability that the input belongs to a specific class.
\end{enumerate}
