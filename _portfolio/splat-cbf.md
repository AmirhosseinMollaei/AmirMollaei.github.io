---
title: "Splat-CBF: Safe Next-Best-View Control"
collection: portfolio
excerpt: "Preprint, 2026. One smooth hard constraint from the Average Value-at-Risk of the Gaussian field, plus a second barrier for informative camera orientations. Runs on a Kinova manipulator and an Ackermann-drive robot."
---

{% include demo-video.html src="splatcbf.mp4" caption="Safe next-best-view control in a 3D Gaussian-splat map." %}

Where to look and how to move are one question for a robot in an unmapped space, and the two answers
pull apart. The regions most worth observing are the ones the map knows least about, which are
exactly the regions where the robot cannot trust its collision margins.

Splat-CBF steers the camera toward the next best view while collision avoidance stays a hard
constraint. A risk-aware barrier turns the Average Value-at-Risk of the Gaussian field into a single
smooth hard constraint. A second barrier rewards camera orientations with high expected Fisher
information gain near the planned path. The two meet in a quadratic program where safety is hard and
perception is soft, and the slack penalty adapts to how often perception has already been relaxed
and how close the robot is to an uncertain region.

The method is verified in indoor simulation, on an Isaac Kinova manipulator, and on an
Ackermann-drive robot. It navigates faster and gathers more information than safety-only and
perception-only baselines, and gives up informative motion only when safety requires it.

**Preprint, 2026.**

- [Paper on arXiv](https://arxiv.org/abs/2609.23100)
