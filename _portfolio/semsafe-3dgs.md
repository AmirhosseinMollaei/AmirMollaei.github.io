---
title: "SemSafe-3DGS: Semantic Risk-Aware Active Navigation"
collection: portfolio
excerpt: "SeMaNa Workshop, IROS 2026. Class-dependent risk weights mean a glass door and a concrete pillar stop producing the same control response. Validated on a real Ackermann-steered robot."
---

{% include base_path %}

{% include demo-video.html src="semsafe.mp4" caption="Semantic risk-aware active navigation in an uncertain 3D Gaussian Splatting map." %}

Safety formulations for navigation almost always reason about geometry alone. The consequence is
that two obstacles with the same shape get the same clearance, even when the cost of touching them
is nothing alike. Geometry is simply not enough information to set a margin.

SemSafe-3DGS attaches semantic attributes to the 3D Gaussian map and lets them modulate an Average
Value-at-Risk clearance model through class-dependent risk weights. Primitives that are
safety-critical carry more influence in the composite barrier, and the weighted clearances aggregate
into a control barrier function. A separate trajectory-relevant perception barrier rewards
observations that reduce geometric map uncertainty along the motion the robot is about to execute.

Both objectives go into one CBF-QP. Semantic risk-aware collision avoidance is the hard constraint;
information acquisition is relaxed wherever it fights safety or task progress. The evaluation covers
semantic-dependent trajectory adaptation and runs on a real robot under Ackermann dynamics, not only
in simulation.

**Accepted for presentation** at the SeMaNa 2026 workshop, IEEE/RSJ IROS 2026.

- [Paper on arXiv](https://arxiv.org/abs/2609.19330)
- [Workshop poster (PDF)]({{ base_path }}/files/semsafe-poster.pdf)
