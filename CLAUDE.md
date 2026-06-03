# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Build

Compile the resume PDF from source:

```bash
pdflatex Vaibhav_Resume.tex
```

For a clean build (resolves cross-reference issues):

```bash
pdflatex Vaibhav_Resume.tex && pdflatex Vaibhav_Resume.tex
```

Clean up LaTeX artifacts:

```bash
rm -f *.aux *.log *.out
```

## Structure

Single-file LaTeX resume. All content lives in `Vaibhav_Resume.tex`; compiled output is `Vaibhav_Resume.pdf`. The `Old/` folder contains historical versions — do not modify those files.

**Custom commands defined in the preamble:**
- `\workheader{Company}{Title}{Date | Location}` — renders a job entry header
- `\projheader{Project Name}{Tech Stack | Year}` — renders a project entry header

**Section order:** Professional Summary → Work Experience → Skills → Projects → Education → Publications

## Formatting conventions

- Font: Lato 9pt on A4 with 10mm margins
- Line spread: 0.83 (tight — critical for fitting on one page)
- Section titles use `\section{}` which auto-uppercases and adds a rule beneath
- Bullet lists use `[leftmargin=1.2em, topsep=2pt, itemsep=0pt, parsep=0pt]` for tight spacing
- `nameblue` color: RGB 31, 73, 125 (used for name in header)
- Always verify the compiled PDF is 1 page after any content changes

## Git conventions

- Branch: `main` is the only branch
- `.gitignore` excludes `*.ini` files
- Commit style is short and descriptive: `"edit"`, `"Edits"`, `"Fix links and tighten spacing"`

## User profile

**Name:** Vaibhav Raheja
**Personal email:** vaibhavvraheja@gmail.com | **Work email:** vaibhav@terra-wise.com
**Phone:** +1 (217) 202-9970 | **Location:** San Francisco, CA
**LinkedIn:** linkedin.com/in/vaibhav-raheja | **GitHub:** github.com/Vaibhav-Raheja | **Portfolio:** vaibhav-raheja.github.io

### Current role
Founding Engineer, TerraWise Solutions, Inc (Mar 2026 – Present, San Francisco, CA)
Building autonomous robotics stack from scratch — NVIDIA Jetson platform bring-up, ODrive CAN bus motor controllers, ROS2 architecture, Docker deployment, LiDAR-based obstacle detection.

### Previous roles
- **Robotics Engineer / Project Lead, EarthSense, Inc** (Aug 2024 – Mar 2026, Champaign, IL)
  - Led 8-person Solarbot team for autonomous solar panel inspection across 3+ multi-site robot units
  - Redesigned C++ motion controller safety state machine (zero-radius turn detection, RPM ramp up/down, full-stop intermediary)
  - Shipped 35+ PRs across Python/C++ stack: motor control, telemetry, camera bringup, Jetson platform deployment
  - Built Hardware-in-the-Loop (HIL) rig comprising onboard compute, router, wheels, and full sensor suite
  - Built teleop system using AWS Kinesis WebRTC (UDP video) + WebSocket over TCP for command/control
  - Integrated Hesai/Unitree LiDAR, PTZ cameras, Seek thermal, RealSense into production via ROS2 and Docker
  - Field deployments in 43–46°C solar farm conditions

- **Robotics Research Developer, UIUC Intelligent Motion Lab** (Aug–Dec 2023, Champaign, IL)
  - Sub-2mm tracking accuracy for autonomous robotic eye examinations using MediaPipe FaceMesh + ZED on UR5
  - Custom camera mount in Fusion 360, 20% improvement in head tracking precision

- **Robotics Research Developer, AIIMS / NMIMS** (Feb 2021 – May 2023, Mumbai, India)
  - Robot-assisted intubation system on xArm5 with HOTAS teleoperation
  - Custom catheter end-effector with integrated miniature camera

### Education
- MEng Autonomy and Robotics, University of Illinois Urbana-Champaign (Aug 2023 – Dec 2024)
- BTech Computer Engineering, MPSTME Mumbai (Jul 2019 – Jun 2023)

### Skills
- **Programming:** Python, C++, ROS/ROS2, OpenCV, PyTorch, ML, CNNs
- **Robotics & Perception:** LiDAR Integration (Hesai), Multi-Sensor Fusion, Camera Calibration, Path Planning, Motion Planning, Control Algorithms, Reinforcement Learning, Gazebo, SLAM, Docker
- **Networking & Protocols:** TCP/IP, UDP, WebSocket, WebRTC, CAN, Serial Communication
- **Tools:** Linux, Git, Fusion 360, CAD, Arduino, Raspberry Pi, 3D Printing

### Projects
- **Unitree Go1 Benchmarking** (2024) — ISAAC Sim framework comparing factory vs RL-based locomotion; deployed "Walk These Ways" on physical Go1
- **GRAIC Autonomous Racing** (2023) — 40.8% lap time improvement on Shanghai circuit using Hybrid A* planner + PD controller
- **IGVC Team DARVIN** (2019–2023) — Co-Captain; 2nd Cyber Challenge (2023), 3rd Auto-Nav (2022); built SOCRATES 2.0 on ROS with Velodyne LiDAR, OpenCV, GPS, ODrive

### Publications
V. Raheja, V. Shah, M. Shetty, and P. Patel, "Multi-Disease Prediction System using Machine Learning," INCOFT 2022. DOI: 10.1109/INCOFT55651.2022.10094382
