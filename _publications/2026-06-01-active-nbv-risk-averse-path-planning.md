---
title: 'Active Next-Best-View Optimization for Risk-Averse Path Planning'
collection: publications
category: conferences
permalink: /publication/2026-06-01-active-nbv-risk-averse-path-planning
excerpt: 'Couples risk-averse path refinement with next-best-view selection, using Average Value-at-Risk statistics computed on an online 3D Gaussian-splat radiance field.'
date: 2026-06-01
venue: 'IEEE International Conference on Robotics and Automation (ICRA)'
paperurl: 'https://arxiv.org/abs/2510.06481'
citation: '<b>A. Mollaei Khass</b>, G. Liu, V. Pandey, W. Jiang, B. Lei, K. Daniilidis, and N. Motee. (2026). &quot;Active Next-Best-View Optimization for Risk-Averse Path Planning.&quot; <i>IEEE International Conference on Robotics and Automation (ICRA)</i>.'
---

Safe movement through a partly known space needs two kinds of reasoning at once: how risky a
motion is, and how much a future observation is worth. This paper handles both from one
representation.

A coarse reference path is refined against a risk field built from Average Value-at-Risk
statistics evaluated on an online 3D Gaussian-splat radiance field. A local A\* search runs
over the subset of grid points that survive the risk filter, which yields a short-horizon
trajectory that is both dynamically feasible and conservative about what the map does not pin
down.

View selection is then posed as optimization on the pose manifold. A Riemannian gradient scheme
maximizes expected information gain under a proximity-weighted Fisher-information objective,
restricted to the region masked around the planned trajectory. The effect is that the robot
spends its looking where it is about to move, rather than reducing uncertainty uniformly.

**Links:** [arXiv](https://arxiv.org/abs/2510.06481) &middot;
[Code and project page](https://github.com/AmirhosseinMollaei/Risk-Averse-Next-best-view-selection)

### BibTeX

```bibtex
@inproceedings{mollaeikhass2026nbv,
  title     = {Active Next-Best-View Optimization for Risk-Averse Path Planning},
  author    = {Mollaei Khass, Amirhossein and Liu, Guangyi and Pandey, Vivek and
               Jiang, Wen and Lei, Boshu and Daniilidis, Kostas and Motee, Nader},
  booktitle = {IEEE International Conference on Robotics and Automation (ICRA)},
  year      = {2026},
  note      = {arXiv:2510.06481}
}
```
