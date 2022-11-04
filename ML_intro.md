

## Metrics in regression

#### MSE
The mean squared error (MSE) is given by
$$
    \text{MSE} = \frac{1}{n} \sum_{j=1}^n (y_j - \hat{y}_j)^2.
$$
where $y_j$ is the ground truth and $y_j$ is the predicted value. MSE is useful when we have outliers in the dataset. 

#### RMSE
$$
    \text{RMSE} = \sqrt{\frac{1}{n} \sum_{j=1}^n (y_j - \hat{y}_j)^2}.
$$

#### MAE
$$
    \text{MAE} = \frac{1}{n} \sum_{j=1}^n |y_j - \hat{y}_j|.
$$

#### Hinge loss
Hinge loss is primarily used with Support Vector Machine (SVM) Classifiers with class labels -1 and 1. Hinge Loss not only penalizes the wrong predictions but also the right predictions that are not confident.
$$
    J = \max(0,1-y\times f(x))
$$
