---
layout: post
title: Hand Segmentation
subtitle: HandSeg&#58; An Automatically Labeled Dataset for Hand Segmentation from Depth Images
tags: [Hand Segmentation]
image: /img/hand-segmentation.png
paper: https://arxiv.org/pdf/1711.05944.pdf
---

We propose an automatic method for generating high-quality annotations for depth-based hand segmentation, and introduce a large-scale hand segmentation dataset. Existing datasets are typically limited to a single hand. By exploiting the visual cues given by an RGBD sensor and a pair of colored gloves, we automatically generate dense annotations for two hand segmentation. This lowers the cost/complexity of creating high quality datasets, and makes it easy to expand the dataset in the future. We further show that existing datasets, even with data augmentation, are not sufficient to train a hand segmentation algorithm that can distinguish two hands.

![result](/img/hand-segmentation-1.png)

## Material

[Dataset download](https://gfx.uvic.ca/pubs/2018/bojja2018handseg/page.md)


## Citation

```
@inproceedings{Bojja2019,
  title = {HandSeg: An Automatically Labeled Dataset for Hand Segmentation from Depth Images},
  author = {A.~K.~Bojja and F.~Mueller and S.~R.~Malireddi and M.~Oberweger and V.~Lepetit and C.~Theobalt and K.~M.~Yi and A.~Tagliasacchi},
  booktitle = {Proc.~of Conference on Computer and Robot Vision},
  year = {2019}
}
```
