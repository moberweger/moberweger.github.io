---
layout: post
title: Deep Heatmaps for 3D Object Pose Estimation
subtitle: Making Deep Heatmaps Robust to Partial Occlusions for 3D Object Pose Estimation
tags: [Heatmaps, Object Pose Estimation]
image: /img/deep-heatmaps.png
paper: https://arxiv.org/pdf/1804.03959.pdf
---

We introduce a novel method for robust and accurate 3D object pose estimation from a single color image under large occlusions. Following recent approaches, we first predict the 2D projections of 3D points related to the target object and then compute the 3D pose from these correspondences using a geometric method. Unfortunately, as the results of our experiments show, predicting these 2D projections using a regular CNN or a Convolutional Pose Machine is highly sensitive to partial occlusions, even when these methods are trained with partially occluded examples. Our solution is to predict heatmaps from multiple small patches independently and to accumulate the results to obtain accurate and robust predictions. Training subsequently becomes challenging because patches with similar appearances but different positions on the object correspond to different heatmaps. However, we provide a simple yet effective solution to deal with such ambiguities. We show that our approach outperforms existing methods on two challenging datasets: The Occluded LineMOD dataset and the YCB-Video dataset, both exhibiting cluttered scenes with highly occluded objects.

## Results

Our method can predict the 3D pose of objects even under heavy occlusions from color images. Samples are objects from the Occluded LineMOD dataset. The green bounding boxes correspond to the ground truth poses, the blue bounding boxes to our estimated poses.

| **Cat** | **Duck** | **Can** |
| ![result](/img/deep-heatmaps-cat.gif) | ![result](/img/deep-heatmaps-duck.gif) | ![result](/img/deep-heatmaps-can.gif) |
| **Holepuncher** | **Driller** | **Glue** |
| ![result](/img/deep-heatmaps-holepuncher.gif) | ![result](/img/deep-heatmaps-driller.gif) | ![result](/img/deep-heatmaps-glue.gif) |

{% include googleDrivePlayer.html id="19FbCliDMOIeXosmaRAh4ZVf27HKk9O17" %}

## Material

Results: The 3D pose is represented as pose matrix [R &#124; t] and stored in a plain text file. Each file corresponds to one frame where the file name corresponds to the frame name. Frames where the object is not present are not exported. Note, that there are slight differences compared to the results in the paper, since PnP with RANSAC introduces randomness in the evaluation.

- [YCB-Video](https://rse-lab.cs.washington.edu/projects/posecnn/) dataset of Y. Xiang: [ECCV'18 DeepHeatmaps](https://drive.google.com/open?id=1jGg02zpqFKc8X7PmjKIbe5ZJzvTS9j5u)


## Citation

```
@InProceedings{Oberweger2018,
  title = {Making Deep Heatmaps Robust to Partial Occlusions for 3D Object Pose Estimation},
  author = {M.~Oberweger and M.~Rad and V.~Lepetit},
  booktitle = {Proc.~of European Conference on Computer Vision},
  year = {2018}
}
```
