---
title: "TRACE: Privacy-Preserving Next-Best-View Selection"
collection: portfolio
excerpt: "Under review, ICRA 2027. A distributed next-best-view protocol that coordinates information acquisition across a team while each robot keeps its own observations and map parameters private."
---

{% include demo-video.html src="trace.mp4" caption="Privacy-preserving next-best-view selection over distributed 3D Gaussian-splat maps." %}

A team of robots exploring together has an obvious reason to coordinate: two agents should not spend
their sensing budget on the same region. The usual way to arrange that is to pool the maps, which
assumes every agent is willing to hand over what it has seen.

TRACE coordinates the next-best-view decision without that assumption. The protocol is distributed,
and each robot keeps its own observations and its Gaussian map parameters private while still
contributing to a joint acquisition plan.

**Under review** at IEEE ICRA 2027.

`TODO: arXiv link once the preprint is posted.`
