---
title: "SemSafe-3DGS: Semantic Risk-Aware Active Navigation"
collection: portfolio
excerpt: "SeMaNa Workshop, IROS 2026. Uses semantic labels in an uncertain Gaussian Splatting map, so how much clearance the robot keeps depends on what the unmapped region probably is."
---

{% include demo-video.html src="semsafe.mp4" caption="Semantic risk-aware active navigation in an uncertain 3D Gaussian Splatting map." %}

Not all uncertainty carries the same cost. A volume the robot cannot see behind a solid wall and a
volume it cannot see across open floor are both unmapped, but entering them means different things.
Treating uncertainty as a single scalar throws that distinction away.

SemSafe-3DGS keeps semantic labels in the Gaussian Splatting map and lets the navigation policy use
them. The risk assigned to an unmapped region depends on what the surrounding semantics suggest it
contains, so the clearance the robot holds varies with the kind of obstacle it is likely to be
approaching rather than being fixed in advance.

Presented at the SeMaNa workshop, IEEE/RSJ IROS 2026.

- [Paper on arXiv](https://arxiv.org/abs/2609.19330)
- `TODO: code repository link, if there is one to share`
