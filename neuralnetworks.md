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
- Batch size (the number of sub samples given to the network after which parameter update happens. A good default for batch size can be 32.
- Number of epochs (the number of times the whole training data is shown to the network while training)

## Activation functions
Activation functions can be divided into two categories
- Linear activation functions
- Non-linear activation functions

Non-linear activation functions makes it easier to adapt to the variation in the data. 

- Sigmoid: 
$$\sigma(z) = \frac{1}{1 + e^{-z}}$$ 
with derivative 
$$\sigma'(z) = \sigma(z) ( 1 - \sigma(z))$$
- Tanh (or hyperbolic): 
$$\sigma(z) = \text{tanh}(x) = \frac{2}{1 + e^{-2z}} - 1$$ with derivative $$\sigma'(z) = 1 - \sigma^2(z)$$.


## Weights
To prevent the gradients of the network’s activations from vanishing or exploding, good weights should follow the principles:
- The mean of the activations should be zero.
- The variance of the activations should stay the same across every layer.

### Xavier
A common way to initialize the weights are using the Xavier weight initialization. The weights are distributed using a uniform probability distribution, in the range $$(-1 / \sqrt{n}, 1 / \sqrt{n})$$, where $$n$$ is the number of inputs to the node. 

We can also consider normalized Xavier weight initialization. We then consider the range $$(- \sqrt{6} / \sqrt{n+m}, \sqrt{6} / \sqrt{n + m})$$, where $$n$$ is the number of nodes in the previous laayer and $$m$$ is the number of nodes in the current layer. 

### He
The He weight initialization is calculated using a Gaussian probability distribution with mean $$0$$ and std of $$\sqrt{2/n}$$.

## Bias

The bias allows us to shift the activation function to the left or right. 

### Bias trick
The bias trick is to include the bias in the weights. We then expand the input vector by one row with value $$1$$. The advantage of the bias trick is that you don't have to deal with it when doing forward and backward propagation.

## Overfitting and underfitting
A big issue when training a neural network is that we may experience overfitting or underfitting. That is, the performance between the training set and the validation/test set are different. 

### Overfitting

Overfitting occurs when the model performs well on the training data, but starts to see patterns in the noise of the training set, which are not relevant. Then it will generalize poorly on unseen data. 

A way to get overfitting is to have a small dataset or using a large network. 

### Underfitting


## Optimizers

### SGD
To find the minimum, we can use the Gradient descent, given by

$$
    w = w - \alpha \nabla_w J_n(w)
$$

where $$\alpha$$ is the learning rate. If $$\alpha$$ is too small, gradient descent can be slow. If $$\alpha$$ is too large, gradient descent can overshoot the minimum. It may fail to converge, or even diverge. Gradient descent can converge to a local minimum, even with the learning rate $$\alpha$$ is fixed, so there is no need to take smaller steps. 

##### Algorithm

- Initialize weights randomly $$\sim N(0,\sigma^2)$$
- Loop until convergence:
    - Compute gradient $$\frac{\partial J(w)}{\partial w}$$
    - Update weights $$w \rightarrow w - \eta \frac{\partial J(w)}{\partial w}$$
- Return weights 

### Adam
Adam is an adaptive optimizer, meaning each parameter (the weights and biases) will have its own learning rate. 


1. It is computationally efficient and has little memory requirement
2. It it invariant to diagonal rescaling of the gradients
3. Adam works well in practice as compared to other stochastic optimization methods


## Forward and backward pass

The forward pass takes the inputs, passes them through the network and allows each neuron to react to a fraction of the input. Neurons generate their outputs and pass them on to the next layer, until eventually the network generates an output. The forward propagation formula is given by

$$
    a_k^{[l]} = g\bigg(\sum_{j=1}^{n^{[l-1]}} w_{jk}^{[l]} a_j^{[l-1]} + b_k^{[l]}\bigg)
$$
