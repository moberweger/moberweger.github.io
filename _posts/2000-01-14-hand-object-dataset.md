---
layout: post
title: Joint Hand-Object Pose Estimation
subtitle: HOnnotate - A method for 3D Annotation of Hand and Objects Poses
tags: [Joint Hand-Object Pose Estimation, Hand-Object Interaction, Dataset]
image: /img/hand-object-dataset.png
paper: https://arxiv.org/pdf/1907.01481.pdf
---

We propose a method for annotating images of a hand manipulating an object with the 3D poses of both the hand and the object, together with a dataset created using this method. There is a current lack of annotated real images for this problem, as estimating the 3D poses is challenging, mostly because of the mutual occlusions between the hand and the object. To tackle this challenge, we capture sequences with one or several RGB-D cameras, and jointly optimizes the 3D hand and object poses over all the frames simultaneously. This method allows us to automatically annotate each frame with accurate estimates of the poses, despite large mutual occlusions. With this method, we created HO-3D, the first markerless dataset of color images with 3D annotations of both hand and  object. This dataset is currently made of 80,000 frames, 65 sequences, 10 persons, and 10 objects, and growing, and we will make it publicly available upon publication. We also use it to train a Deep Network to perform RGB-based single frame hand pose estimation and provide a baseline on our dataset.

{% include googleDrivePlayer.html id="1CDsIcq87EdQ_U4yE7xMPZzKaXa0AFdvn" %}

## Dataset

HO-3D is a dataset with 3D pose annotations for hand and object under severe occlusions from each other. The 68 sequences in the dataset contain 10 different persons manipulating 10 different objects, which are taken from YCB objects dataset. The dataset currently contains annotations for 77,558 images which are split into 66,034 training images (from 55 sequences) and 11,524 evaluation images (from 13 sequences). The evaluation sequences are carefully selected to address the following scenarios:

- Seen object and seen hand: Sequences SM1, SB11 and SB13 contain hands and objects which are also used in the training set.
- Unseen object and seen hand: Sequences AP10, AP11, AP12, AP13 and AP14 contain 019_pitcher_base object which is not used in the training set.
- Seen object and unseen hand: Sequences MPM10, MPM11, MPM12, MPM13 and MPM14
    contain a subject with different hand shape and color andis not part of the training set. 

| ![result](/img/hand-object-dataset-1.png) | ![result](/img/hand-object-dataset-2.png) | ![result](/img/hand-object-dataset-3.png) |
| ![result](/img/hand-object-dataset-4.png) | ![result](/img/hand-object-dataset-5.png) | ![result](/img/hand-object-dataset-6.png) |
| ![result](/img/hand-object-dataset-7.png) | ![result](/img/hand-object-dataset-8.png) | ![result](/img/hand-object-dataset-9.png) |

## Method

For establishing a baseline on our proposed dataset for single RGB image based hand pose  estimation, we use a CNN architecture based on a Convolutional Pose Machine to  predict the 2D  hand joint locations. In addition, we also predict the root relative hand joint directions, by adding an additional stage at the  end of the CPM and replacing the last layer with a fully connected layer. More details on the architecture is provided in the supplementary material. The 3D joint locations and shape parameters of the hand are then obtained by fitting the MANO model to these predictions. 

Qualitative results for single RGB frame based hand pose estimation method are shown below. We recover hand poses when it is heavily occluded by objects and in cluttered scenes. For the hand, we plot the skeleton with 3D joint positions projected to the image, together with the 3D model rendered from a different viewpoint.

| ![result](/img/hand-object-dataset-10.png) | ![result](/img/hand-object-dataset-11.png) | ![result](/img/hand-object-dataset-12.png) |
| ![result](/img/hand-object-dataset-13.png) | ![result](/img/hand-object-dataset-14.png) | ![result](/img/hand-object-dataset-15.png) |

## Material

[Dataset download](https://files.icg.tugraz.at/d/76661ed06445490ab21c/)

[Github](https://github.com/shreyashampali/ho3d)

## Citation

```
@inproceedings{Hampali2020,
  title = {HOnnotate - A method for 3D Annotation of Hand and Objects Poses},
  author = {S.~Hampali and M.~Rad and M.~Oberweger and V.~Lepetit},
  booktitle = {Proc.~of Computer Vision and Pattern Recognition},
  year = {2020},
}
```
