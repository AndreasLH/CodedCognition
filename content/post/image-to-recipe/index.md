---
title: Image to recipe retrieval
description: Advanced Deep learning in computer vision project
slug: hello-world
date: 2023-11-26
image: cover2.png
categories:
    - Multi-modal
tags:
    - CLIP
    - Contrastive learning
weight: 1       # You can add weight to some posts to override the default sorting (date descending)
math: true
---

# Motivation

I realised midways during this project that we had essentially just recreated the CLIP model.

# Data
![alt text](data.png)

## Contrastive learning

### Math

$$
    L_{bi} (a^{n=i}, b^{n=i}, b^{b\neq i}, a^{n\neq i}) = \frac{1}{B} \sum_{j=1}^B L^\prime_{bi}(i,j)\delta(i,j)
$$

![alt text](contrast.png) ![alt text](PCA.png)

# Model
![alt text](model.png)
# Results
We can go both forwards and backwards between images and text.

![Images and recipies](results.png)

## Out of distribution image

![alt text](OOD.png)
