---
title: "Splat-CBF: Safe Next-Best-View Control"
collection: portfolio
excerpt: "Under review at ICRA 2027. The barrier condition is built on the Gaussian-splat map itself, so the safety certificate is about the scene rather than about a thresholded grid."
---

{% include demo-video.html src="splatcbf.mp4" caption="Safe next-best-view control in a 3D Gaussian-splat map." %}

The standard way to get a safety guarantee out of a learned map is to threshold it into free and
occupied cells, then plan against the result. That step is where the information goes. Thresholding
discards how confident the map was, and what you can prove afterwards is a property of the grid, not
of the environment the robot is in.

Splat-CBF puts the barrier condition on the Gaussian-splat representation directly, so the safety
check reads the uncertainty the splats carry. Next-best-view control then runs inside that
constraint. The robot pursues informative viewpoints while staying in the set it can still certify,
and the certificate degrades gracefully where the map is genuinely unsure rather than flipping at a
threshold.

**Status:** under review at IEEE ICRA 2027, submitted October 2026.

- `TODO: arXiv link once the preprint is posted`
- `TODO: code repository link, if there is one to share`
