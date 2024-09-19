---
title: Efficient use of computation
description: Optimising code for fast operation on CPUs and GPUs
date: 2024-01-15 
image: cpu.png
categories:
    - HPC
tags:
    - HPC
---

## CPU
Efficient computation and hardware utilisation underpins most of the methods used in deep learning learning applications.

{{< figure src="cpu.png" title="Different implementations of matrix multiplication on cpu" width=60% >}}

{{< figure src="mkn.png" title="Why it is faster to access in the mkn pattern" width=60% >}}

### Making things faster: multithreading

For this, we are chaning the problem to model the heat spread in a room

{{< figure src="room.png" title="Room shown at different times" width=60% >}}

Now we can utilise all the cores in the machine to make the simulation go a lot faster.

{{< figure src="jacobi.png" title="Performance when using multiple cores, measured in Mega lattice updates/s" width=60% >}}


## Making things even faster: using a gpu

The idea of using blocking is to allow each thread to work on more than one element of the C matrix before being released. This might improve performance, because the overhead of assigning new threads to calculate each element is higher than assigning new work to each thread.

{{< figure src="gpu.png" title="Different implementations of matrix multiplication on cpu" width=60% >}}