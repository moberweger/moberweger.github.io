---
layout: post
title: Domain Transfer for 3D Pose Estimation
subtitle: Domain Transfer for 3D Pose Estimation from Color Images without Manual Annotations
tags: [Transfer Learning, Hand Pose Estimation, Object Pose Estimation]
image: /img/domain-transfer.png
paper: https://arxiv.org/pdf/1810.03707.pdf
---

We introduce a novel learning method for 3D pose estimation from color images. While acquiring annotations for color images is a difficult task, our approach circumvents this problem by learning a mapping from paired color and depth images captured with an RGB-D camera. We jointly learn the pose from synthetic depth images that are easy to generate, and learn to align these synthetic depth images with the real depth images. We show our approach for the task of 3D hand pose estimation and 3D object pose estimation, both from color images only. Our method achieves performances comparable to state-of-the-art methods on popular benchmark datasets, without requiring any annotations for the color images.

## Results

Our method allows very accurate 3D pose estimation from color images without annotated color images. In case of 3D rigid object pose estimation we draw the bounding boxes, where blue is the ground truth bounding box and red the bounding box of our predicted pose. For 3D hand pose estimation, we show the 3D joint locations projected to the color image, blue denoting the ground truth and green our estimation.

| ![result](/img/domain-transfer-1.png) | ![result](/img/domain-transfer-2.png) | ![result](/img/domain-transfer-3.png) | 
| ![result](/img/domain-transfer-4.png) | ![result](/img/domain-transfer-5.png) | ![result](/img/domain-transfer-6.png) |

{% include googleDrivePlayer.html id="13C_PRswf0jgitsXySNg4yXSnUFbTKT65" %}

## Citation

```
@InProceedings{Rad2018c,
  title = {Domain Transfer for 3D Pose Estimation from Color Images without Manual Annotations},
  author = {M.~Rad and M.~Oberweger and V.~Lepetit},
  booktitle = {Proc.~of Asian Conference on Computer Vision},
  year = {2018}
}
```
