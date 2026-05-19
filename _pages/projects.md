---
layout: archive
title: "Projects"
permalink: /projects/
author_profile: true
---

{% include base_path %}

## Research Projects

**MapForest: A Modular Field Robotics System for Forest Mapping and Invasive Species Localization** &nbsp; *(Sep 2024 – Present)*
*MS Thesis — Carnegie Mellon University, Kantor Lab*

Monitoring invasive tree species across large forests is challenging due to limited accessibility, manual scouting reliance, and degraded under-canopy GNSS. MapForest is a modular field robotics system that transforms multi-modal sensor data (LiDAR, IMU, GNSS, RGB) into GIS-ready invasive-species maps. The system features a compact, platform-agnostic sensing payload deployable on UAV, bicycle, or backpack platforms. The software pipeline combines LiDAR–inertial SLAM (GLIM with covariance-aware GNSS factors and robust loss kernels) with a YOLOv8-based Tree-of-Heaven (*Ailanthus altissima*) detector, fusing detections into georeferenced GeoTIFF layers for downstream GIS analysis. Evaluated across six sites spanning urban, park, trail, and forest environments: trajectory deviation error of 1.95 m over a 1.2 km forest traversal, Tree-of-Heaven detection F1 of 0.77. Datasets and tooling are publicly released. \
*Authors: Sandeep S. Zachariah, Francisco Yandun, Sachet Korada, Abhisesh Silwal* \
[[arXiv]](https://arxiv.org/abs/2603.22502) &nbsp; [[Website]](https://kantor-lab.github.io/forestslam/)

---

**Dense Forest Under-Canopy and Above-Canopy Map Merging** &nbsp; *(May 2025 – Present)*
*MS Thesis — Carnegie Mellon University, Kantor Lab*

Foliage occlusions prevent complete 3D reconstruction of dense forest environments from any single viewpoint. This work develops a method to align under-canopy (terrestrial LiDAR/mobile) and above-canopy (UAV/aerial) maps by maximizing mutual information in a shared latent space of tree-likelihood fields inferred from each map. The approach targets dense broadleaf forests where viewpoint-induced appearance differences make correspondence-driven registration unreliable.

---

**Fire Blight Detection in Apple Orchards** &nbsp; *(Jan 2025 – May 2025)*
*Field Robotics Course Project — Carnegie Mellon University*

Erwin is a fully autonomous robotic inspection system for detecting and mapping fire blight (*Erwinia amylovora*) in high-density apple orchards during dormant season. The system uses an Amiga mobile base with a 6-DOF xArm manipulator and custom stereo vision sensors. I led **system integration and navigation**, implementing the mission control software as a behaviour tree in ROS2 to orchestrate navigation (RTK-GNSS waypoint following, obstacle avoidance), disease detection (stereo-vision semantic point cloud pipeline), manipulation (collision-free arm trajectories for full-tree coverage), and spray marking of infected trees. Simulation was performed in NVIDIA Isaac Sim. The Foxglove-based UI provides a georeferenced orchard map with infected trees overlaid in real time. Field-tested at Penn State Fruit Research and Extension Center. \
*Team: Jack Nelson, Daniya Nussipbek, Sarthak Jain, Hayden Feddock, Sandeep S. Zachariah, Yi Wu*

---

**Leveraging Large Language Models for Robotic Systems** &nbsp; *(May 2023 – June 2024)*
*Indian Institute of Technology Delhi*

Current robotic systems are limited to interaction with a predefined set of objects. This project leveraged the zero-shot generalization capabilities of LLMs and VLMs — trained on internet-scale data — to create a holistic robotic system encompassing open-world perception, task planning, and low-level behaviors. Developed an open-world scene graph representation that admits local updates as the scene evolves, achieving superior performance on open-world object detection and relation extraction compared to prior methods. \
[[Paper]](https://openreview.net/pdf?id=IqRpVnq6mC) &nbsp; [[Website]](https://reail-iitdelhi.github.io/scenegraph.github.io/)

---

**Task Planning under Uncertainty for Language-Guided Mobile Manipulator** &nbsp; *(July 2022 – August 2023)*
*Indian Institute of Technology Delhi*

A robot working alongside a human must comprehend natural language instructions, perceive the environment, and generate action sequences in uncertain, partially observable outdoor settings. Our system monitors execution of low-level actions and replans on any discrepancy between expected and perceived state. For partial observability, the planner spawns contextually grounded exploratory behaviors, achieving a Goal Reaching Rate (GRR) of 90%. \
[[Video]](https://youtu.be/sB60bjTd4go) &nbsp; [[Manuscript]](https://drive.google.com/file/d/1gtn0kY44iUEqSBu9fpOs9r2zEnOT0c26/view?usp=drive_link)

---

**Underwater Image Enhancement** &nbsp; *(July 2021 – April 2022)*
*Undergraduate Thesis — NIT Calicut*

Developed a novel wavelet-fusion method combining Multiscale Retinex and Dark Channel Prior (DCP) with custom color balancing algorithms for underwater image enhancement. The method outperformed both naive approaches and learning-based methods (U-Net, CycleGAN) on quantitative and qualitative metrics. Superiority was demonstrated through improved accuracy in underwater object detection. \
[[Thesis]](https://drive.google.com/file/d/1ADiXYufhGzuSJF_GerbJmMzHQ3YGhuF3/view?usp=sharing)

---

**Modelling, Control, and Simulation of Quadruped Robots** &nbsp; *(April 2021 – September 2021)*
*Project Intern — IIST*

Kinematic and dynamic modelling of a quadruped robot using Composite Rigid Body and Recursive Newton-Euler algorithms. Implemented closed-loop inverse kinematics (CLIK) for 6D pose control of torso and foot frames. Joint-space and task-space inverse dynamics control, incorporating holonomic and non-holonomic constraints, contact impact dynamics, and constraint drift compensation, all simulated in MATLAB. \
[[Video 1]](https://youtu.be/GAu-791Tc70) &nbsp; [[Video 2]](https://youtu.be/n5TkmluuKZQ) &nbsp; [[Report]](https://drive.google.com/file/d/1k0NgwT7gTCXW-6YHrqzsvzMsZ65F2Xzy/view?usp=drive_link)

---

**Modelling, Control, and Simulation of a Planar Robotic Manipulator** &nbsp; *(May 2019 – July 2019)*
*Summer Intern — IIST*

Joint-space and task-space kinematic and dynamic analysis of a 2R manipulator via Euler-Lagrange equations. CAD model created in SolidWorks; mass-inertia properties fed into MATLAB/SIMULINK control design. Structural dynamic analysis in ANSYS to verify absence of control-structure interaction. \
[[Report]](https://drive.google.com/file/d/1jaEdBx1TYZqzEl0E7jba9-ifKCAvCTJq/view?usp=drive_link)

---

## Course Projects

**WanPolicy: Representation Alignment for Robust and Efficient World-Action Models** &nbsp; *(Jan 2026 – Present)*
*Carnegie Mellon University — NeurIPS 2026 Submission*

World-Action Models (WAMs) repurpose pretrained video diffusion backbones for robot manipulation by jointly modeling future observations and actions. WanPolicy challenges the dominant pixel-level reconstruction paradigm, replacing the diffusion objective with a representation alignment loss that supervises intermediate DiT features using a frozen DINOv3 encoder. Fine-tuning the DiT as a regressor eliminates iterative denoising at inference — a single forward pass suffices, yielding significant speedups. On LIBERO-Plus (environmental perturbations), WanPolicy achieves 80% success vs. the prior art of 69%, while training on substantially less robot data than competing methods.

---

**Semantic Simultaneous Localization and Mapping** &nbsp; *(Jan 2025 – Apr 2025)*
*Carnegie Mellon University*

Collected a semantic SLAM benchmark on the CMU campus using a custom sensor suite (LiDAR, camera, IMU, GNSS). Evaluated state-of-the-art semantic SLAM systems — Kimera, SegMap, and SlideSLAM — on the benchmark, analysing metric and semantic accuracy across diverse campus environments.

---

**Diffusion Policy and Flow Matching for Long-Horizon Manipulation** &nbsp; *(Aug 2025 – Dec 2025)*
*16-831: Introduction to Robot Learning — Carnegie Mellon University*

Unified evaluation of diffusion-based and flow-matching action-sequence policies on the RoboMimic benchmark, with direct comparison to BC baselines. Diffusion policies model multimodal action distributions via conditional denoising; flow matching learns deterministic continuous-time transports enabling efficient single-step sampling. Targeted ablations on goal conditioning and observation horizon length isolated which design choices drive performance. Results showed diffusion policies achieve state-of-the-art on long-horizon manipulation, while flow matching provides a competitive and faster alternative.

---

## Other Projects

**Brain Tumor Classification using ResNet** &nbsp; *(January 2021 – April 2021)*

Implementation and benchmarking of ResNet on TensorFlow for brain tumour scan classification. Evaluated multiple performance strategies (identity shortcut connections, batch normalization tuning) and deployed on a medical imaging dataset.

---

**3-Band Audio Equalizer** &nbsp; *(March 2020 – May 2020)*

Op-amp-based audio equalizer with independent gain control for Bass, Mid, and Treble bands, plus distortion detection and master gain control. Designed in MATLAB and simulated in Proteus.

---

**Electronic Voting Machine** &nbsp; *(January 2020 – February 2020)*

8051 microcontroller-based EVM with 16×2 LCD display for results and election status. Designed and simulated in Proteus.
