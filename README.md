# 🔒 SheSafe: AI-Powered Gender-Sensitive Crowd & Harassment Detection System

> An AI-driven solution to monitor overcrowding and detect potential harassment in public or disaster-prone zones, empowering safer, gender-sensitive emergency response.

---

## 🧠 Project Overview

During emergencies or crowded events, women often lack safe, private ways to communicate distress or threats. **SheSafe** fills that gap by using real-time AI to:

- Detect **crowd density** from video footage.
- Analyze **suspicious or aggressive movement patterns** (as proxies for harassment).
- Flag potentially dangerous situations for immediate attention.
- Provide a foundation for **FPGA-based** edge deployment (using Pink board).

This repository contains a prototype implementation in **Python**, tested in **Google Colab**, using OpenCV, PyTorch, and YOLOv5.

---

## ✅ Features

- 🎯 Real-time person detection with YOLOv5
- 📊 Crowd density estimation
- 🔍 Harassment/movement anomaly detection using background subtraction
- 🛎️ Automated alert logging and frame flagging
- 📦 Compatible with Google Colab for easy experimentation

---

## 📂 How It Works

1. Upload a **video file** in Google Colab.
2. Use **YOLOv5** to detect people per frame.
3. Estimate **crowd size** from detections.
4. Apply **BackgroundSubtractorMOG2** to detect abnormal movement (possible harassment).
5. If both crowd and motion thresholds are exceeded → trigger alert.
6. Display **flagged frames** for review.

---

## 📦 Dependencies

- Python 3.x
- OpenCV
- NumPy
- Matplotlib
- PyTorch
- YOLOv5 (via `torch.hub`)

Install in your local environment:

```bash
pip install opencv-python matplotlib torch torchvision
