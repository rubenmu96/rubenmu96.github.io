---
layout: page
mathjax: true
permalink: /ML_intro/
---

## Metrics in regression

#### MSE
The mean squared error (MSE) is given by

$$
    \text{MSE} = \frac{1}{n} \sum_{j=1}^n (y_j - \hat{y}_j)^2.
$$

where $$y_j$$ is the ground truth and $$y_j$$ is the predicted value. MSE is useful when we have outliers in the dataset. 

#### RMSE
$$
    \text{RMSE} = \sqrt{\frac{1}{n} \sum_{j=1}^n (y_j - \hat{y}_j)^2}.
$$

#### MAE
$$
    \text{MAE} = \frac{1}{n} \sum_{j=1}^n |y_j - \hat{y}_j.
$$

#### Hinge loss
Hinge loss is primarily used with Support Vector Machine (SVM) Classifiers with class labels -1 and 1. Hinge Loss not only penalizes the wrong predictions but also the right predictions that are not confident.

$$ 
    J = \max(0,1-y\times f(x))
$$

## Metrics in classification
- True Positives (TP): When we predict that someone is positive and the actual result is positive.
- False Positives (FP): When we predict that someone is positive and the actual result is negative.
- False Negatives (FN): When we predict that someone is negative and the actual result is positive.
- True Negatives (TN): When we predict that someone is negative and the actual result is negative.

Some of the different metrics are:
- Accuracy is the amount of correct predictions

$$
    \text{Accuracy} = \frac{\text{TP} + \text{TN}}{\text{TP} + \text{FN} + \text{FP} + \text{TN}}
$$

- Specificity is the percentage of correct predictions for the actual negatives

$$
    \text{Specificity} = \frac{\text{TN}}{\text{TN} + \text{FP}}
$$

- Recall is the fraction of relevant instances that are retrieved: What proportion of actual positives was identified correctly? Recall is a measure of how many relevant elements were detected.

$$
    \text{Recall} = \frac{\text{TP}}{\text{TP} + \text{FN}} = \frac{\text{TP}}{\text{all ground truth instances}}
$$
    
- Precision is the fraction of retrieved instances that are relevant: What proportion of positive identifications was actually correct? The precision of a model describes how many detected items are truly relevant

$$
    \text{Precision} = \frac{\text{TP}}{\text{TP} + \text{FP}} = \frac{\text{TP}}{\text{all predicted}}
$$

- F$$_1$$ is the harmonic mean of precision and recall

$$
    F_1 = 2\frac{\text{Precision} \cdot \text{Recall}}{\text{Precision} + \text{Recall}}
$$

- Average precision is the mean under the curve of the recall-precision curve. 


