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
[Lehigh University](https://www.lehigh.edu/), in the
[Autonomous and Intelligent Robotics Lab (AIRLab)](https://robotics.lehigh.edu/), advised by
[Prof. Nader Motee](https://engineering.lehigh.edu/faculty/nader-motee). I started in 2023 and
passed the doctoral general examination in March 2026.

My research sits between robot perception and safety-critical control. A robot sent into an
unmapped space has to build its own scene representation while it moves, and it has to decide where
to point its camera next. Both decisions are made under a map that is still wrong in places the
robot cannot identify in advance. I work on making those decisions jointly, with a safety guarantee
that survives the uncertainty in the representation itself.

The representation I build on is **3D Gaussian Splatting**. An explicit, differentiable radiance
field is what makes safety-critical control tractable here: it rasterizes fast enough to stay in a
control loop, it admits analytic spatial queries for geometric risk, and its parameters carry an
uncertainty that can be read directly rather than thresholded away. Implicit fields give comparable
photometric quality but not the rendering latency or the analytic structure that a real-time barrier
condition needs.

On top of that representation I treat **active perception** as an optimization problem rather than a
heuristic. Candidate viewpoints are scored by expected information gain, typically through the
Fisher information of the splat parameters, and next-best-view selection is posed on the pose
manifold SE(3) and solved with Riemannian gradient methods. The recurring difficulty is cost: an
information oracle evaluated over every candidate does not fit in a control budget, so a thread of
my work is about getting the same view quality with a small fraction of the oracle calls.

**Safety** is where the perception objective stops being free. The most informative viewpoint is
usually adjacent to the region the map understands least, which is exactly the region whose
collision margins cannot be trusted. I encode safety as a control barrier function built on an
Average Value-at-Risk collision metric over the Gaussian field, so what gets certified is forward
invariance of a safe set defined against the map's own geometric uncertainty. Perception then enters
the same quadratic program as a relaxable constraint with slack, which makes the tradeoff explicit:
safety is never traded away, and informative motion yields only when there is no safe way to take
it.

The same machinery extends in two directions. Semantics let the risk model distinguish obstacles
that are geometrically alike but carry different consequences. Multi-robot settings turn
next-best-view selection into a coupled problem across agents, which I handle with distributed
optimization, including a formulation where agents coordinate acquisition without disclosing their
own observations or map parameters.

I care that this runs on hardware, not only in simulation. The methods have been validated in Isaac
Sim and on physical platforms, including Ackermann-steered mobile robots and a Kinova Gen3 7-DoF
manipulator.

> *I am looking for a **Summer 2027 research internship** in robot perception, planning, and control. If your team works on these problems, I would be glad to hear from you.*

{% include demo-video.html src="hero.mp4" caption="Safe active perception running online in Isaac Sim: a 3D Gaussian-splat map, a risk-aware barrier, and next-best-view selection in the loop." %}

## Research interests

- **Safe active perception** — joint perception and control under an uncertain map
- **Safety-critical control** — control barrier functions, forward invariance, CBF-QP formulations
- **Risk-aware control** — Average Value-at-Risk and other coherent risk measures over learned maps
- **Next-best-view planning** — information-theoretic view selection, expected information gain,
  Fisher information, oracle-efficient selection
- **3D Gaussian Splatting** — explicit differentiable radiance fields for real-time robotics
- **Active scene learning** — online map construction driven by what the robot still needs to see
- **Semantic risk reasoning** — class-dependent clearance and semantically attributed maps
- **Distributed and multi-robot optimization** — consensus ADMM, coupled next-best-view problems,
  privacy-preserving coordination
- **Optimization on manifolds** — Riemannian methods for pose and viewpoint optimization
- **Sim-to-real robotics** — Isaac Sim and Isaac Lab, Ackermann platforms, 7-DoF manipulation

Each paper below has a demo. The full list is on the
[Publications]({{ base_path }}/publications/) page, and longer write-ups are on the
[Research]({{ base_path }}/portfolio/) page.

## News

<!-- To add a news item, copy the line format below and put it at the TOP of this list. -->
<!-- - **[Mon YYYY]** What happened. -->

- **[Oct 2026]** *Splat-CBF* and *TRACE* are under review at ICRA 2027.
- **[Sep 2026]** *AGILE-GS* and *LiTe-GS* are under review at WACV 2027. Both preprints are on arXiv.
- **[Sep 2026]** Presented *SemSafe-3DGS* at the SeMaNa workshop, IROS 2026.
- **[Jul 2026]** Presented at ECC 2026 in Reykjavik.
- **[Jun 2026]** Presented at ICRA 2026 in Vienna.
- **[May 2026]** Our CDC 2026 paper was accepted as an invited session paper.
- **[Mar 2026]** Passed the PhD general examination at Lehigh.

## Education

- **Ph.D.**, Mechanical Engineering, Lehigh University, 2023&ndash;present.
  Doctoral general examination passed, March 2026.
- **M.S.**, Mechanical Engineering, Lehigh University, 2025
- **B.Sc.**, Sharif University of Technology, 2023

## Teaching

Teaching assistant at Lehigh University for **Convex Optimization** and **Control Systems**.

## Technical skills

- **Programming:** Python, C++, MATLAB
- **Robotics and simulation:** ROS/ROS2, Isaac Sim, Isaac Lab, Habitat-Sim, MuJoCo
- **Methods and tools:** PyTorch, 3D Gaussian Splatting, control barrier functions,
  convex optimization, Git, Linux
- **Platforms:** Kinova Gen3, Ackermann-steered mobile robots, RGB-D cameras
