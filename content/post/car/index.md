---
title: Route Planning for self driving cars
description: Value iteration and Q-learning
date: 2021-05-07 
image: car.png
categories:
    - Reinforcement learning
tags:
    - Q-learning
    - Value iteration
    - Markov chain
---

{{< figure src="car.png" title="Snapshot of the environment, we are driving the green car" width=60% >}}


Model the environment as a time to collision matrix.

{{< figure src="TTC.png" title="Time to collision (TTC) matrix" width=60% >}}

5 available actions A(s), which are: {0: ‘LANE_LEFT’, 1: ‘IDLE’, 2: ‘LANE_RIGHT’, 3: ‘FASTER’, 4: ‘SLOWER’}

![Value function when the car is driving](<car driving.gif>)