---
permalink: /
title: "About"
author_profile: true
redirect_from:
  - /about/
  - /about.html
---

{% include base_path %}

I am a PhD student in [Mechanical Engineering](https://engineering.lehigh.edu/mem) at
[Lehigh University](https://www.lehigh.edu/) in Bethlehem, Pennsylvania, where I started in 2023.
I work in the Autonomous and Intelligent Robotics Lab (AIRLab) with
[Prof. Nader Motee](https://engineering.lehigh.edu/faculty/nader-motee).

I work on robots that have to stay safe while they are still figuring out what is around them. My
papers put the safety guarantee and the perception objective into the same optimization problem,
solved at control rates, so neither one is a post-hoc filter on the other.

> *I am looking for a **Summer 2027 research internship** in robot perception, planning, and control. If your team works on these problems, I would be glad to hear from you.*

{% include demo-video.html src="hero.mp4" caption="Safe active perception running online in Isaac Sim: a 3D Gaussian-splat map, a risk-aware barrier, and next-best-view selection in the loop." %}

Each paper's demo is on the [Research]({{ base_path }}/portfolio/) page.

## Research

A robot moving through an unfamiliar space has to do two things with one control input. It has to
pick viewpoints that tell it more about the scene, and it has to stay inside the region it can
confirm is free. The two goals pull against each other. The viewpoint that reveals the most is
usually the one closest to what the robot has not mapped yet. My work writes that tradeoff down
explicitly and solves it fast enough to run online.

### Safety as a hard constraint

I build control barrier functions from Average Value-at-Risk collision metrics evaluated over an
entire 3D Gaussian Splatting map. Because the risk metric reads the geometric uncertainty the map
carries, what the barrier certifies is forward invariance of a safe set defined against that
uncertainty. Nothing is thresholded into free or occupied first, so the guarantee is about the scene
rather than about a grid.

In [SemSafe-3DGS]({{ base_path }}/portfolio/semsafe-3dgs/) the clearance model is also modulated by semantics, with
class-dependent risk weights, so obstacles that are geometrically alike but consequentially
different stop producing the same control response.

### Perception as a soft objective

View quality enters the same quadratic program as a constraint that can be relaxed. I score it with
risk-aware expected information gain, and add perception barrier functions that turn the camera
toward the local direction of information ascent. The perception constraints carry slack variables,
so when there is no safe way left to see more, perception yields and the program still solves
instead of going infeasible.

### Scaling to teams

For a team of robots, next-best-view planning becomes a coupled optimization problem. I solve it
with consensus ADMM, so no agent needs the full map.

**Interests:** safe active perception, control barrier functions, next-best-view planning,
3D Gaussian Splatting, risk-aware control, distributed optimization, multi-agent robotics.

## News

<!-- To add a news item, copy the line format below and put it at the TOP of this list. -->
<!-- - **[Mon YYYY]** What happened. -->

- **[Sep 2026]** Posted *AGILE-GS* to arXiv, under review at WACV 2027.
- **[Sep 2026]** Posted the *LiTe-GS* preprint to arXiv.
- **[Sep 2026]** Posted the *Splat-CBF* preprint to arXiv.
- **[Sep 2026]** Presented *SemSafe-3DGS* at the SeMaNa workshop, IROS 2026.
- **[Jul 2026]** Presented at ECC 2026 in Reykjavik.
- **[Jun 2026]** Presented at ICRA 2026 in Vienna.
- **[May 2026]** Our CDC 2026 paper was accepted as an invited session paper.

## Education

- **Ph.D.**, Mechanical Engineering, Lehigh University, 2023&ndash;present
- **M.S.**, 2025. `TODO: field and institution`
- **B.S.** `TODO: field, institution, and year`

## Teaching

Teaching assistant at Lehigh University for **Convex Optimization** and **Control Systems**.

`TODO: any other courses to list here`
