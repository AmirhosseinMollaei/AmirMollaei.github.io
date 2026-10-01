---
title: 'Conflict-Aware Active Perception and Control in 3D Gaussian Splatting Fields via Control Barrier Functions'
collection: publications
category: conferences
permalink: /publication/2026-12-01-conflict-aware-active-perception-cbf
excerpt: '<b>Invited session paper, CDC 2026.</b> Safety as a hard CBF constraint from an AV@R risk metric, perception as slack-relaxed constraints, both inside one quadratic program.'
date: 2026-12-01
venue: 'IEEE Conference on Decision and Control (CDC), invited session paper'
paperurl: 'https://arxiv.org/abs/2605.20566'
citation: '<b>A. Mollaei Khass</b>, A. Cosse, V. Pandey, and N. Motee. (2026). &quot;Conflict-Aware Active Perception and Control in 3D Gaussian Splatting Fields via Control Barrier Functions.&quot; <i>IEEE Conference on Decision and Control (CDC)</i>. Invited session paper.'
---

**Accepted as an invited session paper at CDC 2026.**

Informative viewpoints tend to sit near the uncertain regions that are also the riskiest to
approach, so active perception and safety do not simply coexist. This paper treats that as the
central design problem rather than a tuning detail.

Safety comes from a control barrier function derived from an Average Value-at-Risk collision
metric over the 3D Gaussian Splatting field. Because the metric is built on the geometric
uncertainty the map carries, the guarantee is forward invariance of a safe set defined against
that uncertainty, not against a binarized occupancy grid.

Perception is handled by a risk-aware expected-information-gain term for next-best-view
selection, plus perception barrier functions that turn the camera toward the local direction of
information ascent. Safety and perception then enter a single quadratic program in which safety
is hard and the perception constraints carry slack variables, so the program stays solvable when
the two genuinely cannot both be satisfied.

**Links:** [arXiv](https://arxiv.org/abs/2605.20566) &middot;
[Project page](https://sircesoc.github.io/Conflict_Aware_Active_Perception/) &middot;
[Code](https://github.com/sircesoc/Conflict_Aware_Active_Perception)

### BibTeX

```bibtex
@inproceedings{mollaeikhass2026conflict,
  title     = {Conflict-Aware Active Perception and Control in 3D Gaussian
               Splatting Fields via Control Barrier Functions},
  author    = {Mollaei Khass, Amirhossein and Cosse, Athanasios and
               Pandey, Vivek and Motee, Nader},
  booktitle = {IEEE Conference on Decision and Control (CDC)},
  year      = {2026},
  note      = {Invited session paper. arXiv:2605.20566}
}
```
