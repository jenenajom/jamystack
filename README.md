# jamystack
🔒 SheSafe: AI-Powered Gender-Sensitive Crowd & Harassment Detection System
An AI-driven solution to monitor overcrowding and detect potential harassment in public or disaster-prone zones, empowering safer, gender-sensitive emergency response.


🧠 Project Overview
During emergencies or crowded events, women often lack safe, private ways to communicate distress or threats. SheSafe aims to fill that gap using real-time AI to:

Detect crowd density from video footage.

Analyze suspicious or aggressive movements (as proxy for harassment).

Flag potentially dangerous situations for immediate action.

Later integrate into FPGA (Pink board) for edge deployment.

This repo contains a prototype for running detection in Google Colab using Python, OpenCV, and YOLOv5.

📂 Features
✅ YOLOv5 for people detection in video/image frames.

✅ Crowd density analysis based on real detection.

✅ Motion anomaly detection using background subtraction.

✅ Frame flagging and alerting if both overcrowding and movement threshold are crossed.

✅ Easy-to-use and Colab compatible.

🛠️ How It Works
Upload a video in Google Colab.

YOLOv5 detects people in each frame.

Crowd count is estimated using detection confidence.

BackgroundSubtractorMOG2 detects excessive motion (possible harassment).

If both overcrowding and anomalous motion are found → alert is logged.

Flagged frames are displayed visually.

🧾 Dependencies
Python 3.x

OpenCV

NumPy

PyTorch

Matplotlib

YOLOv5 (via torch.hub)

Install with:

bash
Copy code
pip install opencv-python matplotlib torch torchvision
🚀 Running in Google Colab
Open the notebook in Colab: SheSafe Crowd Monitor (Colab Link)

Upload your video file.

Run all cells.

See alerts and flagged frames in output.

🧪 Sample Output
yaml
Copy code
📸 Frame 240: Overcrowding and possible harassment detected!
📸 Frame 389: Overcrowding and possible harassment detected!
<img src="https://your-frame-example-url" width="400"/>
🎯 Future Scope
Integrate with FPGA (Pink Board) for real-time edge deployment.

Replace background subtraction with pose detection for better behavior modeling.

Add communication interface (mobile app or alert system) for gender-sensitive emergency messaging.

Train harassment detection models using datasets like [UBI-Fights], [AVA], [Stanford Drone Dataset].

📁 Repository Structure
bash
Copy code
├── yolov5_person_detection.ipynb     # YOLOv5-based detection + analysis
├── crowd_harassment_detection.py     # Script version
├── sample_video.mp4                  # Example input video
├── outputs/                          # Flagged frames and logs
└── README.md                         # This file
🙋‍♀️ Why SheSafe?
Women face increased risk in crowded or chaotic environments. SheSafe aims to give safety visibility, turning passive footage into actionable intelligence — especially during disasters or large gatherings.

👩‍💻 Author
Electronics & Instrumentation | FPGA + AI Enthusiast
Inspired by real-world challenges to build safe, inclusive tech solutions.

