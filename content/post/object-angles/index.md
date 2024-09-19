---
title: Object recognition at different angles
description: My very first encounter with deep learning
date: 2019-09-17 
image: angle experiment.png
categories:
    - Deep learning
tags:
    - Resnet
    - Statistics
---

This was the very first time I played around with an image classifier, just a week after starting my Bachelor's degree in Artificial intelligence and Data. Back then I had no idea how the model actually worked, but accepted is as a black box.

Basically the experiment was to use an out-of-the box Resnet50 model to recognise a phone at different angles. Another purpose of the experiment was to get familiar with means and confidence intervals.

This was gathered in a table

| Angle (deg.) |   |   |   |   |   |   | Avg. (%) |
|-------------:|:-:|:-:|:-:|:-:|:-:|:-:|---------:|
|           90 |  y |y   | y  |y   |  y |   y|      100 |
|           80 | y  | y  |  y |   y|  y | y  |      100 |
|           70 | y  | y  |  y |   y|  y | y |      100 |
|           60 |  y  | y  |  y |   y|  y | y |    100   |
|           50 |  y  | y  |  y |   y|  y | y  |       100   |
|           40 |  y  | y  |  y |   y|  y | y |       100   |
|           30 |  y  | y  |  y |   y|  y | y |       100   |
|           20 |  y  | y  |  y |   y|  y | y |       100   |
|           10 | n  | n  |  n |  y | y  | n  |       33.33   |
|            0 | n  | y  | n  | n  |  n |  n |       16.7   |

We collected these results and found an average accuracy of 85% with a confidence interval [80.6%; 89.4%].

All this was as simple as the following code and some boilerplate to load the image

```python
model = resnet50.ResNet50(weights='imagenet')
# load the image
# ....
processed_image = resnet50.preprocess_input(np.expand_dims(frame, axis=0))
predictions = model.predict(processed_image)
label = resnet50.decode_predictions(predictions)    
```