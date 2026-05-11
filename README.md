# DeltaV — AI-Powered Kinematics Engine

> Turn any physics video into accurate motion graphs — automatically.

![Project Status](https://img.shields.io/badge/status-archived-lightgrey)
![Python](https://img.shields.io/badge/python-3.x-blue)
![React](https://img.shields.io/badge/react-19-61DAFB)
![TypeScript](https://img.shields.io/badge/typescript-backend-3178C6)

---

## What It Does

DeltaV takes a regular video of a physics experiment — a ball throw, a pendulum, a rolling object — and automatically extracts real-world motion data from it. Instead of manually timing with stopwatches or measuring with rulers, you upload a video and get back synchronized velocity and acceleration graphs in real-world units.

The core problem it solves: **raw video data is noisy and pixel-based.** DeltaV handles both.

---

## The Physics & Math

The engineering challenge was making the output accurate despite shaky footage, low resolution, and inconsistent lighting. Here is how each problem was solved:

**Object Tracking**
Used OpenCV with CSRT and MOG2 algorithms to track an object's center of mass frame-by-frame — more robust than simple color detection, which fails under changing light conditions.

**Noise Reduction**
Raw tracking data contains significant jitter. Applied a Savitzky-Golay filter to smooth the positional data while preserving the shape of the underlying motion curve — critical for producing realistic acceleration graphs.

**Velocity & Acceleration**
Implemented numerical differentiation on the smoothed positional data to calculate instantaneous velocity and acceleration at each frame. This is the same mathematical principle used in real motion-capture systems.

**Real-World Calibration**
Built a pixels-to-meters calibration feature so all output is in SI units rather than raw pixel displacement. The user sets a known reference length in the video and the system scales all measurements accordingly.

---

## Tech Stack

| Layer | Technology |
|-------|-----------|
| Computer Vision & Math Engine | Python — NumPy, SciPy, OpenCV |
| Frontend | React 19, Tailwind CSS 4 |
| Backend | TypeScript, MySQL |
| Data Visualization | Plotly.js (synchronized multi-axis charts) |

---

## Running Locally

The live demo is currently offline to minimize hosting costs. To run DeltaV locally:

```bash
# Clone the repository
git clone https://github.com/yourusername/DeltaV-2026-April-5

# Extract the source archive
unzip DeltaV_MegaFile.zip

# Install Python dependencies
pip install numpy scipy opencv-python

# Install frontend dependencies
cd frontend
npm install

# Start the development server
npm run dev
```

---

## Agent State (.skill file)

The `.skill` file in this repository is a saved AI agent state — it captures the full context, logic, and development history of the AI assistant used during this project. Pasting it into a compatible session restores the exact working context, making it easy to resume or extend the project without re-explaining the architecture from scratch.

---

## What I Learned

Building DeltaV pushed me to connect disciplines I had only studied separately — applying calculus concepts like differentiation to real video data, handling the gap between theoretical physics and messy real-world inputs, and architecting a system where a Python math engine communicates with a modern web frontend. The hardest problem was not the math itself but making the math *robust* — understanding why raw data fails and what signal processing techniques fix it.

---

## About

Built by Youbo (Damon) Bao — a student developer at Ridley College exploring the intersection of applied physics and software engineering.
