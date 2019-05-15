---
layout: post
title: Transfer Learning for 3D Pose Estimation
subtitle: Feature Mapping for Learning Fast and Accurate 3D Pose Inference from Synthetic Images
tags: [Transfer Learning, Hand Pose Estimation, Object Pose Estimation]
image: /img/feature-mapping.png
paper: https://arxiv.org/pdf/1712.03904.pdf
---

We propose a simple and efficient method for exploiting synthetic images when training a Deep Network to predict a 3D pose from an image. The ability of using synthetic images for training a Deep Network is extremely valuable as it is easy to create a virtually infinite training set made of such images, while capturing and annotating real images can be very cumbersome. However, synthetic images do not resemble real images exactly, and using them for training can result in suboptimal performance. It was recently shown that for exemplar-based approaches, it is possible to learn a mapping from the exemplar representations of real images to the exemplar representations of synthetic images. In this paper, we show that this approach is more general, and that a network can also be applied after the mapping to infer a 3D pose: At run-time, given a real image of the target object, we first compute the features for the image, map them to the feature space of synthetic images, and finally use the resulting features as input to another network which predicts the 3D pose. Since this network can be trained very effectively by using synthetic images, it performs very well in practice, and inference is faster and more accurate than with an exemplar-based approach. We demonstrate our approach on the LINEMOD dataset for 3D object pose estimation from color images. We show that it allows us to outperform the state-of-the-art on the LINEMOD dataset.


## Results

with Feature Mapping: | ![result](/img/feature-mapping-2.png) | ![result](/img/feature-mapping-3.png) |
w/o Feature Mapping: | ![result](/img/feature-mapping-1.png) | ![result](/img/feature-mapping-4.png) |

{% include googleDrivePlayer.html id="1TpTYcYs63uwVw8BU2OOsztdmiwgcLBXt" %}

We also demonstrate our feature mapping on the NYU dataset for 3D hand pose estimation from depth maps. By using our approach, we achieve an error of 7.4mm, which improves the state-of-the-art by 4.9mm or almost 40%.

{% include googleDrivePlayer.html id="1PLM-XPgDrWJgmGtTiyv3tGDVB3FStxZB" %}
 
## Material

Our results: Each line is the estimated hand pose of a frame. The pose is parametrized by the locations of the joints in (u, v, d) coordinates, ie image coordinates and depth. The coordinates of each joint are stored in sequential order.

- [NYU](http://cims.nyu.edu/%7Etompson/NYU_Hand_Pose_Dataset.htm) dataset of J. Tompson: [FeatureMapping_DeepPrior++](https://drive.google.com/open?id=1EPPXpnrVp4V_Kq2Zck1uhV_SuAmIWZPN)


## Citation

```
@InProceedings{Rad2018,
  title = {Feature Mapping for Learning Fast and Accurate 3D Pose Inference from Synthetic Images},
  author = {M.~Rad and M.~Oberweger and V.~Lepetit},
  booktitle = {Proc.~of Computer Vision and Pattern Recognition},
  year = {2018}
}
```
