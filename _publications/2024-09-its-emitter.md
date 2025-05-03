---
title: "Lite FBCN: Lightweight Fast Bilinear Convolutional Network for Brain Disease Classification from MRI Image"
author_profile: true
collection: publications
permalink: /publications/lite-fbcn
date: 2024-09-03
venue: 'EMITTER International Journal of Engineering Technology'
category: manuscripts

---
Dewinda Julianensi Rumala, Reza Fuad Rachmadi, Anggraini Dwi Sensusiati, and I Ketut Eddy Purnama
<br>
<a href="https://arxiv.org/abs/2409.10952v1"  target="_blank"><i class="fas fa-file-pdf">Preprint</i></a>
<a href="https://github.com/djrumala/lite-fbcn"  target="_blank"><i class="fab fa-github">Code</i></a>
<!-- Link to the publication/paper1 page -->
<br>


Achieving high accuracy with computational efficiency in brain disease classification from Magnetic Resonance Imaging (MRI) scans is challenging, particularly when both coarse and fine-grained distinctions are crucial. Current deep learning methods often struggle to balance accuracy with computational demands. We propose Lite-FBCN, a novel Lightweight Fast Bilinear Convolutional Network designed to address this issue. Unlike traditional dual-network bilinear models, Lite-FBCN utilizes a single-network architecture, significantly reducing computational load. Lite-FBCN leverages lightweight, pre-trained CNNs fine-tuned to extract relevant features and incorporates a channel reducer layer before bilinear pooling, minimizing feature map dimensionality and resulting in a compact bilinear vector. Extensive evaluations on cross-validation and hold-out data demonstrate that Lite-FBCN not only surpasses baseline CNNs but also outperforms existing bilinear models. Lite-FBCN with MobileNetV1 attains 98.10% accuracy in cross-validation and 69.37% on hold-out data (a 3% improvement over the baseline). UMAP visualizations further confirm its effectiveness in distinguishing closely related brain disease classes. Moreover, its optimal trade-off between performance and computational efficiency positions Lite-FBCN as a promising solution for enhancing diagnostic capabilities in resource-constrained and or real-time clinical environments.


Or you can directly download the preprint: <a href="/files/pub/2024-its-emitter/preprint.pdf" target="_blank">here</a>