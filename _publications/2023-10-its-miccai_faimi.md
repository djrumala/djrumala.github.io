---
layout: archive
title: "How You Split Matters: Data Leakage and Subject Characteristics Studies in Longitudinal Brain MRI Analysis"
permalink: /publications/how-you-split-matters
author_profile: true
date: 2023-09-01
venue: 'MICCAI FAIMI'
---
Dewinda Julianensi Rumala
<br>
<a href="https://arxiv.org/abs/2309.00350"  target="_blank"><i class="fas fa-file-pdf"> PDF</i></a>
<a href="https://github.com/djrumala/ADNI-processing"  target="_blank"><i class="fab fa-github"> Code</i></a>
<!-- Link to the publication/paper1 page -->
<br>


# Research Summary
In medical image analysis, we often encounter longitudinal data, where subjects have multiple scans over different time of visits. However, this aspect is often overlooked, leading to biases in AI models, such as over-optimistic results due to data leakage from improper procedures.

This study focuses on assessing how the data splitting strategy during cross-validation (CV) affects data leakage when applying deep learning models to longitudinal data. Specifically, this research used 3D CNNs for Alzheimer's Disease (AD) classification with longitudinal brain MRI data.

The findings revealed that certain data splitting strategies caused data leakage, resulting in identity confounding. This means that models learned to identify subject or identity information along with diagnostic features. While these models performed well during CV, they could not generalize effectively to new subjects in the hold-out data.

To gain insights into the patterns learned by these models, GradCAM visualization is utilized on the hold-out data, revealing the presence of shortcuts, possibly due to identity confounding.

## Introduction
<!-- * Longitudinal data is often not considered
* Little attention is given to data handling procedure when tackling longitudinal data
* Deep learning model performance tends to be  -->

* <b>Neglect of Longitudinal Data</b>: In medical image analysis, the significance of longitudinal data is often overlooked. Longitudinal data, with its repeated observations over time, holds a wealth of information critical for understanding changes and patterns over the progression of diseases.

* <b>Data Handling in Longitudinal Analysis</b>: Proper handling of longitudinal data is a crucial aspect that often receives inadequate attention. Inconsistent or improper data handling procedures can introduce biases and compromise the robustness and reliability of the results.

* <b>Deep Learning Performance Challenges</b>: Deep learning models, despite their high performance, can be misleading in the medical imaging domain. Biases, such as data leakage, can give overly optimistic results during evaluation, potentially leading to incorrect conclusions. Understanding and mitigating these challenges are vital for trustworthy AI-powered medical diagnoses.

## Methods
 
### Evaluation Scheme
Data Splitting Strategies during CV:
- Subject-wise Splitting
- Record-wise Splitting
- Late Splitting


<!-- ### Toy Example for the data splitting strategies for longitudinal data -->
<figure>
  <img src="/images/2023-its-miccai_faimi/toy_ex.jpg" alt="Illustration showing different data split strategies for longitudinal brain MRI: subject-wise, record-wise, and late splitting.">
  <figcaption>A toy example of different data split strategies for longitudinal brain MRI. (a) Subject-wise splitting groups all image scans based on the subjects into k-folds. (b) Record-wise splitting groups image scans based on different visit times into k-folds. (c) Late splitting groups image scans based on transformation technique into k-folds.</figcaption>
</figure>

## Results and Analysis

* Data Splitting Strategy Impact:
  * Data splitting strategy significantly influences model performance (P=0.0389).
  * Record-wise split excels during CV, closely followed by late split.
  * Surprisingly, subject-wise split performs poorest during CV but generalizes best to hold-out data.

* MRI Sequence Influence:
  * Choice between T1 and T2 MRI sequences does not significantly affect overall classification performance (P=0.7921).
  * Both sequences (T1 and T2) prove suitable for the three-way classification task of CN, MCI, and AD.

* Insights from GradCAM Visualization:
    * Certain data splitting strategies may lead to shortcut learning, potentially due to identity confounding.


### GradCAM Visualization

<img src="/images/2023-its-miccai_faimi/gradcam.jpg"  style="max-height: 500px">

### Gif Samples

<!-- | Data Type | Subject-wise Split  | Record-wise Split  | Late Split  |
|:---:| :---: | :---: | :---: |
|<span style="display:block;text-align:center;" rowspan="2"> AD |  <img src="/images/2023-its-miccai_faimi/GradCAM-auto_T1_DenseNet121_test-120_Ax.gif" width="200" height="200"> <br> [o] Correctly classified | <img src="/images/2023-its-miccai_faimi/GradCAM-record_T1_DenseNet121_test-120_Ax.gif" width="200" height="200"> <br> [o] Correctly classified| <img src="/images/2023-its-miccai_faimi/GradCAM-auto_T1_DenseNet121_test-120_Ax.gif" width="200" height="200"> <br> [o] Correctly classified|
| AD |  <img src="/images/2023-its-miccai_faimi/GradCAM-auto_T1_DenseNet121_test-75_Ax.gif" width="200" height="200"> <br> [x] Misclassified| <img src="/images/2023-its-miccai_faimi/GradCAM-late_T1_DenseNet121_test-75_Ax.gif" width="200" height="200"> <br> [x] Misclassified| <img src="/images/2023-its-miccai_faimi/GradCAM-auto_T1_DenseNet121_test-75_Ax.gif" width="200" height="200">  <br> [x] Misclassified| -->


<table>
  <tr>
    <td style="text-align: center;" > <b>Data Group</b></td>
    <td style="text-align: center;"><b>Subject-wise Split</b></td>
    <td style="text-align: center;"><b>Record-wise Split</b></td>
    <td style="text-align: center;"><b>Late Split</b></td>
  </tr>
  <tr> 
    <td rowspan="2" style="text-align: center;">CN</td>
    <td style="text-align: center;"><img src="/images/2023-its-miccai_faimi/GradCAM-auto_T1_DenseNet121_test-20_Ax.gif" width="200" height="200"> <br> [O] Correctly classified</td>
    <td style="text-align: center;"><img src="/images/2023-its-miccai_faimi/GradCAM-record_T1_DenseNet121_test-20_Ax.gif" width="200" height="200"> <br> [O] Correctly classified</td>
    <td style="text-align: center;"><img src="/images/2023-its-miccai_faimi/GradCAM-late_T1_DenseNet121_test-20_Ax.gif" width="200" height="200"> <br> [O] Correctly classified</td>
  </tr>
  <tr>
    <td style="text-align: center;"><img src="/images/2023-its-miccai_faimi/GradCAM-auto_T1_DenseNet121_test-15_Ax.gif" width="200" height="200"> <br> [X] Misclassified</td>
    <td style="text-align: center;"><img src="/images/2023-its-miccai_faimi/GradCAM-record_T1_DenseNet121_test-15_Ax.gif" width="200" height="200"> <br> [X] Misclassified</td>
    <td style="text-align: center;"><img src="/images/2023-its-miccai_faimi/GradCAM-late_T1_DenseNet121_test-15_Ax.gif" width="200" height="200"> <br> [X] Misclassified</td>
  </tr>
  <tr> 
    <td rowspan="2" style="text-align: center;">AD</td>
    <td style="text-align: center;"><img src="/images/2023-its-miccai_faimi/GradCAM-auto_T1_DenseNet121_test-120_Ax.gif" width="200" height="200"> <br> [O] Correctly classified</td>
    <td style="text-align: center;"><img src="/images/2023-its-miccai_faimi/GradCAM-record_T1_DenseNet121_test-120_Ax.gif" width="200" height="200"> <br> [O] Correctly classified</td>
    <td style="text-align: center;"><img src="/images/2023-its-miccai_faimi/GradCAM-late_T1_DenseNet121_test-120_Ax.gif" width="200" height="200"> <br> [O] Correctly classified</td>
  </tr>
  <tr>
    <td style="text-align: center;"><img src="/images/2023-its-miccai_faimi/GradCAM-auto_T1_DenseNet121_test-75_Ax.gif" width="200" height="200"> <br> [X] Misclassified</td>
    <td style="text-align: center;"><img src="/images/2023-its-miccai_faimi/GradCAM-record_T1_DenseNet121_test-75_Ax.gif" width="200" height="200"> <br> [X] Misclassified</td>
    <td style="text-align: center;"><img src="/images/2023-its-miccai_faimi/GradCAM-late_T1_DenseNet121_test-75_Ax.gif" width="200" height="200"> <br> [X] Misclassified</td>
  </tr>
</table>
<!-- Add more publications in a similar format -->


## Limitations
  * Generalization Challenges:
    * Limited generalization to hold-out data likely influenced by data variance in sensitive attributes (e.g., age and gender imbalance).

  * Robustness of Subject-Wise Split:
    * Despite a significant drop in performance, subject-wise splitting demonstrates relative robustness. Addressing potential underfitting by incorporating a more diverse subject pool could enhance this approach's performance.
    Subject-wise splitting strategy shows more robustness but still suffers from performance drops, possibly due to underfitting, which can be mitigated with a larger and more diverse dataset.


## Conclusions
* <b>How You Split Matters</b>: 
  * The choice of data splitting strategy during cross-validation significantly influences the performance and robustness of deep learning models in longitudinal medical image analysis.
* <b>Data Leakage and Identity Confounding</b>: 
  * Improper data splitting can lead to data leakage, causing identity confounding within the models. This compromises their generalization and can result in misleadingly optimistic performance assessments.
* <b>Shortcut Learning Revealed by GradCAM</b>: 
  * Visualization using GradCAM highlights potential shortcut learning in models, particularly from record-wise and late-wise splitting strategies. This suggests that models may learn unintended patterns during cross-validation.
* <b>Subject-Wise Split</b>: 
  * A Promising Approach: Subject-wise splitting demonstrates relative robustness and less vulnerability to data leakage compared to record-wise and late-wise strategies. However, challenges like underperformance indicate the need for further investigation, potentially with a larger and more diverse dataset.
* <b>Future Directions</b>: 
  * Addressing the observed limitations, future research should focus on refining data splitting strategies and exploring methods to improve model generalization. Incorporating a diverse dataset and balancing sensitive attributes could enhance model fairness and accuracy.

## References
1. Chaibub Neto, E., Pratap, A., Perumal, T.M., Tummalacherla, M., Snyder, P., Bot, B.M., Trister, A.D., Friend, S.H., Mangravite, L., Omberg, L.: Detecting the impact of subject characteristics on machine learning-based diagnostic applications. npj Digital Medicine 2(1), 99 (Oct 2019). [https://doi.org/10.1038/s41746-019-0178-x](https://doi.org/10.1038/s41746-019-0178-x){:target="_blank"}
2. Yagis, E., Atnafu, S.W., García Seco de Herrera, A., Marzi, C., Scheda, R., Giannelli, M., Tessa, C., Citi, L., Diciotti, S.: Effect of data leakage in brain MRI classification using 2D convolutional neural networks. Scientific Reports 11(1), 22544 (Nov 2021). [https://doi.org/10.1038/s41598-021-01681-w](https://doi.org/10.1038/s41598-021-01681-w){:target="_blank"}


## Acknowledgement
Special thanks to DGHERT Ministry of Education and Research Technology, Indonesia, Prof. I Ketut Eddy Purnama (Sepuluh Nopember Institut of Technology, Indonesia) and Prof. Tae-Seong Kim (Kyung Hee University, South Korea).