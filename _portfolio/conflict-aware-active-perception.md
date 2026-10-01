---
title: "Conflict-Aware Active Perception and Control"
collection: portfolio
excerpt: "Invited session paper, CDC 2026. Seeing more and staying safe are in conflict. This work puts both in one quadratic program over a 3D Gaussian Splatting field."
---

{% include demo-video.html src="caap.mp4" caption="Conflict-aware active perception and control in a 3D Gaussian Splatting field." %}

A robot that wants to reduce its uncertainty about a scene is pulled toward the parts of the scene
it has not mapped. Those are the same parts it cannot yet certify as safe to enter. The two
objectives share one control input, so one of them has to give way.

This work writes the conflict into a single quadratic program. Safety is a hard constraint, built
from control barrier functions defined over the whole 3D Gaussian Splatting field, so the condition
is checked against the uncertainty the map carries. View quality is a soft constraint in the same
program, scored with an information-theoretic measure. When no safe motion improves the view, the
perception term is what relaxes.

This paper was accepted as an **invited session paper** at the IEEE Conference on Decision and
Control (CDC) 2026.

- [Paper on arXiv](https://arxiv.org/abs/2605.20566)
- `TODO: code repository link, if there is one to share`
