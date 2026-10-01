---
title: "Splat-CBF: Safe Next-Best-View Control"
collection: portfolio
excerpt: "Under review at ICRA 2027. Barrier functions built directly on a 3D Gaussian-splat map, so the safety check uses the map's own uncertainty instead of a thresholded occupancy grid."
---

{% include demo-video.html src="splatcbf.mp4" caption="Safe next-best-view control in a 3D Gaussian-splat map." %}

The usual way to get a safety guarantee out of a learned map is to threshold it into free and
occupied cells first, then plan against that. Thresholding discards how confident the map actually
was, and the guarantee ends up being about the grid rather than about the scene.

Splat-CBF builds the barrier condition on the Gaussian-splat representation itself. The safety
constraint is evaluated against the uncertainty the splats carry, and next-best-view control runs
inside that constraint, so the robot picks informative viewpoints without leaving the region it can
still certify.

Currently **under review** at IEEE ICRA 2027.

- `TODO: arXiv link once the preprint is posted`
- `TODO: code repository link, if there is one to share`
