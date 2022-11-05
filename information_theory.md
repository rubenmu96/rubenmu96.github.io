---
layout: page
mathjax: true
permalink: /information_theory/
---

## Information theory


## Entropy
Entropy is the measure of uncertainty of a random variable or the amount of information required to describe a variable


$$H(X) = - \sum_{i=1}^N p(x_i) \log_2 p(x_i)$$

The unit of entropy is bit (since $$\log_2$$). If you observe the formula, entropy is entirely dependent on the probability of the random variable and not on the value of x itself. There is a negative sign in front of the formula, making it perpetually positive or 0. If entropy is 0, there is no new information to be gained.

The largest entropy will occur when the probability of all the events are the same. 

## Joint and conditional entropy

The joint entropy is given by

$$
    H(X,Y) = - \sum_i \sum_j p(x_i,y_j) \log_2 p(x_i,y_j).
$$

The joint entropy represents the amount of information needed on average to specify the value of two discrete random variables. The \textbf{conditional entropy} is given by

$$
    H(Y|X) = -\sum_i \sum_j p(x_i,y_j) \frac{p(x_i,y_j)}{p(x_i)}
$$

The conditional entropy indicates how much extra information you still need to supply on average to communicate $$Y$$ given that the other party knows $$X$$.

### Mutual information

Mutual information is a measure of the amount of information that one random variable contains about another random variable. Alternatively, it can be defined as the reduction in uncertainty of one variable due to the knowledge of the other. 

Consider two random variables $$X$$ and $$Y$$ with a joint probability mass function $$p(x,y)$$ and marginal probability mass function $$p(x)$$ and $$p(y)$$. The mutual information $I(X;Y)$ is the relative entropy between the joint distribution and the product distribution $$p(x) p(y)$$,

$$
    I(X;Y) = \sum_{x \in X} \sum_{y \in Y} p(x,y) \log \frac{p(x,y)}{p(x) p(y)}
$$

We can also express mutual information using entropy

$$
    I(X;Y) = H(X) - H(X|Y) = H(Y) - H(Y|X).
$$

We see that mutual information is the reduction in the uncertainty of $$X$$ due to the knowledge of $$Y$$. 
