# 👹 Demon Slayer: Total Concentration AR

A real-time Augmented Reality experience that brings **Breathing Styles** and **Blood Demon Arts** from *Demon Slayer (Kimetsu no Yaiba)* to life using your webcam.

Built with **Three.js** for high-performance particle rendering and **MediaPipe** for precise hand tracking.

![g60gx41x1jaf1](https://github.com/user-attachments/assets/9cbe201e-7e36-474f-8181-cfa760e60234)

## ✨ Features

* **Real-Time Hand Tracking:** Detects hand landmarks instantly using computer vision.
* **Dynamic Particle System:** 10,000 interactive particles that morph into 3D shapes based on your movements.
* **Post-Processing:** Unreal-style Bloom (glow) effects adapted for web performance.
* **Gesture Recognition:** Trigger specific anime attacks using hand signs.
* **Optimized Performance:** Runs at ~60 FPS on modern devices using zero-allocation render loops and object pooling.

## 🎮 How to Play (Gesture Guide)

Ensure your hand is clearly visible to the camera. Use the following hand signs to trigger the techniques:

| Character | Technique | Hand Sign | Visual Effect |
| --- | --- | --- | --- |
| **Akaza** | *Destructive Death: Compass Needle* | 🖐️ **Open Hand** (All 5 Fingers) | A glowing blue, vertical snowflake/compass fractal that rotates behind your hand. |
| **Rengoku** | *Flame Breathing: Rising Scorching Sun* | 🖖 **3 Fingers** (Index, Middle, Ring UP) | A massive 80% crescent arc of fire slashing upwards on the right side. |
| **Tanjiro** | *Sun Breathing: Clear Blue Sky* | 👌 **Pinch** (Index + Thumb) | A blinding, pulsating ring of solar fire surrounding your fingers. |
| **Giyu** | *Water Breathing: Dead Calm* | ✌️ **Peace Sign** | Particles drop to the floor, creating a calm, rippling blue water surface. |
| **Muzan** | *Blood Demon Art: Black Blood* | 🤘 **Horns** (Index + Pinky) | Chaotic red/black tendrils and whips erupting from your hand. |
| **Neutral** | *Total Concentration Constant* | **Any other pose** | Idle dust motes floating in a dark void. |

## 🚀 Installation & Setup

Because this project uses ES6 Modules (`import ... from ...`), it **cannot** be run by simply opening the `index.html` file. You must use a local server.

### Option 1: VS Code (Easiest)

1. Open the project folder in **VS Code**.
2. Install the **Live Server** extension.
3. Right-click `index.html` and select **"Open with Live Server"**.

### Option 2: Node.js / Terminal

1. Install a simple http server globally:
```bash
npm install -g http-server

```


2. Navigate to the project directory:
```bash
cd path/to/project

```


3. Start the server:
```bash
http-server

```


4. Open the localhost link provided (usually `http://127.0.0.1:8080`).

## 🛠️ Technologies Used

* **[Three.js](https://threejs.org/):** For 3D graphics, particle systems, and vector mathematics.
* **[MediaPipe Hands](https://developers.google.com/mediapipe/solutions/vision/hand_landmarker):** Google's machine learning pipeline for ultra-fast hand tracking.
* **EffectComposer:** For the bloom/glow post-processing pipeline.

## ⚙️ Optimization Notes

To ensure smooth performance in the browser:

* **Particle Count:** Capped at 10,000 to balance visual density with CPU load.
* **Math Optimization:** Trigonometry calculations write directly to the buffer arrays to avoid creating thousands of temporary objects per frame (Garbage Collection optimization).
* **Bloom Resolution:** The glow effect renders at half-resolution to save GPU bandwidth without sacrificing visual quality.

## 📝 License

This project is for educational and fan purposes. 
