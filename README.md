# DeltaV-2026-April-5
Note:The live demo link is currently inactive to minimize cloud hosting and domain costs. This repository serves as the complete source code archive and also a way to document my own coding journey.

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
