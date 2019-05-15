---
layout: post
title: PhD Thesis
subtitle: 3D Hand Pose Estimation from Images for Interactive Applications
tags: [Hand Pose Estimation, Hand-Object Interaction, Object Pose Estimation, Joint Hand-Object Pose Estimation]
image: /img/hand-pose.png
paper: http://diglib.tugraz.at/download.php?id=5c4a489d042d4&location=aleph
---

Hands are the most important body part for humans to interact with and manipulate their environment. Hence, 3D hand pose estimation is an important cornerstone of many Human-Computer Interaction (HCI), Virtual Reality (VR), and Augmented Reality (AR) applications, such as robotic control or virtual object interaction. Despite the plentiful applications and importance for the industry, hand pose estimation is still an unsolved problem. It requires dealing with many challenges, including many Degrees of Freedom (DoF) and occlusions.  
In this thesis we focus on markerless Computer Vision-based 3D hand pose estimation as well as joint hand-object pose estimation in case a hand is interacting with an object. The input to our methods are single view depth or color images and the outputs are the 3D poses of the hand and/or the object, respectively.
First, we contribute to the class of discriminative methods for 3D hand pose estimation. Our proposed methods are based on Convolutional Neural Networks (CNNs), and we show how to efficiently integrate a prior on the 3D pose into such a network. The prior significantly increases the accuracy of the predicted 3D hand pose and restricts the predicted pose to the manifold of feasible hand poses. Despite the high accuracy, the pose estimator can still make mistakes and thus we propose a second approach that learns to fix the mistakes made by an initial estimator. This approach relies on the analysis-by-synthesis paradigm to fix these mistakes.  
However, these supervised methods require a large amount of accurate training data, which can be cumbersome to acquire. Therefore, we propose an efficient method to generate 3D training data for articulated objects. Our semi-automatic method takes image sequences with sparse 2D annotations as input and outputs 3D annotations for every frame. We also investigate how additional data sources can be leveraged. We present an approach that additionally uses synthetically rendered depth images of the hand, which are easy to generate in practice, and using this additional data source significantly boosts the accuracy of the predictions. We further investigate 3D hand pose estimation from color images. Therefore, we propose a method that transfers the supervision of pairs of unlabeled depth and color images to labeled synthetic depth images. We show that our method—trained without color labels—can achieve similar results to methods trained on labeled color images.  
Practical applications in AR and VR often involve hand-held objects that are manipulated by the hand. These applications require the pose of the hand together with the pose of the object, and thus we introduce an approach that jointly estimates the hand and the object pose. Our method is, to the best of our knowledge, the first single-frame method for joint hand-object pose estimation, and has a comparable accuracy to state-of-the-art tracking-based approaches. When the hand interacts with an object, handling the different occlusions quickly becomes intractable and methods that do not need any prior knowledge of the occluders are required. For such scenarios, we introduce a method for 3D object pose estimation that is inherently robust to occlusions and does not require knowledge of the occluders in advance, while providing high accuracy 3D pose estimates of highly occluded objects.  
Finally, we conclude with a discussion of the proposed methods and possible extensions with directions of future work.


## Citation

```
@phdthesis{Oberweger2018b,
  title = {3D Hand Pose Estimation from Images for Interactive Applications},
  school = {Graz University of Technology},
  author = {M.~Oberweger},
  year = {2018}
}
```
