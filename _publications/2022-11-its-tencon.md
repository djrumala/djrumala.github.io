---
title: "The Effect of Noisy and Blurry Data on Deep Learning: Application in Brain Image Classification"
permalink: /publications/noisy-and-blurry
author_profile: true
date: 2022-11-04
venue: 'IEEE Region 10 Conference (TENCON), 2022'
category: conferences
---
Dewinda Julianensi Rumala<br>
<a href="https://ieeexplore.ieee.org/abstract/document/9977591/"  target="_blank"><i class="fas fa-graduation-cap">Publication</i></a>
<a href="/files/pub/2022-its-tencon/small-poster.pdf"  target="_blank"><i class="fas fa-file-image">Poster</i></a>
<br>

This work has been presented at IEEE TENCON 2022 in Hongkong.

<a href="/files/pub/2022-its-tencon/small-poster.pdf" target="_blank" class="btn"><i class="fa fa-scroll"> Download Poster</i></a>


# Introduction
<!-- * Longitudinal data is often not considered
* Little attention is given to data handling procedure when tackling longitudinal data
* Deep learning model performance tends to be  -->

* Convolutional Neural Networks (CNN) is one of the best Deep Learning algorithms commonly used for computervision tasks, including medical image analysis

* CNN can learn the representational features from images starting from the lower to complex features. However, noisy data can affect the generalization of the networks, which is often found in medical images, such as Magnetic Resonance Imaging (MRI). 

* In this research, we want to see the relation between noisy and blurry data and the performance of CNN models


# Methods

* We investigate a clinical task of brain image classification, specifically for anatomical classification of the brain using MRI. For this classification task, we classify the brain into Class A: Upper part of the brain, Class B : Middle part of the brain, and Class C: Lower part of the brain.

* We build three CNN models to evaluate three different scenarios: original data, blurry data, noisy data.


# Results and Analysis

* The developed CNN 1 is more powerful in identifying original data, however the accuracy difference between each CNN model is not significant.

* The accuracy of CNN 1 falls drastically when evaluating blurry and noisy data. Meanwhile CNN 2 shows better performance in classifying blurry data, but performs not good on noisy data.

* On average, CNN 3 with deeper layers shows superior performance than the other models in the classification task using noisy and blurry data.



# Conclusion
* Noisy and blurry data can hurt the CNN performance by 16.00% and 47.67%, respectively, on average. 
* CNN Models with deeper layers and smaller convolutional kernels that are trained on an ideal epoch can deliver better outcome when dealing with blurry and noisy data.


# References
1. S. Gupta, A. Gupta, “Dealing with Noise Problem in Machine Learning Data-sets: A Systematic Review”, Procedia Computer Science, Volume 161, 2019.
2. Jose A. Saez, Julian Luengo, Francisco Herrera"Evaluating the classifier behavior with noisy data considering performance and robustness: the Equalized Loss of Accuracy measure.“ Neurocomputing, 176 (2016), pp. 26-35
3. Luis PF Garcia, Andre CPLF de Carvalho, Ana C. Lorena, "Effect of label noise in the complexity of classification problems“ Neurocomputing, 160 (2015), pp. 108-119
4. Pelletier, Charlotte et al. (2017), “A Effect of Training Class Label Noise on Classification Performances for Land Cover Mapping with Satellite Image Time Series. Remote Sensing”, 9: 173.



# Acknowledgement
This paper is partially funded by UCE AIHes of Sepuluh Nopember Institute of Technology and Indonesia Endowment Fund for Education under the scheme of Riset Inovatif Produktif (RISPRO) - Invitasi 2019 Grant.
