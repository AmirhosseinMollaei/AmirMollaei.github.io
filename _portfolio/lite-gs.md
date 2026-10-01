---
title: "LiTe-GS: Oracle-Efficient Next Best View Selection"
collection: portfolio
order: 5
date: 2026-09-24
video: lite-gs.mp4
excerpt: "Under review, WACV 2027. Scores a randomized subset of candidate views instead of the full pool, with proved oracle complexity and an explicit dial between efficiency and approximation quality."
---

{% include demo-video.html src="lite-gs.mp4" caption="Oracle-efficient next-best-view selection for 3D Gaussian Splatting." %}

Choosing informative camera views matters when training and refining a 3D Gaussian Splatting model,
because each observation moves the parameters a lot. The cost is that information-driven selection
keeps calling an expensive information-gain oracle, and the number of calls grows with the size of
the candidate pool.

LiTe-GS evaluates a randomized subset of candidates rather than scoring the pool exhaustively. The
result is expected `O(M log(1/e))` oracle complexity in the number of candidates `M`, independent of
how many views are finally selected, and the parameter `e` is an explicit dial between oracle
efficiency and approximation quality. The paper proves bounds on both.

On Blender and Mip-NeRF 360, reconstruction quality holds up against Fisher-information baselines
while the number of Fisher-oracle evaluations drops substantially across acquisition settings.

**Under review** at WACV 2027.

- [Paper on arXiv](https://arxiv.org/abs/2609.30393)
