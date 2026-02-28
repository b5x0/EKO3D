# EKO3D AR Live Challenge

![EKO Mascot](mascott.png)

A fully native WebAR Gamified Trivia Experience built for the AI Night Challenge. EKO3D turns any standard 2D image target into a high-fidelity, interactive 3D dance stage right in the browser. 

*No apps to download. No backend servers to run. Just point your camera.*

## 🚀 Live Demo & Links
* **Live Deployment:** [Vercel Link Here]
* **Demo Video:** [YouTube/Loom Link Here]
* **Target Image:** The `targets.mind` file compiles the features of the target image. Scan the astronaut/robot marker to initiate the AR experience!

## 🎮 Features
- **Instant WebAR:** Powered by MindAR and Three.js, it natively accesses the mobile camera without requiring an external engine like Unity or 8thWall.
- **Dynamic 3D Character:** A fully rigged, animated `.glb` character model smoothly responds to inputs.
- **Trivia Engine:** Real-time randomized EKO3D trivia overlays seamlessly onto the camera feed.
- **Streak & Score Tracking:** Built-in gamification logic rewards correct answers (+10 pts) and punishes wrong ones (streak reset).
- **VFX & SFX:** Integrated `canvas-confetti` bursts and synthesized AudioContext spatial sounds.
- **Live Leaderboard:** A secondary "Arcade Scoreboard" display (`leaderboard.html`) powered by Firebase Realtime Database that updates instantly as players play on their own devices.

## 🛠️ Tech Stack & Architecture
This project was strictly designed to be a **static frontend**.
- **HTML/CSS/JS** (Vanilla, Mobile-First UI)
- **MindAR.js** (Image Tracking & AR Core engine)
- **Three.js** (WebGL 3D Rendering & Animation Mixer)
- **Firebase Realtime Database v8** (Real-time Cloud Leaderboard Synchronization)

Because of the static nature of the build, the Firebase configuration is provided client-side to allow instant, serverless database reads and writes via Firebase's secure rules engine (which has been scoped specifically to remain open only for the duration of the hackathon).

## 💻 Local Setup
To run this locally for testing or modification:
1. Clone the repository: `git clone https://github.com/b5x0/EKO3D.git`
2. Open the directory and serve the static files:
   ```bash
   npx serve . -p 8080
   ```
3. Open `http://localhost:8080` on your mobile device (ensure your computer and phone are on the same Wi-Fi network, or use a tunneling service like ngrok).

## ☁️ Deployment (Vercel)
This repository is pre-configured to deploy seamlessly as a static site.
1. Connect your GitHub account to Vercel.
2. Import the `EKO3D` repository.
3. Leave the Build Command and Output Directory fields completely blank.
4. Click **Deploy**. Vercel will instantly host `index.html` at the root URL.

---
*Built for the AI Night Challenge 2026.*
