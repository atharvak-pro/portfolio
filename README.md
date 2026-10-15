# Atharv Vinod Kurambhatti - Interactive 3D Portfolio

A high-tech, single-page interactive portfolio website for **Atharv Vinod Kurambhatti**, Third-Year ENTC Engineering student and aspiring Cloud/IoT Engineer. The design seamlessly blends high-tech Cloud & IoT aesthetics (AWS deep space theme, neon cyan, glowing orange) with interactive 3D cricket physics.

---

## 🌟 Key Highlights & Architecture

### 1. Hero Section (3D Orbiting Cricket Ball & Glowing Cloud)
- **Mount Point**: `#hero-canvas-container` and `<canvas id="hero-canvas">`
- **Engine**: Three.js WebGL with `ACESFilmicToneMapping`.
- **3D Assets**:
  - **Volumetric Glowing Cloud**: Clustered procedural sphere meshes with a custom translucent physical material (`MeshPhysicalMaterial`) that has transmission, roughness, and internal dual-point lights (neon cyan & electric amber).
  - **Photorealistic Cricket Ball**: Crimson lacquer sphere (`MeshStandardMaterial`) with a raised, hand-stitched white equatorial seam and rotating stitches.
  - **Elliptical Orbit**: Continuous smooth orbit along an inclined 3D plane with a glowing particle track and floating IoT data telemetry nodes (octahedrons).
  - **Parallax & Drag Interactivity**: Smooth cursor lerping for parallax and click-and-drag / touch rotation in 3D space.

### 2. About Me Section (3D LED Cricket Stumps & Zing Bails)
- **Mount Point**: `#stumps-canvas-container` and `<canvas id="stumps-canvas">`
- **3D Assets**:
  - Three carbon-ash stumps (Off, Middle, Leg) with vertical embedded frosted acrylic LED channels.
  - Two Zing bails resting in the top grooves.
  - White bowling crease line and cyber yard markings.
- **Scroll & Click Trigger**:
  - As the user scrolls into the section, **GSAP ScrollTrigger** fires a simulated 145.4 km/h ball impact!
  - Stumps tilt, bails launch with physical angular momentum, and the Zing LEDs flash intensely in high-voltage neon red and fire orange.
  - Auto-reassembles cleanly after 2.8 seconds.
  - Can also be manually tested anytime via the **"145 km/h"** button or by clicking the 3D canvas directly.

### 3. Tech Stack & Skills Bento Grid
- **Design**: Bento-box CSS grid with 3D tilt interaction.
- **Interactive Tilt**: Pure mathematical 3D perspective tilt (`perspective(1000px) rotateX(...) rotateY(...)`) following cursor coordinates with an internal radial glow border.
- **Categories**:
  - ☁️ **Cloud & AWS Infrastructure** (EC2, Lambda, S3, IAM, VPC, CloudWatch, DynamoDB)
  - 🔌 **IoT & Embedded Systems** (ESP32, Arduino, MQTT, Raspberry Pi, Embedded C/C++, Sensors)
  - 🛠️ **DevOps & Infrastructure as Code** (Docker, GitHub Actions CI/CD, Linux CLI, Git, Terraform)
  - 🧠 **AI, Machine Learning & Computer Vision** (Python 3.x, OpenCV, TensorFlow, Scikit-learn, Edge AI)

### 4. Footer & Contact (3D Bat on Server Rack Back-to-Top)
- **Mount Point**: `#footer-bat-container` and `<canvas id="footer-bat-canvas">`
- **3D Assets**:
  - 42U datacenter server rack with blinking status LEDs across multiple blade units.
  - Handcrafted English Willow cricket bat with carbon grip and rubber ribs leaning against the chassis at a 15-degree angle.
- **Interactivity**:
  - Hovering causes the server LEDs to accelerate and the bat to gleam.
  - Clicking the bat executes a smooth 3D swing animation and smoothly scrolls the window back to the top of the page.

### 5. Synthesized Web Audio API (Optional)
- Ultra-clean, non-intrusive sound effects (button clicks, wicket zing flash, bat stroke).
- Audio is muted by default with an easy toggle button in the navigation bar.

---

## 🚀 Running Locally

The portfolio is built with zero-build dependency HTML5, Tailwind CSS, GSAP, and Three.js loaded via optimized CDNs.

### Using Python
```bash
# In the project directory:
python -m http.server 3000
```
Then visit: `http://localhost:3000`

---

## 📂 File Structure

```
d:\atharvak\
├── index.html            # Main single-page portfolio layout & semantic HTML5
├── README.md             # Project documentation & Three.js guide
├── css\
│   └── style.css         # Glassmorphism, neon glows, custom scrollbars & bento tilt styles
└── js\
    ├── main.js           # GSAP ScrollTrigger, 3D tilt, Web Audio, telemetry simulator
    ├── three-hero.js     # Three.js glowing cloud + orbiting cricket ball scene
    ├── three-stumps.js   # Three.js LED stumps + Zing bails shatter physics
    └── three-footer.js   # Three.js server rack + cricket bat back-to-top button
```
