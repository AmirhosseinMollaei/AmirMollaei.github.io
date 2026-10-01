---
title: 'Multi-Agent Next-Best-View Optimization for Risk-Averse Planning'
collection: publications
category: manuscripts
permalink: /publication/2026-06-02-multi-agent-nbv-risk-averse
excerpt: 'Each robot keeps a private local 3D Gaussian Splatting map and the team maximizes expected information gain jointly through Consensus ADMM, exchanging only viewpoints, trajectory descriptors and scalar EIG contributions.'
date: 2026-06-02
venue: 'Preprint'
paperurl: 'https://arxiv.org/abs/2606.04158'
citation: '<b>A. Mollaei Khass</b>, V. Pandey, G. Liu, A. Cosse, E. Bayrak, and N. Motee. (2026). &quot;Multi-Agent Next-Best-View Optimization for Risk-Averse Planning.&quot; <i>Preprint</i>. arXiv:2606.04158.'
---

Coordinating next-best-view selection across a team is where the centralized version of this
problem stops scaling. Sharing raw sensor data, or the communication overhead that replaces it,
grows faster than the team does.

This paper keeps the map private. Each robot maintains its own local 3D Gaussian Splatting map, and
the team jointly maximizes expected information gain restricted to masked zones along the planned
trajectories. The resulting distributed objective is solved with Consensus ADMM over a
communication graph, and each robot exchanges only candidate viewpoints, planned trajectory
descriptors, and scalar EIG contributions. Nothing about the map itself leaves the robot.

Safety enters the same way it does in the single-robot work. Collision risk along each trajectory
is modeled with Average Value-at-Risk over the local 3DGS map, and that risk both shapes the
masking radius and scores the planned paths.

Experiments in Gibson environments across several team sizes show the distributed formulation
approaching the centralized baseline on mapping quality and trajectory safety while cutting
communication by orders of magnitude.

**Links:** [arXiv](https://arxiv.org/abs/2606.04158)

### BibTeX

```bibtex
@article{mollaeikhass2026multiagent,
  title   = {Multi-Agent Next-Best-View Optimization for Risk-Averse Planning},
  author  = {Mollaei Khass, Amirhossein and Pandey, Vivek and Liu, Guangyi and
             Cosse, Athanasios and Bayrak, Emrah and Motee, Nader},
  journal = {arXiv preprint arXiv:2606.04158},
  year    = {2026}
}
```
