# Yoga Pose Detection

Real-time yoga pose detection and classification using MediaPipe Pose.

## Overview
Detects and classifies yoga poses (e.g., T-Pose, Warrior II, Tree Pose) from images or video streams using MediaPipe's pose landmark detection and angle calculations.

## Detected Poses
- Warrior II Pose
- T Pose
- Tree Pose

## Setup
```bash
pip install -r requirements.txt
```

## Usage

**From a Python script:**
```python
from server.main1 import extractKeypoint, classifyPose
landmarks, keypoints, angles, image = extractKeypoint("path/to/image.jpg")
output_image, label = classifyPose(landmarks, image)
```

**Interactive notebook:**
Open `demo_mediapipe_pose.ipynb` for an end-to-end demonstration.

## Architecture
- **MediaPipe Pose** — Extracts 33 body landmarks
- **Angle Calculation** — Computes 8 key joint angles
- **Rule-Based Classifier** — Maps angle combinations to pose labels
