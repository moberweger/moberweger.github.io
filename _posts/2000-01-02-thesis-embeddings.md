---
layout: post
title: Master's Thesis
subtitle: Embeddings for Random Ferns Classification
tags: [Random Ferns, Random Forest, Embedding]
image: /img/embeddings.png
paper: http://diglib.tugraz.at/download.php?id=576a79934ccb2&location=aleph
---

Efficient multi-class machine learning methods are a key component in many computer vision applications. In this area the Random Forest classifier is considered state-of-the-art as it provides an efficient way to learn an inherently multi-class classifier, that naturally handles high dimensional, multi-modal data. Recent research focused on optimizing this classifier for different applications, by learning appropriate node split criteria. In this work we present a different scheme for acquiring these node splits. By selecting feature subsets and using an ensemble of weak classifiers, we propose different linear subspace and ordinal embeddings to derive flat classifiers for leaf assignment, similar to the popular Random Ferns classifier. Therefore we use a generic framework into which we integrate all of our proposed embeddings.  
We evaluate our classifiers on several machine learning benchmark datasets, as well as on well-known computer vision datasets. We show, that our classifiers can outperform conventional Random Ferns and even Random Forest without significantly increasing computational costs. Further, we show the applicability of our classifier for the task of planar object tracking, as well as 3D interest point recognition.


## Citation

```
@mastersthesis{Oberweger2014a,
  title = {Embeddings for Random Ferns Classification},
  school = {Graz University of Technology},
  author = {M.~Oberweger},
  year = {2014}
}
```
