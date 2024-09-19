---
title: Heart rhythm estimation in face videos
description: Bachelor's Thesis
date: 2022-06-06
image: bvp2.png
categories:
    - Thesis
Tags:
    - Signal processing
---



{{< figure src="bpm.png" title="Processing the data from the BVP sensor" width=90% >}}

Use the excellent [MediaPipe framework](https://chuoling.github.io/mediapipe/solutions/face_mesh.html) to find faces in videos. The video below shows how excellent this library is at finding the face.

![Real time face processing with the Mediapipe frame work](face_mesh_android_gpu.gif)

{{< figure src="face crop.png" title="Extraction of the skin of the face, and finding the relevant keypoints." width=90% >}}
