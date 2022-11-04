---
layout: page
mathjax: true
permalink: /page1/
---

# Machine learning

## Information theory


## Entropy
Entropy is the measure of uncertainty of a random variable or the amount of information required to describe a variable


$$H(X) = - \sum_{i=1}^N p(x_i) \log_2 p(x_i)$$

The unit of entropy is bit (since $\log_2$). If you observe the formula, entropy is entirely dependent on the probability of the random variable and not on the value of x itself. There is a negative sign in front of the formula, making it perpetually positive or 0. If entropy is 0, there is no new information to be gained.

The largest entropy will occur when the probability of all the events are the same. 

### Mutual information
