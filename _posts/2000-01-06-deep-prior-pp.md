---
layout: post
title: Deep Prior++ for Hand Pose Estimation
subtitle: DeepPrior++&#58; Improving Fast and Accurate 3D Hand Pose Estimation
tags: [Hand Pose Estimation]
image: /img/deep-prior-pp.png
paper: https://arxiv.org/pdf/1708.08325.pdf
code: https://github.com/moberweger/deep-prior-pp/
---

[DeepPrior]({% post_url 2000-01-03-deep-prior %}) is a simple approach based on Deep Learning that predicts the joint 3D locations of a hand given a depth map. Since its publication early 2015, it has been outperformed by several impressive works.  Here we show that with simple improvements: adding ResNet layers, data augmentation, and better initial hand localization, we achieve better or similar performance than more sophisticated recent methods on the three main benchmarks (NYU, ICVL, MSRA) while keeping the simplicity of the original method.

## Results

{% include googleDrivePlayer.html id="1zQ2kmthI_LldJWnhtRgNEYQSysSBUjdP" %}

## Material

Poster: [ICCVW'17 poster](https://drive.google.com/open?id=1XMn-rOs0sKDv-DONzqPACA01lW0UdQLI)

Our results: Each line is the estimated hand pose of a frame. The pose is parametrized by the locations of the joints in (u, v, d) coordinates, ie image coordinates and depth. The coordinates of each joint are stored in sequential order.

- [ICVL](http://www.iis.ee.ic.ac.uk/%7Edtang/hand.html) dataset of D. Tang: [ICCVW'17 DeepPrior++](https://drive.google.com/open?id=1S8w7wbOatUxNh1q7AshQSjKkP4JzzvjL)
- [NYU](http://cims.nyu.edu/%7Etompson/NYU_Hand_Pose_Dataset.htm) dataset of J. Tompson: [ICCVW'17 DeepPrior++](https://drive.google.com/open?id=1YlPMvObGz9so9nRLNBElM8Zm9i1uf5Iy)
- MSRA dataset of X. Sun: [ICCVW'17 DeepPrior++](https://drive.google.com/open?id=1CUdbAoVsrkKaga6g9PxDFZqMMaBd4ijD)

## Code

Here you can find the code for our ICCVW'17 paper "DeepPrior++: Improving Fast and Accurate 3D Hand Pose Estimation". It is distributed as a single package [DeepPrior++](https://github.com/moberweger/deep-prior-pp) under GPLv3. It also includes pretrained models for the NYU, MSRA and ICVL dataset.
There is no proper documentation yet, but a basic readme file is included. If you have questions please do not hesitate to contact us.
If you use the code, please cite us (see below). 


## Citation

```
@InProceedings{Oberweger2017,
  title = {DeepPrior++: Improving Fast and Accurate 3D Hand Pose Estimation},
  author = {M.~Oberweger and V.~Lepetit},
  booktitle = {Proc.~of International Conference on Computer Vision Workshops},
  Year = {2017}
}
```
