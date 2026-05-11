# DeltaV: AI-Powered Kinematics Engine

> Upload a physics video. Get back motion graphs in real-world units.

![Project Status](https://img.shields.io/badge/status-archived-lightgrey)
![Python](https://img.shields.io/badge/python-3.x-blue)
![React](https://img.shields.io/badge/react-19-61DAFB)
![TypeScript](https://img.shields.io/badge/typescript-backend-3178C6)

---

## What It Does

DeltaV takes a regular video of a physics experiment (a ball throw, a pendulum, a rolling object) and extracts real-world motion data from it automatically. You upload the video, set a calibration reference, and get back synchronized velocity and acceleration graphs in SI units. No stopwatch. No ruler. No manual data entry.

The hard part was not the tracking. Raw video data is noisy and pixel-based, and turning it into clean, accurate physics output required solving both problems separately.

---

## The Physics and Math

**Object Tracking**
OpenCV's CSRT and MOG2 algorithms track the object's center of mass across frames. This is more reliable than color-based detection, which breaks under changing light conditions.

**Noise Reduction**
Raw positional data from video has a lot of jitter. A Savitzky-Golay filter smooths it out while keeping the shape of the motion curve intact. Without this step, the acceleration graphs are unreadable.

**Velocity and Acceleration**
The code runs numerical differentiation on the smoothed data to get instantaneous velocity and acceleration at each frame. Same principle used in real motion-capture pipelines.

**Calibration**
A pixels-to-meters feature lets you set a known reference length in the video. Every output value scales to that reference, so the graphs show meters and meters per second rather than pixels.

---

## Tech Stack

| Layer | Technology |
|-------|-----------|
| Computer Vision and Math | Python, NumPy, SciPy, OpenCV |
| Frontend | React 19, Tailwind CSS 4 |
| Backend | TypeScript, MySQL |
| Visualization | Plotly.js |

---

## Running Locally

The live demo is offline to keep hosting costs down. To run it on your own machine:

```bash
# Clone the repository
git clone https://github.com/DamonB2011/Damon-Project_1/tree/Code-Based-Projects

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

The `.skill` file is a saved AI agent state. It stores the full context and logic from the AI assistant used during this project. Pasting it into a new session restores that context so you can pick up exactly where the project left off without re-explaining the architecture.

---

## What I Learned

The interesting problems here were not the math concepts themselves but making them work on real input. Smoothing noisy data, calibrating pixel space to physical units, getting a Python math engine to talk to a React frontend, handling async database writes without dropping frames. Each piece was straightforward in isolation. Getting them to work together reliably took a lot of iteration.

---

## About

Built by Youbo (Damon) Bao, a student developer at Ridley College interested in applied physics and engineering.
