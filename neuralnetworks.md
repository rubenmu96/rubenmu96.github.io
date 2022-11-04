---
layout: page
use_math: true
permalink: /neural_networks/
---
# Neural networks

## Hyperparameters 
Examples of hyperparameters in a neural network are
- Number of hidden units
- Learning rate
- Batch size (the number of sub samples given to the network after which parameter update happens. A good default for batch size might be 32. Also try 32, 64, 128, 256, and so on.
- Number of epochs (the number of times the whole training data is shown to the network while training)


## Activation functions

- Sigmoid: $\sigma(z) = \frac{1}{1 + e^{-z}}$ with derivative $\sigma'(z) = \sigma(z) ( 1 - \sigma(z))$
- Tanh (or hyperbolic): $\sigma(z) = \text{tanh}(x) = \frac{2}{1 + e^{-2z}} - 1$
