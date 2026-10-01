---
permalink: /
title: "About"
author_profile: true
redirect_from:
  - /about/
  - /about.html
---

I am a PhD student in [Mechanical Engineering](https://engineering.lehigh.edu/mem) at
[Lehigh University](https://www.lehigh.edu/) in Bethlehem, Pennsylvania, where I started in 2023.
I work in the Autonomous and Intelligent Robotics Lab (AIRLab) with
[Prof. Nader Motee](https://engineering.lehigh.edu/faculty/nader-motee).
My research is on how a robot can stay safe while it is still working out what its surroundings
look like.

> *I am looking for a **Summer 2027 research internship** in robot perception, planning, and control. If your team works on these problems, I would be glad to hear from you.*

## Research

A robot moving through an unfamiliar space has to do two things with one control input. It has to
pick viewpoints that tell it more about the scene, and it has to stay inside the region it can
confirm is free. The two goals pull against each other. The viewpoint that reveals the most is
usually the one closest to what the robot has not mapped yet. My work writes that tradeoff down
explicitly and solves it fast enough to run online.

### Safety as a hard constraint

I define risk-averse control barrier functions over an entire 3D Gaussian Splatting map. The safety
condition is checked against the uncertainty the map itself carries, rather than against an
occupancy grid that has already been thresholded to free or occupied.

### Perception as a soft objective

View quality is scored with an information-theoretic measure, and it enters the same quadratic
program as a constraint that can be relaxed. The weight on its slack variable adapts when the robot
runs out of safe ways to see more.

### Scaling to teams

For a team of robots, next-best-view planning becomes a coupled optimization problem. I solve it
with consensus ADMM, so no agent needs the full map.

**Interests:** safe active perception, control barrier functions, next-best-view planning,
3D Gaussian Splatting, risk-aware control, distributed optimization, multi-agent robotics.

## News

<!-- To add a news item, copy the line format below and put it at the TOP of this list. -->
<!-- - **[Mon YYYY]** What happened. -->

- **[Oct 2026]** Submitted *Splat-CBF* to ICRA 2027.
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
