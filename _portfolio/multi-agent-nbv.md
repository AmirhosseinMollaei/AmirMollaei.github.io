---
title: "Multi-Agent Next-Best-View Optimization for Risk-Averse Planning"
collection: portfolio
order: 6
date: 2026-06-02
video: multi-agent-nbv.mp4
excerpt: "Preprint, 2026. Each robot keeps its own 3D Gaussian Splatting map private; the team reaches consensus on informative viewpoints through C-ADMM, exchanging only viewpoints, trajectory descriptors and scalar information-gain values."
---

{% include demo-video.html src="multi-agent-nbv.mp4" caption="Distributed risk-aware next-best-view selection across a team of robots holding separate local maps." %}

Coordinating next-best-view selection across a team is where the centralized version of this
problem stops scaling. Either the robots share raw sensor data, or they pay a communication cost
that grows faster than the team does.

This work keeps each robot's map private. Every agent maintains its own local 3D Gaussian Splatting
map, and the team jointly maximizes expected information gain restricted to masked zones along the
planned trajectories. The distributed objective is solved with Consensus ADMM over a communication
graph, and what crosses the network is only candidate viewpoints, planned trajectory descriptors,
and scalar EIG contributions.

Safety enters as it does in the single-robot work: collision risk along each trajectory is modeled
with Average Value-at-Risk over the local 3DGS map, and that risk both sets the masking radius and
scores the planned paths.

Experiments in Gibson environments at several team sizes show the distributed formulation
approaching the centralized baseline on mapping quality and trajectory safety, while cutting
communication by orders of magnitude.

**Preprint, 2026.**

- [Paper on arXiv](https://arxiv.org/abs/2606.04158)
