---
layout: post
title: Deep Prior for Hand Pose Estimation
subtitle: Hands Deep in Deep Learning for Hand Pose Estimation
tags: [Hand Pose Estimation]
image: /img/deep-prior.png
paper: https://arxiv.org/pdf/1502.06807.pdf
code: https://github.com/moberweger/deep-prior/
---

We introduce and evaluate several architectures for Convolutional Neural Networks to predict the 3D joint  locations of a hand given a depth map. We first show that a prior on the 3D pose can be easily introduced and significantly improves the accuracy and reliability of the predictions. We also show how to use context efficiently to deal with ambiguities between fingers. These two contributions allow us to significantly  outperform the state-of-the-art on several challenging benchmarks, both in terms of accuracy and computation times.

## Details

We introduce a prior model for predicting the 3D joint locations of a hand given a depth map using Convolutional Neural Networks (CNN). In particular, we show that 1) a prior model improves the accuracy by constraining the predicted hand pose to possible ones; 2) our non-linear, compressed model can be learnt in a data-driven manner and explicitly benefits from a holistic hand pose representation; 3) our prior model seamlessly integrates into a standard CNN architecture creating an unusual "bottleneck". We show that our contributions allow us to significantly outperform the state-of-the-art on several challenging benchmarks, both in terms of accuracy and computation times.

This [ICCV'15 paper (Depth-based hand pose estimation: data, methods, and challenges)](http://www.cv-foundation.org/openaccess/content_iccv_2015/papers/Supancic_Depth-Based_Hand_Pose_ICCV_2015_paper.pdf) independently shows that our approach outperforms the other ones :)

## Results

{% include googleDrivePlayer.html id="1eqM4n_og4clzq0OcSBRlKJY_oPUEUCpB" %}

## Material

Presentation: [CVWW'15 presentation](https://drive.google.com/open?id=1cVcqpY5ehtOiucpzSwmQqLNLCOTwpCvh)

Our results: Each line is the estimated hand pose of a frame. The pose is parametrized by the locations of the joints in (u, v, d) coordinates, ie image coordinates and depth. The coordinates of each joint are stored in sequential order.

- [ICVL](http://www.iis.ee.ic.ac.uk/%7Edtang/hand.html) dataset of D. Tang: [CVWW'15 Prior](https://drive.google.com/open?id=1wylJO3n95VsxcIdod_aaEOjRJ5ZdNZ7H), [CVWW'15 Refinement](https://drive.google.com/open?id=1o8gFubG4CFi8A4HVnfjawt2chXTmUo8t)
- [NYU](http://cims.nyu.edu/%7Etompson/NYU_Hand_Pose_Dataset.htm) dataset of J. Tompson: [CVWW'15 Prior](https://drive.google.com/open?id=1_77tO0lDVaIJh4L_VGisVEL8i8I7XIbM), [CVWW'15 Refinement](https://drive.google.com/open?id=1CmNkc6KQrTrsK9gKCrZht_sW15yifiMY) 

## Code

Here you can find the code for our CVWW'15 paper "Hands Deep in Deep Learning for Hand Pose Estimation". It is distributed as a single package [DeepPrior](https://github.com/moberweger/deep-prior) under GPLv3. It also includes two pretrained models for the NYU and ICVL dataset.
There is no proper documentation yet, but a basic readme file is included. If you have questions please do not hesitate to contact us.
If you use the code, please cite us (see below). 

## Citation

```
@inproceedings{Oberweger2015,
  author = {M.~Oberweger and P.~Wohlhart and V.~Lepetit},
  title = {Hands Deep in Deep Learning for Hand Pose Estimation},
  booktitle = {Proc.~of Computer Vision Winter Workshop},
  year = 2015
}
```
