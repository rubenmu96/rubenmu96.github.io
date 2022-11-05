---
layout: page
mathjax: true
permalink: /image_processing/
---

# Image processing

## Histogram

The brightness histogram $$h_f(z)$$ of an image provides the frequency of the brightness value of $$z$$ in the image - the histogram of an image with $$L$$ gray-levels is represented by a one-dimensional array with $$L$$ elements.


Algorithm:
1. Assign zero values to all elements of the array $$h_f$$
2. For all pixels $$(x,y)$$ of the image $$f$$, increment $$h_f(f(x,y))$$ by $$1$$


## Cross-correlation
$$
    G[i,j] = \sum_{u=-k}^k \sum_{v = -k}^k h[u,v] F[i+ u, j + v]    
$$


## Convolution
$$
    G[i,j] = \sum_{u=-k}^k \sum_{v = -k}^k h[u,v] F[i - u, j - v]    
$$

We can also use the cross-correlation formula, given that we flip the kernel. 

## Image gradient

The gradient of an image is defined by

$$
    \nabla f = \bigg(\frac{\partial f}{\partial x},\frac{\partial f}{\partial y}\bigg),
$$

where the gradient direction is given by

$$
    \theta = \tan^{-1}\bigg(\frac{\partial f}{\partial y} / \frac{\partial f}{\partial x}\bigg).
$$

The amount of change is given the gradient magnitude

$$
    ||\nabla f|| = \sqrt{\bigg(\frac{\partial f}{\partial x}\bigg)^2 + \bigg(\frac{\partial f}{\partial y}\bigg)^2}.
$$


### Laplacian
The simplest isotropic derivative operator is the Laplacian, which, for a function/image $$f(x,y)$$ of two variables, is defined as

$$
    \nabla^2 f = \frac{\partial^2 f}{\partial x^2} + \frac{\partial^2  f}{\partial y^2}.
$$

In the $$x$$-direction we have

$$
    \frac{\partial^2 f}{\partial x^2} =  f(x+1,y) - 2f(x,y) + f(x-1,y)
$$

and in the $$y$$-direction we have

$$
    \frac{\partial^2 f}{\partial y^2} =  f(x,y+1) - 2f(x,y) + f(x,y-1).
$$

We therefore end up with the following expression for the Laplacian of $$f$$,

$$
    \nabla^2 f = f(x+1,y) + f(x,y+1) - 4f(x,y) + f(x-1,y)  + f(x,y-1).
$$
