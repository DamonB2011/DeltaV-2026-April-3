# DeltaV-2026-April-5 (The links to this project is DeltaV_MegaFile.zip and deltav-kinematics.skill)

Note: The live demo link is currently inactive to minimize cloud hosting and domain costs. This repository serves as the complete source code archive and documents my personal coding journey. The ZIP archive contains the full source code used to build the website, while the .skill file preserves the Agent State. This file captures the AI's learned context and logic, essentially allowing me (or you) to "download" its consciousness and development history from any session and paste it into the AI whenever I'd like to use it for something akin to this project.

Hi GitHub, this is my first project on this website. I am a student developer exploring the intersection of physics and code. With the help of AI-accelerated workflows(Manus.AI), this is my first tool that can solve real-world engineering problems. The point of this mini-project was to help me explore Applied Mathematics and learn code and I plan to make more websites in the future.

# DeltaV: AI-Powered Kinematics Engine

### Project Status: Archived
Note: The live website is currently offline to save on cloud hosting costs. This repository contains the complete source code, which you can download and run locally on your own computer.

---

### About the Project
Hi! I am a Grade 9 student, and DeltaV is my first full-stack engineering project. I wanted to build a tool that could take a regular video of a physics experiment (like a ball throw) and automatically turn it into accurate graphs, replacing the need for manual stopwatches and rulers.

### The Physics and Math
The biggest challenge was making the data accurate despite shaky hands or low-quality video. Here is the math I implemented to solve that:

*   Computer Vision: I used OpenCV to track objects. Instead of just looking for color, I used algorithms (CSRT/MOG2) that can follow the object's center of mass.
*   Smoothing the Data: Raw video data is really noisy. I applied a Savitzky-Golay filter to smooth out the jitters so the acceleration graphs look clean and realistic.
*   Calculus: The code performs Numerical Differentiation to calculate exactly how fast the object is moving (velocity) and accelerating frame-by-frame.
*   Calibration: I built a "Pixels-to-Meters" feature so the output is in real-world units, not just pixels.

### Tech Stack
*   Engine: Python (NumPy, SciPy for the math)
*   Frontend: React 19 and Tailwind 4 (for the UI)
*   Backend: TypeScript and MySQL
*   Visualization: Plotly.js (for the synchronized charts)

### How I Built It
Since this was my first deep dive into full-stack development, I used an AI-assisted workflow (Manus.AI) to help me architect the system. This process taught me how to connect a Python math engine to a modern web interface and how to handle complex database issues like asynchronous processing.

# VEX V5RC May 7th 2026: Override Concept Bot By Team 1509R 🤖

[![Game Mode: Override](https://shields.io)](https://vexrobotics.com)
[![Platform: V5](https://shields.io)]()
[![Status: Concept/WIP (Work in Progress)]([https://shields.io)](https://cad.onshape.com/documents/1adbd9bc1c73c2427d1771a0/w/e842d6b7500cc3935959ca32/e/5a69c71ebb3461d94fe6e010))]()

A high-performance, symmetrical robot design for the 2026 VEX Robotics Competition season. This project focuses on vertical dominance via a mirrored DR4B lift and a multi-modal intake system.

---

## 🛠 Project Structure & CAD Studios

The design is modularized across several specialized Part Studios to ensure precision spacing and structural symmetry.

### 🏎️ Drivetrain (DT)
*   **Studio: `Mirrored DT` / `DT`**
    *   **Frame:** Fully symmetrical C-channel chassis for balanced weight distribution.
    *   **Wheel Configuration:** Hybrid drive utilizing **Traction Wheels** (defense/stability) and **Omni Wheels** (agility).
    *   **Gearing:** Optimized **36:60 Gear Ratio** for a competitive balance between torque and traversal speed.
    *   **Hardware:** Integrated **36t Shafts** with documented `Shaft Disassembled` views for maintenance.

### 🏗️ Lift System (DR4B)
*   **Studio: `Modified DR4B 1509R` / `Mirrored DR4B`**
    *   **Architecture:** Double Reverse Four-Bar based on the high-efficiency 1509R linkage.
    *   **Interactivity:** Developed using the `DR4B Interactive` studio to ensure a 100% linear vertical travel path.
    *   **Evolution:** Iterated from `Basic DR4B` prototypes to a final `Mirrored Side` assembly to eliminate lateral sway.

### 🏗️ Manipulator & Intake
*   **Studio: `Claw Concept` / `Roller`**
    *   **Multi-Axis Grip:** Features both **Front/Back** and **Left/Right** claw designs to handle Pins and Cups from any orientation.
    *   **Active Intake:** High-speed **Roller** system for "Touch It, Own It" game element acquisition.
    *   **Symmetry:** Fully `Mirrored Claw` assembly to maximize motor efficiency and gripping force.

---

## 📐 Engineering Optimization
This repository emphasizes precision tolerances and clearance management:

-   **`Part Studio 1`**: Central hub for final assembly and global variable management.
-   **`Spacing`**: Dedicated studio for interference checking between the DR4B arms and the internal drivetrain components.
-   **`Assembly 1`**: Final top-level assembly for motion testing and center-of-mass analysis.

## 🚀 Strategic Goals
1.  **Midfield Dominance:** Use high-traction wheels and 36:60 gearing to control the central zones.
2.  **High-Tier Stacking:** Utilize the linear DR4B reach to efficiently score on the highest goals.
3.  **Vision Alignment:** Symmetrical chassis design optimized for AI Vision Sensor mounting and AprilTag tracking.

---

## 📝 License
This design is intended for the VRC community. Please credit 1509R if you use elements of this DR4B or Claw geometry.
