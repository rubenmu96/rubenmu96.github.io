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


<math xmlns="http://www.w3.org/1998/Math/MathML" display="block">
  <mi>H</mi>
  <mo stretchy="false">(</mo>
  <mi>X</mi>
  <mo stretchy="false">)</mo>
  <mo>=</mo>
  <mo>&#x2212;</mo>
  <munderover>
    <mo data-mjx-texclass="OP">&#x2211;</mo>
    <mrow data-mjx-texclass="ORD">
      <mi>i</mi>
      <mo>=</mo>
      <mn>1</mn>
    </mrow>
    <mi>N</mi>
  </munderover>
  <mi>p</mi>
  <mo stretchy="false">(</mo>
  <msub>
    <mi>x</mi>
    <mi>i</mi>
  </msub>
  <mo stretchy="false">)</mo>
  <msub>
    <mi>log</mi>
    <mn>2</mn>
  </msub>
  <mo data-mjx-texclass="NONE">&#x2061;</mo>
  <mi>p</mi>
  <mo stretchy="false">(</mo>
  <msub>
    <mi>x</mi>
    <mi>i</mi>
  </msub>
  <mo stretchy="false">)</mo>
</math>

The unit of entropy is bit (since $\log_2$). If you observe the formula, entropy is entirely dependent on the probability of the random variable and not on the value of x itself. There is a negative sign in front of the formula, making it perpetually positive or 0. If entropy is 0, there is no new information to be gained.

The largest entropy will occur when the probability of all the events are the same. 

### Mutual information
