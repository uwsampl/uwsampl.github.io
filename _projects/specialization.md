---
title: Sequential Model Specialization

description: |
  Fast Video Classification via Adaptive Cascading of Deep Models

people:
  - haichen
  - seungyeop
  - arvind
  - matthai

layout: project
last-updated: 2018-03-05
---

In this project, we consider recognizing entities such as objects, people, 
scenes and activities in every frame of video footage of day-to-day life. In
principle, these entities could be drawn from thousands of classes. Recent 
advances in convolutional neural networks (CNNs) have opened up the possibility 
of using a single, pre-trained “oracle” classifier to recognize thousands of 
classes. However, these classifiers are relatively heavyweight, so that applying 
them to classify every frame of video is costly.

We show that day-to-day video exhibits highly skewed class
distributions over the short intervals. To exploit such temporal locality, we propose an architecture that cascades a cheap classifier (7-200x fewer FLOPs) with the oracle shown in the figure below.
We demonstrate that when class distribution is highly skewed toward small sets of classes, “specialized” models have comparable accuracy.

{:center: style="text-align: center"}
![specialized model](/img/specialization/specialized_model.png){: width="50%"}
{:center}

We formulate the problem of detecting the short-term skews
online and exploiting models based on it as a new sequential decision making
problem dubbed the Online Bandit Problem, and present a new algorithm to solve
it. When applied to recognizing faces in TV shows and movies, we realize
end-to-end classification speedups of **2.4-7.8x/2.6-11.2x** (on GPU/CPU)
relative to a state-of-the-art convolutional neural network, at competitive
accuracy.



## Reference Paper

- Haichen Shen, Seungyeop Han, Matthai Philipose, and Arvind Krishnamurthy. [Fast Video Classification via Adaptive Cascading of Deep Models](https://homes.cs.washington.edu/~haichen/papers/specialization.pdf). CVPR 2017 (**spotlight**)

