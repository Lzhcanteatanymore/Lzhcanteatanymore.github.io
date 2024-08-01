---
title: "Applying SGD Algorithm to Functional Data"
excerpt: "SGD fit compared with the ture function<br/><img src='/images/Rplot02.png'>
Loss under different number of stochastic data<br/><img src='/images/Rplot01.png'> fit function on a certain data block <br/><img src='/images/fit.png'> errors on the learning process<br/><img src='/images/error.png'>
[code](https://github.com/Lzhcanteatanymore/FDA-with-SGD-optimization)"
collection: portfolio
---

I write a code with R to apply SGD algorithm to functional data analysis, and compare the fit errors to find the best parametor.

You can find my [code](https://github.com/Lzhcanteatanymore/FDA-with-SGD-optimization) here.
This code shows the SGD optimization applied in FDA(nonparametic regression), I simulate a 1000 elements sample and the original function as y = sin(x) + 0.5 * sin(3 * x) + sigma. Then with Fourier basis functions, I choose stochastic data from the sample and calculate the gradient, and make the parameter descent with the gradient.

this is the fit when I choose 50 stochastic data from the sample to optimization the regression
<br/><img src='/images/Rplot02.png'>

Above I use SGD to optimazation the nonparameter regression with each experiment I choose 50 stochastic data from the sample, now I want to compare the loss when the number of data I choose was different from 10, 50, 100, 500. In the end, I depict a figure to vitually reflect the loss in different number of stochastic sample                         
<br/><img src='/images/Rplot01.png'>

Imagine there is a fanctional data flow. Each time, we can capture 100 data samples, and we call it a data block. To simplify the analysis, I assume there is 1000 data blocks in total. In each block, I use SGD algorithm to fit the function. Theoratically, with the learning process, the fit will be better and better. 

I draw a plot figure of 100000 samples(1000 blocks * 100 data samples)<br/><img src='/images/simulate.png'>

After 1000 times learning, I draw a fit function on a certain data block <br/><img src='/images/fit.png'>

To test whether the learning process can actually improve the efficiency and accuracy. I draw the fit errors in 1000 blocks. The error decreases through learning, and become stable aroud the 200th learning <br/><img src='/images/error.png'>
