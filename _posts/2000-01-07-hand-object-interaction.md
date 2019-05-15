---
layout: post
title: Hand-Object Interaction
subtitle: Efficient Physics-Based Implementation for Realistic Hand-Object Interaction in Virtual Reality
tags: [Hand-Object Interaction, AR, VR]
image: /img/hand-object.png
paper: https://drive.google.com/open?id=1WwSRqDG80-dFXiLxHci_q9NFV2W-lFUA
---

We propose an efficient physics-based method for dexterous 'real hand'-'virtual object' interaction in Virtual Reality environments. Our method is based on the Coulomb friction model, and we show how to efficiently implement it in a commodity VR engine for real-time performance. This model enables very convincing simulations of many types of actions such as pushing, pulling, grasping, or even dexterous manipulations such as spinning objects between fingers without restrictions on the objects’ shapes or hand poses. Because it is an analytic model, we do not require any prerecorded data, in contrast to previous methods. For the evaluation of our method, we conduction a pilot study that shows that our method is perceived more realistic and natural, and allows for more diverse interactions. Further, we evaluate the computational complexity of our method to show real-time performance in VR environments.

## Results

Demonstration of our physics-based hand interaction method for VR environments. Our approach allows countless complex interactions such as handling a box in one hand and opening it with the other (top-left), or smashing a wall with an axe held in one hand (top-right). We can even spin an object between two fingers from two different hands (bottom-left) or from the same hand (bottom-right) in a very realistic manner. The red arrows indicate the forces calculated with our method and applied to the objects. Yellow arrows depict the global hand motion depicted for demonstration purposes only.

![result](/img/hand-object-1.png)

{% include googleDrivePlayer.html id="1fXpXTCnxccrcB4rpq2CwDGYmHQoSEjK4" %}

## Citation

```
@InProceedings{Hoell2018,
  title = {Efficient Physics-Based Implementation for Realistic Hand-Object Interaction in Virtual Reality},
  author = {M.~H\"oll and M.~Oberweger and C.~Arth and V.~Lepetit},
  booktitle = {Proc.~of Conference on Virtual Reality and 3D User Interfaces},
  year = {2018}
}
```
