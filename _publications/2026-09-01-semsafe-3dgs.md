---
title: 'SemSafe-3DGS: Semantic Risk-Aware Active Navigation in Uncertain 3D Gaussian Splatting Maps'
collection: publications
category: conferences
permalink: /publication/2026-09-01-semsafe-3dgs
excerpt: 'Class-dependent risk weights modulate an AV@R clearance model, so semantically different obstacles produce different control responses. Includes real-robot results under Ackermann dynamics.'
date: 2026-09-01
venue: 'SeMaNa Workshop, IEEE/RSJ International Conference on Intelligent Robots and Systems (IROS)'
paperurl: 'https://arxiv.org/abs/2609.19330'
citation: '<b>A. Mollaei Khass</b>, A. Cosse, and N. Motee. (2026). &quot;SemSafe-3DGS: Semantic Risk-Aware Active Navigation in Uncertain 3D Gaussian Splatting Maps.&quot; <i>SeMaNa Workshop, IEEE/RSJ International Conference on Intelligent Robots and Systems (IROS)</i>.'
---

{% include base_path %}

**Accepted for presentation at the SeMaNa 2026 workshop at IROS 2026.**

Safety formulations for navigation usually reason about geometry alone. A consequence is that
two obstacles with the same shape get the same treatment even when the cost of touching them is
not remotely the same.

This paper attaches semantic attributes to the 3D Gaussian map and lets them modulate an Average
Value-at-Risk clearance model through class-dependent risk weights. Safety-critical primitives
therefore carry more influence in the composite barrier. The weighted clearances aggregate into
a control barrier function, and a separate trajectory-relevant perception barrier rewards
observations that cut geometric map uncertainty along the motion the robot is about to execute.

Both go into a unified CBF-QP: semantic risk-aware collision avoidance is enforced as a hard
constraint, and information acquisition is relaxed where it fights safety or task progress. The
evaluation covers semantic-dependent trajectory adaptation and execution on a real robot with
Ackermann dynamics.

**Links:** [arXiv](https://arxiv.org/abs/2609.19330) &middot;
[Workshop poster (PDF)]({{ base_path }}/files/semsafe-poster.pdf)

### BibTeX

```bibtex
@inproceedings{mollaeikhass2026semsafe,
  title     = {SemSafe-3DGS: Semantic Risk-Aware Active Navigation in
               Uncertain 3D Gaussian Splatting Maps},
  author    = {Mollaei Khass, Amirhossein and Cosse, Athanasios and
               Motee, Nader},
  booktitle = {SeMaNa Workshop, IEEE/RSJ International Conference on
               Intelligent Robots and Systems (IROS)},
  year      = {2026},
  note      = {arXiv:2609.19330}
}
```
