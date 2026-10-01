---
title: "Conflict-Aware Active Perception and Control"
collection: portfolio
date: 2026-12-01
video: caap.mp4
excerpt: "Invited session paper, CDC 2026. Seeing more and staying safe genuinely conflict. Safety is a hard CBF constraint, perception is relaxed through slack, and both live in one quadratic program."
---

{% include demo-video.html src="caap.mp4" caption="Conflict-aware active perception and control in a 3D Gaussian Splatting field." %}

The informative viewpoint and the safe viewpoint are usually not the same viewpoint. What a robot
most needs to look at is the region it has not mapped, and that is exactly the region it cannot yet
certify as free. Most pipelines resolve this with a weight someone tuned. This work resolves it in
the formulation.

Safety is enforced by a control barrier function derived from an Average Value-at-Risk collision
metric over the 3D Gaussian Splatting field. Because that metric is built from the geometric
uncertainty the map actually carries, what the CBF guarantees is forward invariance of a safe set
defined against that uncertainty. Nothing gets thresholded into free or occupied first.

Perception contributes two things: a risk-aware expected-information-gain term for choosing the next
view, and perception barrier functions that rotate the camera toward the local direction of
information ascent. Safety and perception then meet in one quadratic program, where safety is a hard
constraint and the perception constraints carry slack variables. When the two cannot both be
satisfied, perception yields and the program still has a solution.

**Accepted as an invited session paper** at IEEE CDC 2026.

- [Paper on arXiv](https://arxiv.org/abs/2605.20566)
- [Project page](https://sircesoc.github.io/Conflict_Aware_Active_Perception/)
- [Code](https://github.com/sircesoc/Conflict_Aware_Active_Perception)
