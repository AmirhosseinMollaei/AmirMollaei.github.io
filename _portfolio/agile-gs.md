---
title: "AGILE-GS: Anchor-Guided Fast Next-Best-View Selection"
collection: portfolio
excerpt: "Under review, WACV 2027. Separates searching for information from choosing a camera, so the expensive oracle never has to score the whole candidate pool. One to two orders of magnitude less selection latency."
---

{% include demo-video.html src="agile-gs.mp4" caption="Anchor-guided next-best-view selection for active 3D Gaussian Splatting." %}

A radiance field needs hundreds of views, and where they are placed matters as much as how many
there are. The standard next-best-view loop for 3D Gaussian Splatting scores every candidate in the
pool and keeps one. That conflates two different problems: finding where the information is, and
picking a camera you can actually use.

AGILE-GS splits them. A virtual anchor pose is optimized on SE(3) by Riemannian gradient ascent on
expected information gain. The anchor does not have to be reachable, or even be in the candidate
pool at all; its job is to mark where the model is most uncertain. Candidates are then scored
against the anchor's viewing geometry, and a greedy ridge-leverage step distills the pool into a
short, non-redundant shortlist without rendering a single candidate.

The shortlist can be spent two ways. AGILE-GS takes the first entry, so no Fisher information is
computed for any candidate at all. AGILE-GS+ evaluates only the shortlisted views, so the expensive
step runs over a handful instead of the whole pool. On standard benchmarks and in closed-loop
embodied acquisition, both match or beat existing baselines while cutting selection latency by one
to two orders of magnitude.

**Under review** at WACV 2027.

- [Paper on arXiv](https://arxiv.org/abs/2609.34176)
