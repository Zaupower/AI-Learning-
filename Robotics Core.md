# Robotics Core — Study Guide

Two courses taken in parallel: one geometric/model-based (Tedrake), one classical mechanics (Lynch & Park).

---

## MIT 6.4210: Robotic Manipulation (Russ Tedrake)

The single best manipulation course. Geometric pose estimation, grasping, motion planning, deep-learning-based manipulation, deformable objects. Updated every year, full interactive notes, Colab problem sets in Drake.

- **Course notes (HTML, main version):** [manipulation.csail.mit.edu](https://manipulation.csail.mit.edu/)
- **Fall 2025 offering:** [manipulation.csail.mit.edu/Fall2025](https://manipulation.csail.mit.edu/Fall2025/)
- **PDF version:** [github.com/RussTedrake/manipulation/releases](https://github.com/RussTedrake/manipulation/releases)
- **MIT OCW (Fall 2022, with lecture videos):** [ocw.mit.edu/courses/6-4210](https://ocw.mit.edu/courses/6-4210-robotic-manipulation-fall-2022/)
- **Code repo:** [github.com/RussTedrake/manipulation](https://github.com/RussTedrake/manipulation)
- **Drake (simulator/toolbox used throughout):** [drake.mit.edu](https://drake.mit.edu/)
- **Fall 2022 Lecture 1 (YouTube):** [Watch](https://www.youtube.com/watch?v=QlrRb7X4JvA)

### Prerequisites

Linear algebra, basic probability, Python. No robotics experience required. Tedrake recommends brushing up on:
- Linear algebra: [MIT 18.06 (Gilbert Strang, OCW)](https://ocw.mit.edu/courses/mathematics/18-06-linear-algebra-spring-2010/)
- Convex optimization (optional): [Boyd lectures (YouTube)](https://youtube.com/playlist?list=PL3940DD956CDF0622), [textbook (free)](https://web.stanford.edu/~boyd/cvxbook/)

### Chapters & Topics

Work through the HTML notes chapter by chapter. Each has exercises at the end — these are the problem sets.

| Ch | Title | Topics | Link |
|----|-------|--------|------|
| 1 | Introduction | What is manipulation, open-world manipulation, simulation, model-based design | [Read](https://manipulation.csail.mit.edu/intro.html) |
| 2 | Let's Get You a Robot | URDF/SDF, arms (position vs torque control), grippers, sensors, HardwareStation in Drake | [Read](https://manipulation.csail.mit.edu/robot.html) |
| 3 | Basic Pick and Place | Spatial transforms, forward kinematics, Jacobians, differential IK, grasp/pre-grasp poses, trajectories | [Read](https://manipulation.csail.mit.edu/pick.html) |
| 4 | Geometric Pose Estimation | Cameras, depth sensors, point clouds, ICP, outlier handling, segmentation, tracking | [Read](https://manipulation.csail.mit.edu/pose.html) |
| 5 | Bin Picking | Cluttered scenes, contact/friction, static equilibrium, model-based grasp selection, grasp from point clouds, state machines, LLMs for task planning | [Read](https://manipulation.csail.mit.edu/clutter.html) |
| 6 | Motion Planning | Inverse kinematics, trajectory optimization, RRT, PRM, Graphs of Convex Sets (GCS), time-optimal paths | [Read](https://manipulation.csail.mit.edu/trajectories.html) |
| 7 | Mobile Manipulation | Active perception, wheeled/legged robots, navigation, mapping | [Read](https://manipulation.csail.mit.edu/mobile.html) |
| 8 | Manipulator Control | Trajectory tracking, force control, impedance/stiffness control, operational space control, peg-in-hole | [Read](https://manipulation.csail.mit.edu/force.html) |
| 9 | Object Detection & Segmentation | Crowd-sourced datasets, fine-tuning, synthetic data, self-supervised learning, large-scale models | [Read](https://manipulation.csail.mit.edu/segmentation.html) |
| 10 | Deep Perception for Manipulation | Learned pose estimation, grasp selection, semantic keypoints, dense correspondences, scene flow | [Read](https://manipulation.csail.mit.edu/deep_perception.html) |
| 11 | Reinforcement Learning | Policy gradients, value-based methods, model-based RL for manipulation | [Read](https://manipulation.csail.mit.edu/rl.html) |
| 12 | Soft Robots & Tactile Sensing | Soft hardware, soft-body simulation, visuotactile sensing (GelSight etc.), perception and control with touch | [Read](https://manipulation.csail.mit.edu/tactile.html) |

### Priority for your cloth project

Chapters 1–6 are core — do all of them with exercises. Chapter 8 (control) matters for real hardware. Chapters 9–10 (deep perception) are directly relevant to perceiving crumpled garments. Chapter 11 (RL) bridges to CS285. Chapter 12 (tactile) is bonus but interesting for cloth grasping.

---

## Modern Robotics (Lynch & Park, Northwestern)

Kinematics, dynamics, screw theory, control. The mathematical backbone. Free textbook, free videos, free software.

- **Textbook (free preprint PDF):** [modernrobotics.northwestern.edu](https://modernrobotics.northwestern.edu/)
- **Wiki + all resources:** [hades.mech.northwestern.edu/Modern_Robotics](https://hades.mech.northwestern.edu/index.php/Modern_Robotics)
- **YouTube (all videos, one playlist):** [Modern Robotics playlist](https://www.youtube.com/playlist?list=PLggLP4f-rq02vX0OQQ5vrCxbJrzamYDfx)
- **Software (Python/MATLAB):** [github.com/NxRLab/ModernRobotics](https://github.com/NxRLab/ModernRobotics)
- **Cambridge University Press page:** [cambridge.org/Modern-Robotics](https://www.cambridge.org/core/books/modern-robotics/57C3BB1C6D5CB40320FA96E5FA3BCEC6)

### What to cover

Lynch himself skips Chapters 7, 10, and 12 in his own class. Focus on:

| Ch | Title | Topics | Priority |
|----|-------|--------|----------|
| 2–3 | Configuration Space & Rigid-Body Motions | Degrees of freedom, rotation matrices, SO(3), homogeneous transforms, screws | Core |
| 4 | Forward Kinematics | Product of exponentials formula | Core |
| 5 | Velocity Kinematics & Statics | Jacobians, manipulability, statics | Core |
| 6 | Inverse Kinematics | Analytical and numerical IK | Core |
| 8 | Dynamics of Open Chains | Newton-Euler, Lagrangian, mass matrix, forward/inverse dynamics | Core |
| 9 | Trajectory Generation | Point-to-point, polynomial, time scaling | Useful |
| 11 | Robot Control | PID, computed torque, force control, impedance control | Useful |
| 13 | Wheeled Mobile Robots | Kinematics, motion planning | Optional |

### How to use it

Watch the videos (short, 5–15 min each, Lightboard format) before reading the chapter. Do the end-of-chapter exercises. Use the Python library to verify your solutions computationally.

---

## Optional: Underactuated Robotics (Russ Tedrake)

Deeper control theory — nonlinear dynamics, Lyapunov analysis, trajectory optimization, LQR, model predictive control. Not required for cloth manipulation (perception and policy dominate), but excellent if you want a stronger controls foundation.

- **Course notes:** [underactuated.csail.mit.edu](https://underactuated.csail.mit.edu/)
- **MIT OCW:** [ocw.mit.edu/courses/6-832](https://ocw.mit.edu/courses/6-832-underactuated-robotics-spring-2009/)

---

## Suggested sequencing

```
Week 1–2:   Modern Robotics Ch 2–6 (kinematics) + Tedrake Ch 1–2 (setup)
Week 3–4:   Modern Robotics Ch 8–9 (dynamics) + Tedrake Ch 3–4 (pick-and-place, pose estimation)
Week 5–6:   Modern Robotics Ch 11 (control) + Tedrake Ch 5–6 (bin picking, motion planning)
Week 7–8:   Tedrake Ch 8–10 (control, detection, deep perception)
Week 9:     Tedrake Ch 11–12 (RL, tactile) — bridges to CS285
```

This pairs well with running CS285 in parallel starting around Week 3–4.
