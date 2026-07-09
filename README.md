# Learning Roadmap: Robotic Cloth Manipulation

From zero to "can train and deploy a garment-flattening policy on a real arm."
Estimated time: 4–6 months of serious part-time work.

---

## Sequencing

```
CS231n + Zero-to-Hero (parallel)
        │
        ▼
Tedrake (Robotic Manipulation) + CS285 (parallel — one geometric, one learning-based)
        │
        ▼
CS224R + LeRobot tutorial (with hardware in hand)
        │
        ▼
Papers (no courses exist for cloth manipulation — it's research territory)
```

---

## Stage 1 — Foundations

### CS231n: Deep Learning for Computer Vision (Stanford, Spring 2025)

The reference course. Do the assignments, not just the lectures.

- **Course site:** [cs231n.stanford.edu](https://cs231n.stanford.edu/)
- **Notes & assignments:** [cs231n.github.io](https://cs231n.github.io/)
- **YouTube playlist:** [Stanford CS231N Spring 2025](https://www.youtube.com/playlist?list=PLoROMvodv4rOmsNzYBMe0gJY2XS8AQg16)
- **Community 2025 notes:** [github.com/raimbekovm/cs231n-2025-notes](https://github.com/raimbekovm/cs231n-2025-notes)

See the separate [CS231n Study Guide](./CS231n_2025_Study_Guide.md) for the full lecture-to-assignment mapping.

### Karpathy's Neural Networks: Zero to Hero

If your PyTorch is weak, this is denser and faster than any MOOC — you build backprop, then GPT, from scratch. Do this in parallel with CS231n.

- **YouTube playlist:** [Neural Networks: Zero to Hero](https://www.youtube.com/playlist?list=PLAqhIrjkxbuWI23v9cThsA9GvCAUhRvKZ)
- **Repos:** [micrograd](https://github.com/karpathy/micrograd), [makemore](https://github.com/karpathy/makemore), [nanoGPT](https://github.com/karpathy/nanoGPT)

---

## Stage 2 — Robotics Core

### Modern Robotics (Lynch & Park, Northwestern)

Kinematics, dynamics, screw theory, control. Use the textbook + lecture videos directly, skip the Coursera packaging. Chapters 2–6, 8–9 are the core; skip 7, 10, 12 as even Lynch does in class.

- **Textbook (free preprint):** [modernrobotics.northwestern.edu](https://modernrobotics.northwestern.edu/)
- **Wiki + resources:** [hades.mech.northwestern.edu/Modern_Robotics](https://hades.mech.northwestern.edu/index.php/Modern_Robotics)
- **YouTube (all videos):** [Modern Robotics playlist](https://www.youtube.com/playlist?list=PLggLP4f-rq02vX0OQQ5vrCxbJrzamYDfx)
- **Software (Python/MATLAB):** [github.com/NxRLab/ModernRobotics](https://github.com/NxRLab/ModernRobotics)

### MIT 6.4210: Robotic Manipulation (Russ Tedrake)

The single best manipulation course in existence: geometric pose estimation, grasping, motion planning, deep-learning-based manipulation, and it touches deformable objects. Updated every year, full notes online, Colab-based problem sets in Drake. If you take only one robotics course, take this one.

- **Course notes (HTML, updated continuously):** [manipulation.csail.mit.edu](https://manipulation.csail.mit.edu/)
- **Fall 2025 offering:** [manipulation.csail.mit.edu/Fall2025](https://manipulation.csail.mit.edu/Fall2025/)
- **MIT OCW (Fall 2022 version):** [ocw.mit.edu/courses/6-4210](https://ocw.mit.edu/courses/6-4210-robotic-manipulation-fall-2022/)
- **Code / Drake:** [github.com/RussTedrake/manipulation](https://github.com/RussTedrake/manipulation)

### Optional: Underactuated Robotics (Russ Tedrake)

Deeper control theory. For your task it's not strictly required — cloth work is perception/policy-heavy, not control-heavy.

- **Course notes:** [underactuated.csail.mit.edu](https://underactuated.csail.mit.edu/)

---

## Stage 3 — Robot Learning / RL

### Berkeley CS285: Deep Reinforcement Learning (Sergey Levine)

The canonical graduate deep RL course. Levine's group produced much of the robot learning literature you'll be reading. Covers imitation learning, model-based RL, offline RL — all directly relevant.

- **Course site:** [rail.eecs.berkeley.edu/deeprlcourse](https://rail.eecs.berkeley.edu/deeprlcourse/)
- **YouTube (Fall 2023, most developed version):** [CS285 Fall 2023 playlist](https://www.youtube.com/playlist?list=PL_iWQOsE6TfVYGEGiAOMaOzzv41Jfm_Ps)
- **YouTube (Fall 2020, online-friendly format):** [CS285 Fall 2020 playlist](https://www.youtube.com/playlist?list=PL_iWQOsE6TfURIIhCrlt-wj9ByIVpbfGc)

### Stanford CS224R: Deep Reinforcement Learning (Chelsea Finn, Spring 2025)

Complementary to CS285, more focused on the practical robot-learning stack: learning behavior from high-dimensional observations, learning from demonstrations — exactly the paradigm (behavior cloning, diffusion policies, VLA fine-tuning) you'll use. Finn co-founded Physical Intelligence (π0), so the material tracks the current frontier.

- **Course site:** [cs224r.stanford.edu](https://cs224r.stanford.edu/)
- **YouTube playlist:** [CS224R Spring 2025](https://www.youtube.com/playlist?list=PLoROMvodv4rPwxE0ONYRa_itZFdaKCylL)

### LeRobot Robot Learning Tutorial (Hugging Face)

Read the full tutorial PDF, not the simplified course version. Comprehensive guide to robot learning aimed at researchers and practitioners. Fastest bridge from "took CS285" to "trained a policy on a real arm." LeRobot even has a published t-shirt folding experiment.

- **Full tutorial:** [huggingface.co/spaces/lerobot/robot-learning-tutorial](https://huggingface.co/spaces/lerobot/robot-learning-tutorial)
- **Course (simplified):** [huggingface.co/learn/robotics-course](https://huggingface.co/learn/robotics-course/en/unit0/1)
- **LeRobot repo:** [github.com/huggingface/lerobot](https://github.com/huggingface/lerobot)

---

## Stage 4 — Tooling (short, do alongside Stages 2–3)

### NVIDIA Isaac Sim / Isaac Lab

Treat as documentation-with-exercises, not a course. The directly relevant modules:

- **Building Your First Robot in Isaac Sim** (beginner, 2–3 hrs)
- **Isaac Lab: RL training** (intermediate, 3–4 hrs)
- **SO-101 sim-to-real with GR00T** (intermediate, 6–10 hrs) — configure, calibrate, demonstrate, post-train a GR00T policy for pick-and-place, deploy to real hardware
- **All modules:** [docs.nvidia.com/learning/physical-ai](https://docs.nvidia.com/learning/physical-ai/)

### ROS 2

Don't take a course. Read the official docs and build something. If you use LeRobot end-to-end you can defer ROS almost indefinitely.

- **Official docs:** [docs.ros.org](https://docs.ros.org/)

---

## Stage 5 — Papers, Not Courses

Once through CS285/CS224R + Tedrake, the cloth-specific knowledge lives in ~15 papers. Reading them will be straightforward at that point.

| Paper | What it covers |
|-------|---------------|
| FlingBot (Ha & Song, 2021) | Dynamic fling actions for cloth unfolding |
| SpeedFolding (Avigal et al., 2022) | Bimanual high-speed garment folding |
| Cloth Funnels (Canberk et al., 2022) | Canonicalized alignment for multi-purpose garment manipulation |
| FabricFlowNet (Weng et al., 2022) | Bimanual cloth manipulation with flow-based policy |
| Diffusion Policy (Chi et al., 2023) | Visuomotor policy learning via action diffusion |
| GPT-Fabric (2024) | Foundation models for fabric smoothing and folding |
| APS-Net (2025) | Dual-arm unfolding + standardization for ironing/folding |
| GarmentLab (2024) | Isaac Sim-based garment simulation benchmark, 20 tasks |
| DexGarmentLab (2025) | Dexterous hand garment manipulation in Isaac Sim |
| π0 / Physical Intelligence | Vision-language-action model for general manipulation |
| ICRA Cloth Competition Report (2024) | Dissects a competition-winning unfolding system |
| SimWeaver (2025) | Zero-shot RGB sim-to-real for deformable manipulation |
| RGBench (2025) | Benchmark for measuring sim-to-real gap in garment tasks |

---

## Hardware (buy around Stage 3)

Both the HF LeRobot course and NVIDIA's sim-to-real course use the SO-101 arm. Get one early — hands-on beats theory.

- **SO-101 arm:** ~$150–300, 3D-printable
- **Camera:** Intel RealSense D435 or ZED Mini (RGB-D)
- **Later upgrade:** UR5e or xArm for serious work, ideally two arms (bimanual)
