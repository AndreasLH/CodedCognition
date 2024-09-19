---
title: Explainable AI using Saliency maps and Proto-PNet
description: class activation mappings and prototype-based networks for explanations in CNN classifications
date: 2023-04-05 
image: image.png
categories:
    - Responsible AI
tags:
    - CNN
    - 
---


Class Activation mappings (CAM) based on the output of a simple ResNet18 model
![Class activation mappings](image.png)

Prototype based network. Works on a this-looks-like-that principle, i.e. it looks in other images with similar features to explain why it classifies image to certain classes.
![Proto-PNet model architecture](protop.png)

![Explanations from the Proto-PNet model](ProtoP_bboxes.png)