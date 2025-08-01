

```markdown
# PoseNet 360 🕺🎥

**PoseNet 360** is a real-time multi-angle human motion capture system that reconstructs 3D human poses using synchronized camera feeds. Built for immersive applications like AR/VR, sports biomechanics, and motion analysis, PoseNet 360 bridges 2D pose estimation with 3D reconstruction to deliver skeletal animation-ready outputs.

---

## 🔧 Features

- 📸 Multi-camera setup for capturing different angles of human motion  
- 🔍 2D Pose Estimation using state-of-the-art models (e.g., MediaPipe, OpenPose, YOLO + Keypoint R-CNN)  
- 🧠 2D-to-3D pose reconstruction using triangulation and optimization techniques  
- 🎮 Export support for 3D animation formats (e.g., BVH, FBX, or JSON skeletal data)  
- ⏱️ Real-time processing pipeline for interactive environments  
- 🧍‍♂️ Accurate skeletal keypoint tracking (up to 33 landmarks per frame)  

---

## 📂 Project Structure

```

PoseNet360/
├── data/                   # Input video/images or camera stream
├── models/                 # Pre-trained pose estimation models
├── src/
│   ├── pose\_estimation/    # 2D pose detection scripts
│   ├── reconstruction/     # 3D pose reconstruction code
│   ├── visualization/      # 2D/3D rendering utilities
│   └── export/             # Exporters for animation software
├── utils/                  # Helper functions and calibration tools
├── requirements.txt
└── README.md

````

---

## 🚀 Getting Started

### Prerequisites

- Python 3.8+
- pip (or conda)
- Webcam or multiple synchronized camera feeds

### Installation

```bash
git clone https://github.com/yourusername/PoseNet360.git
cd PoseNet360
pip install -r requirements.txt
````

### Dependencies

* OpenCV
* NumPy
* MediaPipe / OpenPose / YOLO (optional depending on 2D model)
* PyTorch or TensorFlow (based on selected pose estimation model)
* matplotlib (for visualization)

---

## 📸 Camera Calibration

Before 3D reconstruction, you must calibrate your camera setup using chessboard images or a calibration rig:

```bash
python src/utils/camera_calibration.py --input data/calibration/
```

---

## ▶️ Running the System

### 1. Perform 2D Pose Estimation

```bash
python src/pose_estimation/detect_pose.py --input data/camera1.mp4
```

Repeat for all camera feeds.

### 2. Reconstruct 3D Poses

```bash
python src/reconstruction/triangulate_3d.py --inputs data/cam1_keypoints.json data/cam2_keypoints.json
```

### 3. Visualize or Export

```bash
python src/visualization/plot_3d.py
python src/export/export_bvh.py --input reconstructed_3d.json
```

---

## 🎯 Use Cases

* **🎮 Virtual Reality / Gaming**: Control 3D avatars using real-world movements
* **⚽ Sports Biomechanics**: Analyze athletic performance with precision
* **🕺 Choreography**: Record, compare, and refine complex dance routines
* **🧑‍⚕️ Healthcare**: Monitor physical therapy and patient movement patterns

---

## 📊 Sample Output

![3D Pose Example](docs/sample_output.gif)

---

## 🤝 Contributing

We welcome contributions! Please open an issue or pull request to discuss feature improvements, bugs, or documentation updates.

---

## 📜 License

This project is licensed under the MIT License. See `LICENSE` file for details.

---

## 📬 Contact

Created by **PoseNet360 Team**
For questions or collaborations, reach out to: \[[your-email@example.com](mailto:your-email@example.com)]

---


