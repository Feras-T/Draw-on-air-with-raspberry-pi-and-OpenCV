# Draw on Air (Raspberry Pi + OpenCV)

Draw on the screen by moving your finger in the air — using a Raspberry Pi camera feed and OpenCV.

This repo contains:
- `code.py` — the Python/OpenCV implementation
- `Video.mp4` — a demo recording of the project in action :contentReference[oaicite:1]{index=1}

---

## Demo

📹 See: **`Video.mp4`** in this repository. :contentReference[oaicite:2]{index=2}

---

## How it works (high level)

1. The camera stream opens in a window.
2. You **sample** the fingertip (or the colored point you want to track) by clicking it with the mouse.
3. The script tracks that point and draws its motion path on the video feed.

> Tip: Good lighting makes tracking much more stable.

---

## Requirements

### Hardware
- Raspberry Pi (Pi 3/4/5 should work)
- Raspberry Pi Camera (PiCamera module) or a USB webcam
- Monitor + mouse/keyboard (for the initial click/sample step)

### Software
- Python 3
- OpenCV (cv2)

---

## Setup

### 1) Enable / connect the camera
- If using a PiCamera: make sure the camera is enabled and detected by your OS.
- If using a USB webcam: plug it in and confirm it appears as a video device.

### 2) Install dependencies
On Raspberry Pi OS, install pip (if needed) and OpenCV:

```bash
sudo apt update
sudo apt install -y python3 python3-pip
pip3 install opencv-python


This implementation is based on the concept/demo from ProgrammingHut:

YouTube: https://www.youtube.com/watch?v=BDyhyQ1qjBY
