---
title: "Fast Estimation and Inference of Functional Linear Regression with SGD"
excerpt: "nothing"
collection: portfolio
---

Functional data are widely used in many fields. When the sample size is extremely large, with tens of millions of observations and high 
dimensionality, traditional estimation and inference methods often require storing large datasets and computing the inverse of matrices, 
which can be infeasible. To achieve fast estimation and inference for functional linear regression, we developed an online learning method 
using the Stochastic Gradient Descent (SGD) algorithm. Compared to the Bootstrap method, the SGD method performs more efficiently and
accurately. For a functional linear regression:
$$Y_{i} = \alpha + \int x_{i}(t)\beta(t)dt + \epsilon_{i}$$
We can use basis expansion to represent $$\beta(t) = \sum_{l=1}^{d} B_{l}(t)\theta_{l} = \mathbb{B}^{\prime}\theta$$\\


