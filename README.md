Got it! Here's the updated `README.md` file with the project name as **AI Threat Detection System**:

---

# 🛡️ AI Threat Detection System

This is a real-time **AI-powered surveillance system** that combines **object detection**, **hand movement tracking**, and **facial recognition** to detect potential threats, track suspicious activity, and recognize individuals.

---

# 🚀 Features

- 🔫 **Threat Detection** using YOLOv8 for objects like knives, guns, and other hazardous items.
- ✋ **Hand Movement Tracking** with MediaPipe to flag unusual or suspicious hand activity.
- 🧠 **Facial Recognition** to identify known individuals in the camera feed.
- 🎥 **Live Webcam Monitoring** for real-time threat visualization and tracking.

---

# 📦 Requirements

Install the required Python libraries using:

```bash
pip install opencv-python numpy mediapipe face_recognition ultralytics
```

> **Note**: The `face_recognition` library depends on `dlib`, which may require Visual Studio (Windows) or `cmake` and `boost` (Linux/macOS) to compile.

---

# 📁 Folder Structure

```
AI_Threat_Detection_System/
│
├── main.py                        # Core script
├── faces/                         # Directory for known face images
│   ├── shivam.jpeg
│   ├── naman.jpeg
│   └── mayank.jpeg
└── README.md                      # This file
```

---

# ⚙️ How It Works

1. **YOLOv8 Object Detection**
   - Uses the pre-trained `yolov8s.pt` model from Ultralytics.
   - Identifies threatening objects like:
     ```
     ["Knife", "Smoke", "needle", "Scissors", "Chainsaw", "Gun"]
     ```

2. **Face Recognition**
   - Loads face encodings from images of known individuals.
   - Detects faces in the webcam feed and labels them.

3. **Hand Tracking**
   - Uses MediaPipe to detect hand landmarks.
   - Calculates wrist movement to flag unusual hand gestures or rapid motion.

4. **Face Offset Detection**
   - Tracks the position of detected faces relative to the frame center using smoothing.
   - Useful for attention monitoring or smart PTZ camera integration.

---

# 🧪 How to Run

Make sure your webcam is connected and then run:

```bash
python main.py
```

Press `q` to exit the program.

---

# ⚠️ Notes

- Replace the images in the `faces/` folder with your own known face data for facial recognition.
- Ensure your webcam has sufficient lighting for better detection accuracy.
- Threat detection is sensitive to object visibility and clarity.

---

# 💡 Potential Extensions

- Trigger a **buzzer or alarm** via Arduino using `serial` when a threat is detected.
- Add **timestamped logging** for detected threats and faces.
- Integrate **SMS/email alerts** for remote monitoring.
- Deploy on **Jetson Nano or Raspberry Pi** for edge surveillance systems.

---
