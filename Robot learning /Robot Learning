# Robot Learning / RL — Study Guide

Three resources: CS285 (deep RL theory), CS224R (practical robot learning), LeRobot tutorial (hands-on bridge to real hardware).

---

## Berkeley CS285: Deep Reinforcement Learning (Sergey Levine, Fall 2023)

The canonical graduate deep RL course. Levine's group (RAIL lab) produced much of the robot learning literature. Covers imitation learning, policy gradients, Q-learning, model-based RL, offline RL, exploration, inverse RL, and sequence models.

- **Course site (current):** [rail.eecs.berkeley.edu/deeprlcourse](https://rail.eecs.berkeley.edu/deeprlcourse/)
- **Fall 2023 site (best self-study version):** [rail.eecs.berkeley.edu/deeprlcourse-fa23](https://rail.eecs.berkeley.edu/deeprlcourse-fa23/)
- **YouTube (Fall 2023):** [CS285 Fall 2023 playlist](https://www.youtube.com/playlist?list=PL_iWQOsE6TfVYGEGiAOMaOzzv41Jfm_Ps)
- **Syllabus:** [rail.eecs.berkeley.edu/deeprlcourse-fa23/syllabus](https://rail.eecs.berkeley.edu/deeprlcourse-fa23/syllabus/)
- **Community discussion:** [reddit.com/r/berkeleydeeprlcourse](https://reddit.com/r/berkeleydeeprlcourse/)
- **Textbook (companion):** Sutton & Barto, *Reinforcement Learning: An Introduction* — [free online](http://incompleteideas.net/book/the-book-2nd.html)

### Prerequisites

Basic ML (MDPs, neural networks, gradient descent), probability, linear algebra, Python/PyTorch. If you did CS231n, you're set.

### Lectures → Homework Mapping

5 homeworks, each with theory and implementation (MuJoCo environments). Below is the full schedule.

**HW1: Imitation Learning** — do after Lectures 1–3

| # | Lecture | Topics | Slides |
|---|---------|--------|--------|
| 1 | Introduction and Course Overview | What is RL, why deep RL, course structure | [PDF](https://rail.eecs.berkeley.edu/deeprlcourse-fa23/deeprlcourse-fa23/static/slides/lec-1.pdf) |
| 2 | Supervised Learning of Behaviors | Behavioral cloning, DAgger, distribution shift | [PDF](https://rail.eecs.berkeley.edu/deeprlcourse-fa23/deeprlcourse-fa23/static/slides/lec-2.pdf) |
| 3 | PyTorch Tutorial | Practical PyTorch for RL | [PDF](https://rail.eecs.berkeley.edu/deeprlcourse-fa23/deeprlcourse-fa23/static/slides/lec-3.pdf) |

→ **[Homework 1: Imitation Learning](https://rail.eecs.berkeley.edu/deeprlcourse-fa23/deeprlcourse-fa23/static/homeworks/hw1.pdf)** — Behavioral cloning + DAgger

---

**HW2: Policy Gradients** — do after Lectures 4–6

| # | Lecture | Topics | Slides |
|---|---------|--------|--------|
| 4 | Introduction to Reinforcement Learning | MDPs, reward, return, RL objective | [PDF](https://rail.eecs.berkeley.edu/deeprlcourse-fa23/deeprlcourse-fa23/static/slides/lec-4.pdf) |
| 5 | Policy Gradients | REINFORCE, baselines, variance reduction | [PDF](https://rail.eecs.berkeley.edu/deeprlcourse-fa23/deeprlcourse-fa23/static/slides/lec-5.pdf) |
| 6 | Actor-Critic Algorithms | Advantage estimation, GAE, A2C | [PDF](https://rail.eecs.berkeley.edu/deeprlcourse-fa23/deeprlcourse-fa23/static/slides/lec-6.pdf) |

→ **[Homework 2: Policy Gradients](https://rail.eecs.berkeley.edu/deeprlcourse-fa23/deeprlcourse-fa23/static/homeworks/hw2.pdf)** — REINFORCE, baselines, GAE

---

**HW3: Q-Learning and Actor-Critic** — do after Lectures 7–10

| # | Lecture | Topics | Slides |
|---|---------|--------|--------|
| 7 | Value Function Methods | Fitted value iteration, convergence | [PDF](https://rail.eecs.berkeley.edu/deeprlcourse-fa23/deeprlcourse-fa23/static/slides/lec-7.pdf) |
| 8 | Deep RL with Q-Functions | DQN, double Q-learning, SAC | [PDF](https://rail.eecs.berkeley.edu/deeprlcourse-fa23/deeprlcourse-fa23/static/slides/lec-8.pdf) |
| 9 | Advanced Policy Gradients | Natural gradients, TRPO, PPO | [PDF](https://rail.eecs.berkeley.edu/deeprlcourse-fa23/deeprlcourse-fa23/static/slides/lec-9.pdf) |
| 10 | Optimal Control and Planning | LQR, iLQR, MPC, random shooting, CEM | [PDF](https://rail.eecs.berkeley.edu/deeprlcourse-fa23/deeprlcourse-fa23/static/slides/lec-10.pdf) |

→ **[Homework 3: Q-Learning and Actor-Critic](https://rail.eecs.berkeley.edu/deeprlcourse-fa23/deeprlcourse-fa23/static/homeworks/hw3.pdf)** — DQN, DDQN, Actor-Critic, SAC

---

**HW4: Model-Based RL** — do after Lectures 11–12

| # | Lecture | Topics | Slides |
|---|---------|--------|--------|
| 11 | Model-Based Reinforcement Learning | Learning dynamics models, planning with learned models | [PDF](https://rail.eecs.berkeley.edu/deeprlcourse-fa23/deeprlcourse-fa23/static/slides/lec-11.pdf) |
| 12 | Model-Based Policy Learning | Dyna, model-based policy optimization, world models | [PDF](https://rail.eecs.berkeley.edu/deeprlcourse-fa23/deeprlcourse-fa23/static/slides/lec-12.pdf) |

→ **[Homework 4: Model-Based RL](https://rail.eecs.berkeley.edu/deeprlcourse-fa23/deeprlcourse-fa23/static/homeworks/hw4.pdf)**

---

**HW5: Exploration and Offline RL** — do after Lectures 13–16

| # | Lecture | Topics | Slides |
|---|---------|--------|--------|
| 13 | Exploration (Part 1) | Count-based, curiosity-driven, information gain | [PDF](https://rail.eecs.berkeley.edu/deeprlcourse-fa23/deeprlcourse-fa23/static/slides/lec-13.pdf) |
| 14 | Exploration (Part 2) | Posterior sampling, unsupervised RL | [PDF](https://rail.eecs.berkeley.edu/deeprlcourse-fa23/deeprlcourse-fa23/static/slides/lec-14.pdf) |
| 15 | Offline RL (Part 1) | Batch RL, distribution shift in offline setting, CQL | [PDF](https://rail.eecs.berkeley.edu/deeprlcourse-fa23/deeprlcourse-fa23/static/slides/lec-15.pdf) |
| 16 | Offline RL (Part 2) | IQL, decision transformers, offline-to-online | [PDF](https://rail.eecs.berkeley.edu/deeprlcourse-fa23/deeprlcourse-fa23/static/slides/lec-16.pdf) |

→ **[Homework 5: Exploration and Offline RL](https://rail.eecs.berkeley.edu/deeprlcourse-fa23/deeprlcourse-fa23/static/homeworks/hw5.pdf)**

---

**Remaining lectures (no homework — watch for depth)**

| # | Lecture | Topics | Slides |
|---|---------|--------|--------|
| 17 | RL Theory Basics | Sample complexity, PAC bounds | [PDF](https://rail.eecs.berkeley.edu/deeprlcourse-fa23/deeprlcourse-fa23/static/slides/lec-17.pdf) |
| 18 | Variational Inference and Generative Models | VAEs, flow models, connection to RL | [PDF](https://rail.eecs.berkeley.edu/deeprlcourse-fa23/deeprlcourse-fa23/static/slides/lec-18.pdf) |
| 19 | Connection between Inference and Control | Control as inference, MaxEnt RL, soft optimality | [PDF](https://rail.eecs.berkeley.edu/deeprlcourse-fa23/deeprlcourse-fa23/static/slides/lec-19.pdf) |
| 20 | Inverse Reinforcement Learning | Learning reward functions from demonstrations | [PDF](https://rail.eecs.berkeley.edu/deeprlcourse-fa23/deeprlcourse-fa23/static/slides/lec-20.pdf) |
| 21 | RL with Sequence Models | Decision transformers, trajectory transformers | [PDF](https://rail.eecs.berkeley.edu/deeprlcourse-fa23/deeprlcourse-fa23/static/slides/lec-21.pdf) |
| 22 | Meta-Learning and Transfer Learning | MAML, few-shot adaptation, transfer | [PDF](https://rail.eecs.berkeley.edu/deeprlcourse-fa23/deeprlcourse-fa23/static/slides/lec-22.pdf) |
| 23 | Challenges and Open Problems | Frontiers of deep RL | [PDF](https://rail.eecs.berkeley.edu/deeprlcourse-fa23/deeprlcourse-fa23/static/slides/lec-23.pdf) |

> **For your cloth project:** Lectures 2 (imitation/behavioral cloning), 15–16 (offline RL), 18–19 (generative models / inference-as-control), and 21 (sequence models / decision transformers) are the most directly relevant. Diffusion Policy and VLA models build on exactly these ideas.

---

## Stanford CS224R: Deep Reinforcement Learning (Chelsea Finn, Spring 2025)

Complementary to CS285. More focused on the practical robot-learning stack: learning from demonstrations, learning from high-dimensional observations, offline datasets, goal-conditioned RL, meta-RL. Finn co-founded Physical Intelligence (π0).

- **Course site:** [cs224r.stanford.edu](https://cs224r.stanford.edu/)
- **YouTube playlist (Spring 2025):** [CS224R Spring 2025](https://www.youtube.com/playlist?list=PLoROMvodv4rPwxE0ONYRa_itZFdaKCylL)
- **Stanford Bulletin description:** [bulletin.stanford.edu/courses/2242591](https://bulletin.stanford.edu/courses/2242591)

### Structure

3 homeworks + midterm + project. Lectures cover:

- Imitation learning and behavioral cloning
- Policy gradient methods (REINFORCE, PPO)
- Off-policy actor-critic (SAC)
- Model-based RL
- Offline RL
- Goal-conditioned RL
- Meta-RL and multi-task RL
- Unsupervised skill discovery
- RL from human feedback (RLHF)
- Frontiers (VLAs, foundation models for robotics)

### How CS224R differs from CS285

CS285 is broader and more theoretical — it covers the full RL algorithm landscape. CS224R is more applied and robot-focused — it centers on the paradigms you'd actually use to get a policy onto hardware (behavior cloning, diffusion policies, VLA fine-tuning, offline RL from demonstrations). If you can only do one, do CS285 first for the foundations. If you can do both, CS224R second.

---

## Hugging Face LeRobot: Robot Learning Tutorial

The fastest bridge from "took CS285" to "trained a policy on a real arm." Comprehensive guide aimed at researchers and practitioners.

- **Full tutorial (PDF/interactive):** [huggingface.co/spaces/lerobot/robot-learning-tutorial](https://huggingface.co/spaces/lerobot/robot-learning-tutorial)
- **Course (simplified, unit-based):** [huggingface.co/learn/robotics-course](https://huggingface.co/learn/robotics-course/en/unit0/1)
- **LeRobot repo:** [github.com/huggingface/lerobot](https://github.com/huggingface/lerobot)
- **T-shirt folding experiment:** referenced in the LeRobot repo — an end-to-end demonstration of folding t-shirts

### What LeRobot covers

- Classical robotics foundations vs learning-based approaches
- LeRobotDataset format (synchronized video + state/action in Parquet)
- Imitation learning, reinforcement learning, and VLA models — all implemented in pure PyTorch
- Deployment on real hardware (SO-100/SO-101, ALOHA/ALOHA-2)
- Thousands of community robotics datasets on Hugging Face Hub

### Supported policies

LeRobot implements state-of-the-art policies including ACT, Diffusion Policy, TDMPC, VQ-BeT, and Pi0 — the exact algorithms you'll need for cloth manipulation.

### Hardware it supports

| Robot | Cost | Type |
|-------|------|------|
| SO-100 / SO-101 | ~$150–300 | 3D-printable single arm |
| ALOHA / ALOHA-2 | ~$10k+ | Bimanual teleoperation system |

### How to use it

1. Read the full tutorial PDF (not the simplified course) after completing CS285
2. Install LeRobot, load a dataset, visualize episodes
3. Train a Diffusion Policy or ACT on a sim environment
4. If you have an SO-101: teleoperate, record demonstrations, train, deploy
5. Iterate toward your cloth task

---

## NVIDIA Physical AI Learning (do alongside, not sequential)

Short modules, not full courses. Treat as documentation-with-exercises.

- **All modules:** [docs.nvidia.com/learning/physical-ai](https://docs.nvidia.com/learning/physical-ai/)

| Module | Time | What you get |
|--------|------|--------------|
| Building Your First Robot in Isaac Sim | 2–3 hrs | Isaac Sim interface, physics, sensors, first simulation |
| Isaac Lab: RL Training | 3–4 hrs | GPU-accelerated parallel RL, policy training |
| SO-101 Sim-to-Real with GR00T | 6–10 hrs | Configure robot, teleoperate demos, post-train GR00T policy, deploy to real hardware, close sim-to-real gap |
| GR00T Humanoid Manipulation | 4–12 hrs | GR00T reference workflow, Isaac Lab-Arena, Jetson Thor |

> The SO-101 sim-to-real module is the most relevant. It's literally your pipeline minus the cloth.

---

## Suggested sequencing

```
Weeks 1–3:  CS285 Lectures 1–8 + HW1–HW2
            (imitation learning, policy gradients, actor-critic, Q-learning)

Weeks 4–5:  CS285 Lectures 9–12 + HW3–HW4
            (advanced PG, model-based RL)
            Start NVIDIA Isaac Sim basics module alongside

Weeks 6–7:  CS285 Lectures 13–16 + HW5
            (exploration, offline RL)
            Start CS224R playlist

Weeks 8–9:  CS285 Lectures 17–23 (no HW, watch for depth)
            Continue CS224R
            Read LeRobot tutorial PDF

Week 10+:   LeRobot hands-on with SO-101 hardware
            NVIDIA SO-101 sim-to-real module
            → Transition to papers (see Roadmap)
```

This is 10 weeks at ~15–20 hrs/week, overlapping with the Robotics Core stage.
