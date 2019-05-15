---
layout: post
title: Training Data for Hand Pose Estimation
subtitle: Efficiently Creating 3D Training Data for Fine Hand Pose Estimation
tags: [Training Data, Hand Pose Estimation]
image: /img/training-data.png
paper: https://arxiv.org/pdf/1605.03389.pdf
code: https://github.com/moberweger/semi-auto-anno/
---

While many recent hand pose estimation methods critically rely on a training set of labelled frames, the  creation of such a dataset is a challenging task that has been overlooked so far. As a result, existing  datasets are limited to a few sequences and individuals, with limited accuracy, and this prevents these methods from delivering their full potential. We propose a semi-automated method for efficiently and  accurately labeling each frame of a hand depth video with the corresponding 3D locations of the joints:   The user is asked to provide only an estimate of the 2D reprojections of the visible joints in some reference frames, which are automatically selected to minimize the labeling work by efficiently optimizing a sub-modular loss function. We then exploit spatial, temporal, and appearance constraints to retrieve the  full 3D poses of the hand over the complete sequence. We show that this data can be used to train a recent  state-of-the-art hand pose estimation method, leading to increased accuracy.

## Material

Presentation: [CVPR'16 poster](https://drive.google.com/open?id=1nCfDaGF66Gs1iPbJ6mXUkD58tEC0qAPC)

## Datasets

- [Synthetic dataset](https://drive.google.com/open?id=1XptUmjS8yELHmEw77S_ph3uQCwlhFD8x) with ground truth 3D joint locations used for the evaluation of our method.
- [Egocentric 3D hand pose dataset](https://drive.google.com/open?id=1taV30_IbUWcMJsz2kGWKCuGCPAByE0az) created with our method (used in our CVPR paper).

![result](/img/training-data-1.png)

## Multi-User Egocentric Datasets

Using our annotation tool, we created a large dataset with 3D hand pose annotations. This dataset targets hand pose estimation from an egocentric viewpoint. The dataset was captured by mounting an RGBD camera on a tripod at head height facing away from the subject. The subject is standing behind the camera, simulating a camera viewpoint equivalent to mounting the camera on an HMD.

The subjects were asked to perform common hand articulations, as well as typical articulations for AR/VR interaction. For each subject we recorded 19 sequences, 18 of which contain the same hand articulation performed by each subject, and 1 sequence with individual articulation.

We collected data from 4 subjects (1 male, 3 female) and approximately 63k RGBD frames (each around 15k). Data and annotations can be downloaded below. More annotations will be released soon :)


| Subject 1: | [RGB+Depth Data 6.6GB](https://files.icg.tugraz.at/f/184092f8f4/?raw=1) | [Hand 3D detections 96KB](https://files.icg.tugraz.at/f/c78eb46dba/?raw=1)|
| Subject 2: | [RGB+Depth Data 7.9GB](https://files.icg.tugraz.at/f/81a09b46aa/?raw=1) | [Hand 3D detections 96KB](https://files.icg.tugraz.at/f/d1f03521b6/?raw=1) |
| Subject 3: | [RGB+Depth Data 7.2GB](https://files.icg.tugraz.at/f/6cfcd2d248/?raw=1) | [Hand 3D detections 92KB](https://files.icg.tugraz.at/f/caa775687e/?raw=1) |
| Subject 4: | [RGB+Depth Data 8.0GB](https://files.icg.tugraz.at/f/722fc7f5b1/?raw=1) | [Hand 3D detections 120KB](https://files.icg.tugraz.at/f/65ca6c5850/?raw=1) |


## Code

Here you can find the code for our CVPR'16 paper "Efficiently Creating 3D Training Data for Fine Hand Pose Estimation". It is distributed as a single package [SemiAutoAnno](https://github.com/moberweger/semi-auto-anno) under GPLv3. The code can be run out-of-the-box with our [synthetic dataset](https://drive.google.com/open?id=1XptUmjS8yELHmEw77S_ph3uQCwlhFD8x).
There is no proper documentation yet, but a basic readme file and a short manual on how to use the GUI are included. If you have questions please do not hesitate to contact us.
If you use the code, please cite us (see below). 


## Citation

```
@inproceedings{Oberweger2016,
  author = {M.~Oberweger and G.~Riegler and P.~Wohlhart and V.~Lepetit},
  title = {Efficiently Creating 3D Training Data for Fine Hand Pose Estimation},
  booktitle = {Proc.~of Computer Vision and Pattern Recognition},
  year = 2016
}
```
