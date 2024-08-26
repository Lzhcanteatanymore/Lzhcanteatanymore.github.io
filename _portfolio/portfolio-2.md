---
title: "Fast Inference of Functional Linear Regression with SGD for Ultra-Large Dataset"
excerpt: "[demonstration](https://lzhcanteatanymore.github.io/files/Demo.pdf)
[code](https://github.com/Lzhcanteatanymore/FDA-with-SGD-optimization)
The error decreases through learning<br/><img src='/images/error.png'>comparison of computing times between our method and the Bootstrap method<br/><img src='/images/Comparison.png'>
"
collection: portfolio
---


To start with, first, I simulate the original function as y = sin(x) + 0.5 * sin(3 * x) + sigma. Then with Fourier basis functions to fit it, I choose stochastic data from the sample and calculate the gradient, and make the parameter descent with the gradient.

Imagine there is a fanctional data flow. Each time, we can capture 100 data samples, and we call it a data block. To simplify the analysis, I assume there is 1000 data blocks in total. In each block, I use SGD algorithm to fit the function. Theoratically, with the learning process, the fit will be better and better. 

To test whether the learning process can actually improve the efficiency and accuracy. I draw the fit errors in 1000 blocks. The error decreases through learning, and become stable aroud the 200th learning <br/><img src='/images/error.png'>

To advance our research, we apply the SGD algorithm to Functional Linear Regression, particularly to address scenarios involving ultra-large datasets where traditional methods may be infeasible due to memory constraints and slow computation. Our method demonstrates superior efficiency and accuracy compared to other widely used approaches, such as the Bootstrap method, in similar situations.

You can find additional [demonstrations](https://lzhcanteatanymore.github.io/files/Demo.pdf) of the algorithm and theories, including how to update the learning rate and penalized parameters, here.
Here is a comparison of computing times between our method and the Bootstrap method. As the dataset size increases to ultra-large scales, our method demonstrates significantly faster performance.<br/><img src='/images/Comparison.png'>
