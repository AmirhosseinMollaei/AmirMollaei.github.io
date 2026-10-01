---
title: "Active Next-Best-View Optimization for Risk-Averse Path Planning"
collection: portfolio
excerpt: "ICRA 2026. Risk-averse path refinement and next-best-view selection driven from the same online Gaussian-splat map, so the robot looks where it is about to move. Includes video and the full pipeline figure."
---

{% include base_path %}

{% include demo-video.html src="nbv-risk-averse.mp4" caption="Risk-averse navigation with active next-best-view selection on an online 3D Gaussian-splat map." %}

A robot refining a path through a partly mapped space has to answer two questions with one control
input: how risky is this motion, and how much is the next observation worth. Answering them
separately wastes the fact that both are questions about the same uncertain map.

This work builds both from one representation. A coarse reference path is refined against a risk
field computed from Average Value-at-Risk statistics over an online 3D Gaussian-splat radiance
field. A local A\* search runs only over grid points that survive the risk filter, producing a
short-horizon trajectory that is dynamically feasible and conservative where the map is thin.

View selection is then an optimization on the pose manifold. A Riemannian gradient scheme maximizes
a proximity-weighted Fisher-information objective, restricted to a mask around the planned
trajectory. That coupling is the point: the executed controls keep the robot on a safe path, and the
selected views spend sensing budget on the regions that are about to matter.

<figure>
  <img src="{{ base_path }}/images/nbv-risk-averse-pipeline.png"
       alt="Pipeline: 3DG-SLAM feeds local risk-averse path planning, then risk-aware masking, then the NBV optimizer, which closes the loop through executed actions.">
  <figcaption>The loop. 3DG-SLAM maintains the splat map; risk-averse planning produces a local
  trajectory; masking restricts attention to the risk-relevant region; the NBV optimizer picks the
  views that reduce uncertainty there.</figcaption>
</figure>

**Published at** IEEE ICRA 2026, Vienna.

- [Paper on arXiv](https://arxiv.org/abs/2510.06481)
- [Code and project page](https://github.com/AmirhosseinMollaei/Risk-Averse-Next-best-view-selection)
