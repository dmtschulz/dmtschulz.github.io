---
title: 'Bias vs. Variance'
date: 2025-11-27
permalink: /posts/2025/11/bias-variance/
tags:
  - model-bias
  - machine-learning
  - model-evaluation
---
![Bias vs Variance](/images/blog/bias_variance.jpg)
======

![Bias vs Variance](/images/blog/bias_variance.jpg)

Imagine a dartboard. Each dart represents a prediction of a model for the same input $$x_0$$.

Different darts appear because the model is trained on different datasets sampled from the same distribution. The location where a dart lands is the model's prediction for that particular $$x_0$$.

- **Bias (shift or offset)** — the distance between the true value $$y_0$$ (the center of the dartboard) and the average position of all darts.  
- **Variance (spreading)** — how much the darts spread around their own mean, regardless of $$y_0$$.

In other words:  
- Each dart represents a prediction $$\hat{y}(x_0)$$ from the **same model** trained on **different datasets**.
- Bias measures the difference between the **average prediction of the model** and the true value $$y_0$$.
- Variance measures how scattered the predictions are around their mean. 

The total expected squared error of a model at a point $$x_0$$ can be decomposed as:

$$
\mathbb{E}\Big[(\hat{y}(x_0) - y_0)^2\Big] 
= \underbrace{(\mathbb{E}[\hat{y}(x_0)] - y_0)^2}_{\text{Bias}^2} 
+ \underbrace{\mathbb{E}[(\hat{y}(x_0) - \mathbb{E}[\hat{y}(x_0)])^2]}_{\text{Variance}} 
+ \underbrace{\sigma_\epsilon^2}_{\text{Irreducible error}}
$$

Where:  
- $$\hat{y}(x_0)$$ — prediction of the model for input $$x_0$$
- $$y_0$$ — true value at $$x_0$$
- Bias — squared difference between the mean prediction and the true value  
- Variance — spread of predictions around their mean  
- $$\sigma_\epsilon^2$$ — noise inherent in the data that cannot be reduced  

![Bias vs Variance](/images/blog/Bias_and_variance_contributing_to_total_error.png)
