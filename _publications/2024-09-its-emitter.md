---
title: "Lite FBCN: Lightweight Fast Bilinear Convolutional Network for Brain Disease Classification from MRI Image"
author_profile: false
collection: publications
permalink: /publications/lite-fbcn
# excerpt: 'This paper is about the number 2. The number 3 is left for future work.'
date: 2024-09-03
venue: 'EMITTER International Journal of Engineering Technology'
# citation: 'Rumala, D.J., van Ooijen, P., Rachmadi, R.F. et al. Deep-Stacked Convolutional Neural Networks for Brain Abnormality Classification Based on MRI Images. J Digit Imaging 36, 1460–1479 (2023). https://doi.org/10.1007/s10278-023-00828-7'
---
Dewinda Julianensi Rumala, Reza Fuad Rachmadi, Anggraini Dwi Sensusiati, and I Ketut Eddy Purnama
<br>
<a href=""  target="_blank"><i class="fas fa-file-pdf"> Preprint</i></a>
<a href="https://github.com/djrumala/lite-fbcn"  target="_blank"><i class="fab fa-github"> Code</i></a>
<!-- Link to the publication/paper1 page -->
<br>
<body>

Achieving high accuracy with computational efficiency in brain disease classification from Magnetic Resonance Imaging (MRI) scans is challenging, particularly when both coarse and fine-grained distinctions are crucial. Current deep learning methods often struggle to balance accuracy with computational demands. We propose Lite-FBCN, a novel Lightweight Fast Bilinear Convolutional Network designed to address this issue. Unlike traditional dual-network bilinear models, Lite-FBCN utilizes a single-network architecture, significantly reducing computational load. Lite-FBCN leverages lightweight, pre-trained CNNs fine-tuned to extract relevant features and incorporates a channel reducer layer before bilinear pooling, minimizing feature map dimensionality and resulting in a compact bilinear vector. Extensive evaluations on cross-validation and hold-out data demonstrate that Lite-FBCN not only surpasses baseline CNNs but also outperforms existing bilinear models. Lite-FBCN with MobileNetV1 attains 98.10% accuracy in cross-validation and 69.37% on hold-out data (a 3% improvement over the baseline). UMAP visualizations further confirm its effectiveness in distinguishing closely related brain disease classes. Moreover, its optimal trade-off between performance and computational efficiency positions Lite-FBCN as a promising solution for enhancing diagnostic capabilities in resource-constrained and or real-time clinical environments.


</body>