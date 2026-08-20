<div align="center">

#CamRead

**A real-time gesture recognition app powered by MediaPipe, OpenCV, and Python**

![Python](https://img.shields.io/badge/Python-3.12-blue?style=flat-square&logo=python&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-4.x-green?style=flat-square&logo=opencv&logoColor=white)
![MediaPipe](https://img.shields.io/badge/MediaPipe-Google-red?style=flat-square)
![License](https://img.shields.io/badge/License-MIT-yellow?style=flat-square)

</div>

---

## What Is CamRead?

CamRead watches your webcam, reads your hand gestures in real time, and fires off animated GIF responses — no clicks, no keyboards, just vibes and hand signals. Flash a peace sign, get a reaction. Throw up the horns, get another. It's part tech demo, part party trick, entirely too fun.

Built entirely in Python with no external servers or special hardware — just your webcam and a willing hand.

---

## ✋ Supported Gestures

| Gesture | Sign | What It Triggers |
|--------|------|-----------------|
| Thumbs Up | 👍 | Positive reaction GIF |
| Peace Sign | ✌️ | Peace reaction GIF |
| Thumbs Down | 👎 | Negative reaction GIF |
| Middle Finger | 🖕 | ...you know the one |
| Rock Sign | 🤘 | Rock on GIF |

---

## 🚀 Getting Started

### Prerequisites

- Python **3.12+**
- A working webcam
- A hand (one is sufficient)

### Installation

1. **Clone the repo**

   ```bash
   git clone https://github.com/Rajindu-Amithirigala/camread.git
   cd camread
   ```

2. **Install dependencies**

   ```bash
   pip install opencv-python mediapipe numpy Pillow
   ```

   > Tkinter ships with Python on most systems. If it's missing, install it via your package manager (e.g. `sudo apt install python3-tk` on Linux).

3. **Run the app**

   ```bash
   python main.py
   ```

4. Hit **Launch** on the start screen, point your webcam at your hand, and start gesturing.

---

## 🏗️ How It Works

```
Webcam Feed
    │
    ▼
MediaPipe Hand Tracking  ──►  21 hand landmarks detected per frame
    │
    ▼
Gesture Classifier  ──►  Finger state logic maps landmarks → gesture label
    │
    ▼
Tkinter GUI  ──►  Animated GIF plays in response, overlay shown on video feed
```

- **MediaPipe** tracks 21 hand landmarks per frame at high speed
- A custom classifier reads finger positions and angles to identify each gesture
- **OpenCV** handles the live webcam feed and draws overlays
- **Tkinter** manages the GUI start screen and GIF display
- **Pillow** handles animated GIF playback frame-by-frame

---

## 📦 Dependencies

| Package | Purpose |
|--------|---------|
| `opencv-python` | Webcam capture and video rendering |
| `mediapipe` | Real-time hand landmark detection |
| `numpy` | Numerical operations on landmark data |
| `Pillow` | Animated GIF loading and display |
| `tkinter` | GUI start screen (built into Python) |

---

## 🗺️ Roadmap

Things worth building next:

- [ ] **Gesture-based interactions** — use gestures to control apps, media, or presentations
- [ ] **Sound effects** — trigger audio clips alongside GIFs
- [ ] **More gestures** — wave, OK sign, finger guns, pointing, etc.
- [ ] **Custom GIF mapping** — let users assign their own GIFs to gestures
- [ ] **Multi-hand support** — detect both hands simultaneously
- [ ] **Confidence threshold tuning** — reduce false positives in tricky lighting

---

## 🤝 Credits

- [**MediaPipe**](https://mediapipe.dev/) by Google — hand tracking engine
- [**OpenCV**](https://opencv.org/) — computer vision and video capture
- [**Pillow**](https://python-pillow.org/) — image and GIF handling

---

<div align="center">

Made with Python, a webcam, and questionable hand gestures.

</div>
