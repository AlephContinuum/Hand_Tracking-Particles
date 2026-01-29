# 🖐️ Gesture-Controlled 3D Particle System

![Status](https://img.shields.io/badge/Status-Active-success)
![Tech](https://img.shields.io/badge/Three.js-WebGL-black)
![Tech](https://img.shields.io/badge/MediaPipe-Computer_Vision-blue)

A real-time, interactive 3D visualization that uses computer vision to track hand movements. This system maps hand gestures to particle physics, allowing users to rotate, expand, and morph 3D shapes using only their webcam.

## 🚀 Overview

This project integrates **Three.js** for high-performance 3D rendering with **Google MediaPipe** for robust hand tracking. It runs entirely in the browser but requires a local server to handle module security policies (CORS).

### Key Features
* **Real-time Hand Tracking:** Detects hand position, pinch gestures, and finger spread with low latency.
* **Dynamic Shape Morphing:** Seamlessly transitions between mathematical shapes:
    * 🌐 Sphere
    * ❤️ Parametric Heart
    * 🪐 Saturn (Planetary Ring)
    * 🌸 3D Flower
* **Interactive Physics:**
    * **Rotation:** Move your hand left/right/up/down to rotate the scene.
    * **Expansion:** Spread your fingers (or release a pinch) to explode the particles outward.
    * **Shape Switching:** Perform a "Pinch" gesture (Index + Thumb) to cycle through shapes.

---

## 🛠️ Technology Stack

* **HTML5 / CSS3:** Structure and UI overlay.
* **Three.js:** WebGL rendering engine for the particle system.
* **Google MediaPipe Hands:** Machine learning pipeline for hand landmark detection.
* **JavaScript (ES6):** Core logic and interaction handling.

---

## 💻 Installation & Usage

Because this project uses ES6 Modules and webcam access, **it must be run on a local server**. Opening the HTML file directly (`file://`) will result in security errors.

### Prerequisites
* A modern web browser (Chrome, Edge, or Firefox).
* A webcam.
* **Python 3.x** (recommended for starting a simple server).

### Step 1: Project Setup
1.  Create a folder on your computer (e.g., `ParticleSystem`).
2.  Save the project code as `index.html` inside this folder.

### Step 2: Running the Server
1.  Open your Command Prompt or Terminal.
2.  Navigate to your project folder:
    ```bash
    cd path/to/your/ParticleSystem
    ```
3.  Start the Python local server:
    ```bash
    python -m http.server
    ```
    *(If that doesn't work, try `python3 -m http.server`)*

### Step 3: Accessing the Application
1.  Open your web browser.
2.  Go to: `http://localhost:8000`
3.  **Allow Camera Access** when prompted by the browser.

---

## 🎮 Controls & Gestures

| Gesture | Action | Description |
| :--- | :--- | :--- |
| **Move Hand** | **Rotate** | Move your hand vertically or horizontally to rotate the 3D object. |
| **Pinch** (👌) | **Switch Shape** | Touch your **Index Finger** to your **Thumb** to trigger a shape morph. |
| **Spread Fingers** | **Expand** | Open your hand wide to make the particles expand/explode outward. |

---

## 🔧 Troubleshooting

**1. "Loading..." stays on the screen forever:**
* Check your browser console (F12 -> Console tab).
* If you see `Access to script... has been blocked by CORS policy`, you are likely opening the file directly. **You must use the Python server method described above.**

**2. Camera doesn't turn on:**
* Ensure no other application (Zoom, Teams, etc.) is currently using your webcam.
* Check that you clicked "Allow" on the browser permission popup.

**3. Performance is slow:**
* This is a GPU-intensive application. It runs best on devices with a dedicated graphics card.
* You can reduce the `PARTICLE_COUNT` variable in the code (line 55) to improve speed on older laptops.

---

## 📜 License

This project is open-source and available for educational purposes. 
This project is licensed under the MIT License.
---

**Created with Three.js and MediaPipe.**
