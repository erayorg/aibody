📖 Introduction

aibody is a future-oriented open-source AI body perception framework designed to deeply integrate computer vision with human body science. Whether you're building intelligent fitness apps, developing medical rehabilitation systems, or creating immersive VR experiences, aibody provides you with powerful body data perception capabilities.

We believe everyone's body deserves to be digitally understood. With aibody, you can easily build your own digital twin body.

✨ Key Features

Module	Description	Status	
Pose Estimation Engine	2D/3D real-time keypoint detection with 95%+ accuracy	✅ Available	
Action Recognition System	Custom action classification with anomaly alerts	✅ Available	
Physiological Data Fusion	Integration with wearables (HR, SpO2, etc.)	🚧 In Dev	
Digital Twin Generation	Building personalized virtual body models	🚧 In Dev	
Cloud Sync Service	Real-time data cloud upload & multi-device sync	📅 Planned	

🚀 Quick Start

Requirements
- Python 3.8+
- CUDA 11.0+ (recommended for GPU acceleration)
- Webcam or video file

Installation

```bash
# Clone repository
git clone https://github.com/erayorg/aibody.git
cd aibody

# Create virtual environment
python -m venv venv
source venv/bin/activate  # Linux/Mac
# or venv\Scripts\activate  # Windows

# Install dependencies
pip install -r requirements.txt

# Download pre-trained models
python scripts/download_models.py
```

Run Examples

```bash
# Start real-time pose detection
python examples/pose_estimation.py --source 0  # 0 for default webcam

# Run web interface
python -m aibody.web.app
# Visit http://localhost:8000
```

📁 Project Structure

```
aibody/
├── aibody/                 # Core library
│   ├── core/               # Pose estimation core
│   ├── models/             # Pre-trained models
│   ├── fusion/             # Multi-modal data fusion
│   └── digital_twin/       # Digital twin module
├── examples/               # Example code
├── web/                    # Web service & frontend
├── docs/                   # Documentation
├── tests/                  # Test cases
└── scripts/                # Utility scripts
```

🛠️ Architecture

```
┌─────────────────────────────────────┐
│        Application Layer             │
│  ┌─────────┐ ┌─────────┐ ┌────────┐ │
│  │Fitness  │ │Medical │ │ VR     │ │
│  │   App   │ │ System  │ │ Game   │ │
│  └────┬────┘ └────┬────┘ └───┬────┘ │
└───────┼───────────┼──────────┼───────┘
        │           │          │
┌───────┴───────────┴──────────┴───────┐
│         API Layer (FastAPI)            │
└─────────────────┬───────────────────┘
                  │
┌─────────────────┴───────────────────┐
│         Core Engine Layer            │
│  ┌──────────┐ ┌──────────┐ ┌────────┐ │
│  │  Pose    │ │ Action   │ │ Data   │ │
│  │ Estimation│ │Recognition│ │ Fusion │ │
│  │(MediaPipe│ │  (LSTM)  │ │(Kalman)│ │
│  │ /YOLOv8) │ │          │ │ Filter)│ │
│  └──────────┘ └──────────┘ └────────┘ │
└───────────────────────────────────────┘
                  │
┌─────────────────┴───────────────────┐
│          Data Layer                  │
│  ┌──────────┐ ┌──────────┐ ┌────────┐ │
│  │ Video    │ │ Sensors  │ │ Cloud  │ │
│  │ Stream   │ │  (BLE)   │ │ (AWS)  │ │
│  │ (OpenCV) │ │          │ │        │ │
│  └──────────┘ └──────────┘ └────────┘ │
└───────────────────────────────────────┘
```

🤝 Contributing

We welcome all forms of contributions!

Especially needed:
- 🐛 Bug reports & fixes
- 📖 Documentation translation & improvement
- 🧠 New model integration (pose estimation, action recognition)
- 🎨 UI/UX design
- 🌍 Multi-language support

📜 License

This project is open-sourced under the [MIT License](LICENSE).

🙏 Acknowledgments

- [MediaPipe](https://mediapipe.dev) for powerful pose estimation foundation
- [PyTorch](https://pytorch.org) deep learning framework
- All contributors and community supporters
