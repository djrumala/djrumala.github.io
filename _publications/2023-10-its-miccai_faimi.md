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


### About this research
In medical image analysis, we often encounter longitudinal data, where subjects have multiple scans over different time of visits. However, this aspect is often overlooked, leading to biases in AI models, such as over-optimistic results due to data leakage from improper procedures.

Our study focuses on assessing how the data splitting strategy during cross-validation affects data leakage when applying deep learning models to longitudinal data. Specifically, we used 3D CNNs for Alzheimer's Disease (AD) classification with longitudinal brain MRI data.

Our findings revealed that certain data splitting strategies caused data leakage, resulting in identity confounding. This means that models learned to identify subject or identity information along with diagnostic features. While these models performed well during cross-validation, they didn't generalize effectively to new subjects in the hold-out data.

To gain insights into the patterns learned by these models, we used GradCAM visualization on the hold-out data, revealing the presence of shortcuts, possibly due to identity confounding.


<br>

# Evaluation Scheme

### Data Splitting Strategies

- Subject-wise Splitting
- Record-wise Splitting
- Late Splitting


### Toy Example for the data splitting strategies for longitudinal data
<img src="/images/2023-its-miccai_faimi/toy_ex.jpg"  style="max-height: 1000px">

<br>

# GradCAM Visualization

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
