---
title: "Applying SGD Algorithm to Functional Data"
excerpt: "SGD fit compared with the ture function<br/><img src='/images/IMG_5994.PNG'>"
collection: portfolio
---

I write a code with R to apply SGD algorithm to functional data analysis, and compare the fit errors to find the best parametor.

You can find my [code](https://github.com/Lzhcanteatanymore/FDA-with-SGD-optimization) here.
This code shows the SGD optimization applied in FDA(nonparametic regression), I simulate a 1000 elements sample and the original function as y = sin(x) + 0.5 * sin(3 * x) + sigma. Then with Fourier basis functions, I choose stochastic data from the sample and calculate the gradient, and make the parameter descent with the gradient.

this is the fit when I choose 50 stochastic data from the sample to optimization the regression
<br/><img src='/images/IMG_5994.PNG'>

Above I use SGD to optimazation the nonparameter regression with each experiment I choose 50 stochastic data from the sample, now I want to compare the loss when the number of data I choose was different from 10, 50, 100, 500. In the end, I depict a figure to vitually reflect the loss in different number of stochastic sample                         
<br/><img src='/images/IMG_5994.PNG'>

