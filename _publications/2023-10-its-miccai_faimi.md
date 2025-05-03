---
title: "How You Split Matters: Data Leakage and Subject Characteristics Studies in Longitudinal Brain MRI Analysis"
permalink: /publications/how-you-split-matters
author_profile: true
date: 2023-09-01
venue: 'MICCAI FAIMI'
category: conferences
---
Dewinda Julianensi Rumala<br>
<a href="https://link.springer.com/chapter/10.1007/978-3-031-45249-9_23"  target="_blank"><i class="fas fa-graduation-cap">Publication</i></a>
<a href="https://arxiv.org/abs/2309.00350" target="_blank"><i class="fas fa-file-pdf">Preprint</i></a>
<a href="https://github.com/djrumala/ADNI-processing" target="_blank"><i class="fab fa-github">Code</i></a>
<a href="/files/pub/2023-its-miccai_faimi/small-poster.pdf" target="_blank"><i class="fas fa-file-image">Poster</i></a>
<a href="https://youtu.be/czkG9Oqts6o?si=hxehYYp1BXiyDLLo&t=6637" target="_blank"><i class="fas fa-play-circle">Video</i></a>
<br>

<!-- Link to the publication/paper1 page -->
[_MICCAI FAIMI 2023_](https://faimi-workshop.github.io/2023-miccai/){:target="_blank"}

This work has been honored with the <b>Best Poster Presentation Award</b> at MICCAI FAIMI 2023 workshop.

<a href="/files/pub/2023-its-miccai_faimi/small-poster.pdf" target="_blank" class="btn"><i class="fa fa-scroll"> Download Poster</i></a>
<a href="/files/pub/2023-its-miccai_faimi/best_poster_award.pdf"  target="_blank" class="btn"><i class="fa fa-award"> View Award Certificate</i></a> 


<!-- # Research Summary -->
<!-- In medical image analysis, we often encounter longitudinal data, where subjects have multiple scans over different time of visits. However, this aspect is often overlooked, leading to biases in AI models, such as over-optimistic results due to data leakage from improper procedures.

This study focuses on assessing how the data splitting strategy during cross-validation (CV) affects data leakage when applying deep learning models to longitudinal data. Specifically, this research used 3D CNNs for Alzheimer's Disease (AD) classification with longitudinal brain MRI data.

The findings revealed that certain data splitting strategies caused data leakage, resulting in identity confounding. This means that models learned to identify subject or identity information along with diagnostic features. While these models performed well during CV, they could not generalize effectively to new subjects in the hold-out data.

To gain insights into the patterns learned by these models, GradCAM visualization is utilized on the hold-out data, revealing the presence of shortcuts, possibly due to identity confounding. -->

# Introduction
<!-- * Longitudinal data is often not considered
* Little attention is given to data handling procedure when tackling longitudinal data
* Deep learning model performance tends to be  -->

* <b>Neglect of Longitudinal Data</b>: In medical image analysis, the significance of longitudinal data is often overlooked. Longitudinal data, with its repeated observations over time, holds a wealth of information critical for understanding changes and patterns over the progression of diseases, offering insights into treatment efficacy.

* <b>Data Handling in Longitudinal Analysis</b>: Proper handling of longitudinal data is a crucial aspect that often receives inadequate attention. Inconsistent or improper data handling procedures can introduce biases and compromise the robustness and reliability of the results, even in 3D-based medical image analysis.

* <b>Deep Learning Performance Challenges</b>: Deep learning models, despite their high performance, can be misleading in the medical imaging domain. Biases, such as data leakage, can give overly optimistic results during evaluation, potentially leading to incorrect conclusions. Understanding and mitigating these challenges are vital for trustworthy AI-powered medical diagnoses.

# Methods

* Deep Learning model: 3D CNN [(DenseNet121)](https://github.com/ZFTurbo/classification_models_3D)
* Datasets: 3D Longitudinal T1-weighted and T2-weighted MRI from [ADNI](https://adni.loni.usc.edu/) (Dataset statistics see Table S1)
* Data Processing: [CAT12](https://andysbrainbook.readthedocs.io/en/latest/CAT12/CAT12_Overview.html) with VBM pipeline 
* Purpose: Three-way classification (CN, MCI, and AD)

<b>Table S1.</b> Dataset Statistics. The ratio of females to males and the average age are based on the number of images rather than the number of subjects.

<table>
<thead>
  <tr>
    <td rowspan="2" style="text-align: center;" > <b>Collection</b></td>
    <td rowspan="2" style="text-align: center;"><b>Data Group</b></td>
    <td rowspan="2" style="text-align: center;"><b>No of Subjects</b></td>
    <td rowspan="2" style="text-align: center;"><b>Female / Male </b></td>
    <td rowspan="2" style="text-align: center;"><b>Age </b></td>
    <td colspan="2" style="text-align: center;"><b>No of Scans </b></td>
  </tr>
  <tr> 
    <td style="text-align: center;"><b>Before Augmentation</b></td>
    <td style="text-align: center;"><b>After Augmentation</b></td>
  </tr>
</thead>
  <tr> 
    <td rowspan="3" style="text-align: center;">5-Fold data</td>
    <td style="text-align: center;">CN</td>
    <td style="text-align: center;">41</td>
    <td style="text-align: center;">85/65</td>
    <td style="text-align: center;">76.68 ± 4.15</td>
    <td style="text-align: center;">150</td>
    <td style="text-align: center;">300</td>
  </tr>
  <tr> 
    <td style="text-align: center;">MCI</td>
    <td style="text-align: center;">45</td>
    <td style="text-align: center;">50/100</td>
    <td style="text-align: center;">74.19 ± 8.57</td>
    <td style="text-align: center;">150</td>
    <td style="text-align: center;">300</td>
  </tr>
  <tr> 
    <td style="text-align: center;">AD</td>
    <td style="text-align: center;">25</td>
    <td style="text-align: center;">30/20</td>
    <td style="text-align: center;">74.22 ± 8.90</td>
    <td style="text-align: center;">50</td>
    <td style="text-align: center;">300</td>
  </tr>
  <tr> 
    <td rowspan="3" style="text-align: center;">Hold-out data</td>
    <td style="text-align: center;">CN</td>
    <td style="text-align: center;">8</td>
    <td style="text-align: center;">17/13</td>
    <td style="text-align: center;">74.81 ± 3.13</td>
    <td style="text-align: center;">30</td>
    <td style="text-align: center;">-</td>
  </tr>
  <tr> 
    <td style="text-align: center;">MCI</td>
    <td style="text-align: center;">11</td>
    <td style="text-align: center;">8/22</td>
    <td style="text-align: center;">75.42 ± 7.26</td>
    <td style="text-align: center;">30</td>
    <td style="text-align: center;">-</td>
  </tr>
  <tr> 
    <td style="text-align: center;">AD</td>
    <td style="text-align: center;">7</td>
    <td style="text-align: center;">16/1</td>
    <td style="text-align: center;">78.26 ± 6.52</td>
    <td style="text-align: center;">30</td>
    <td style="text-align: center;">-</td>
  </tr>
</table>

## Evaluation Scheme
Data Splitting Strategies during CV:
- Subject-wise Splitting
- Record-wise Splitting
- Late Splitting


<!-- ### Toy Example for the data splitting strategies for longitudinal data -->
<figure>
  <img src="/images/2023-its-miccai_faimi/toy_ex.jpg" alt="Illustration showing different data split strategies for longitudinal brain MRI: subject-wise, record-wise, and late splitting.">
  <figcaption>A toy example of different data split strategies for longitudinal brain MRI. (a) Subject-wise splitting groups all image scans based on the subjects into k-folds. (b) Record-wise splitting groups image scans based on different visit times into k-folds. (c) Late splitting groups image scans based on transformation technique into k-folds.</figcaption>
</figure>


## Training Setups
<b>Table S2.</b> Overview of the parameters used across all experiments: the learning rate was reduced using the ReduceLROnPlateau scheduler from TensorFlow by a factor of 0.1 when validation loss did not decrease after 10 epochs. Adam was used as the optimizer.

| Parameter | Value | 
|:--------|:-------:|
| Learning rate   | 0.0001   |
| Epsilon   | 0.0001   |
| Beta 1   | 0.9 |
| Beta 2   | 0.99   |
| Epoch   | 100  |
| Batch size   | 24  |

# Results and Analysis

* Data Splitting Strategy Impact:
  * Data splitting strategy significantly influences model performance (P=0.0389).
  * Record-wise split excels during CV, closely followed by late split.
  * Surprisingly, subject-wise split performs poorest during CV but generalizes best to hold-out data.

* MRI Sequence Influence:
  * Choice between T1 and T2 MRI sequences does not significantly affect overall classification performance (P=0.7921).
  * Both sequences (T1 and T2) prove suitable for the three-way classification task of CN, MCI, and AD.

* Insights from GradCAM Visualization:
    * Presence of shortcut learning found frem certain data splitting strategies: record-wise and late splits.


## GradCAM Visualization

<img src="/images/2023-its-miccai_faimi/gradcam.jpg"  style="max-height: 500px">

### Gif Samples

<!-- | Data Type | Subject-wise Split  | Record-wise Split  | Late Split  |
|:---:| :---: | :---: | :---: |
|<span style="display:block;text-align:center;" rowspan="2"> AD |  <img src="/images/2023-its-miccai_faimi/GradCAM-auto_T1_DenseNet121_test-120_Ax.gif" width="200" height="200"> <br> [o] Correctly classified | <img src="/images/2023-its-miccai_faimi/GradCAM-record_T1_DenseNet121_test-120_Ax.gif" width="200" height="200"> <br> [o] Correctly classified| <img src="/images/2023-its-miccai_faimi/GradCAM-auto_T1_DenseNet121_test-120_Ax.gif" width="200" height="200"> <br> [o] Correctly classified|
| AD |  <img src="/images/2023-its-miccai_faimi/GradCAM-auto_T1_DenseNet121_test-75_Ax.gif" width="200" height="200"> <br> [x] Misclassified| <img src="/images/2023-its-miccai_faimi/GradCAM-late_T1_DenseNet121_test-75_Ax.gif" width="200" height="200"> <br> [x] Misclassified| <img src="/images/2023-its-miccai_faimi/GradCAM-auto_T1_DenseNet121_test-75_Ax.gif" width="200" height="200">  <br> [x] Misclassified| -->


<table>
<thead>
  <tr>
    <td style="text-align: center;" > <b>Data Group</b></td>
    <td style="text-align: center;"><b>Subject-wise Split</b></td>
    <td style="text-align: center;"><b>Record-wise Split</b></td>
    <td style="text-align: center;"><b>Late Split</b></td>
  </tr>
</thead>
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



# Discussion
* <b>How You Split Matters</b>
  * The choice of data splitting strategy during cross-validation significantly influences the performance and robustness of deep learning models in longitudinal medical image analysis.
* <b>Data Leakage and Identity Confounding</b>
  * Improper data splitting can lead to data leakage, causing identity confounding within the models. This compromises their generalization and can result in misleadingly optimistic performance assessments.
* <b>Shortcut Learning Revealed by GradCAM</b>
  * Visualization using GradCAM highlights potential shortcut learning in models, particularly from record-wise and late-wise splitting strategies. This suggests that models may learn unintended patterns during cross-validation.
* <b>Validating Robustness with Subject-Wise Split</b>
  * This study validates previous findings suggesting a promising approach---subject-wise split demonstrates relative robustness and less vulnerability to data leakage compared to record-wise and late splitting strategies. However, challenges like underperformance indicate the need for further investigation, potentially with a larger and more diverse dataset.
* <b>Future Directions</b>
  * Promoting Subject-wise split: future research should strongly consider subject-wise split for more reliable model evaluation and development.
  * Investigating data variance and sensitive attributes: Further research should delve into the correlation between data splitting strategies and data variance, particularly exploring the influence of sensitive attributes such as age and sex. Understanding these relationships can lead to more nuanced and fair models.

## Limitations
  * Generalization Challenges:
    * Limited generalization to hold-out data likely influenced by data variance in sensitive attributes (e.g., age and gender imbalance).

  * Robustness of Subject-Wise Split:
    * Despite a significant drop in performance, subject-wise splitting demonstrates relative robustness. Addressing potential underfitting by incorporating a more diverse subject pool could enhance this approach's performance.
    Subject-wise splitting strategy shows more robustness but still suffers from performance drops, possibly due to underfitting, which can be mitigated with a larger and more diverse dataset.

# References
1. Chaibub Neto, E., Pratap, A., Perumal, T.M., Tummalacherla, M., Snyder, P., Bot, B.M., Trister, A.D., Friend, S.H., Mangravite, L., Omberg, L.: Detecting the impact of subject characteristics on machine learning-based diagnostic applications. npj Digital Medicine 2(1), 99 (Oct 2019). [https://doi.org/10.1038/s41746-019-0178-x](https://doi.org/10.1038/s41746-019-0178-x){:target="_blank"}
2. Yagis, E., Atnafu, S.W., García Seco de Herrera, A., Marzi, C., Scheda, R., Giannelli, M., Tessa, C., Citi, L., Diciotti, S.: Effect of data leakage in brain MRI classification using 2D convolutional neural networks. Scientific Reports 11(1), 22544 (Nov 2021). [https://doi.org/10.1038/s41598-021-01681-w](https://doi.org/10.1038/s41598-021-01681-w){:target="_blank"}


# Acknowledgement
Special thanks to Directorate General of Higher Education and Research Technology, Indonesia, Prof. I Ketut Eddy Purnama (Sepuluh Nopember Institute of Technology, Indonesia) and Prof. Tae-Seong Kim (Kyung Hee University, South Korea).