# RWCP-S 🚆
## 5G-Enabled Predictive AI System for Railway Collision Prevention & Smart Track Safety

**RWCP-S (Railway Collision Prevention System)** is an intelligent railway safety system designed to detect, analyze, and predict potential collisions involving **humans, animals, and obstacles** on railway tracks.

The system combines **Artificial Intelligence, Computer Vision, IoT, Edge Computing, Stereo Vision, and 5G communication** to transform railway safety from a reactive monitoring approach into a proactive and predictive system.

---

## 👥 Team

**Manasi Baranidharan**  
SRM Institute of Science and Technology

**Nithveen Kavi P**  
SRM Institute of Science and Technology

---

## 📌 Overview

Railway tracks frequently encounter unexpected objects, wildlife, and human trespassers. Traditional monitoring approaches such as manual surveillance and track patrols may not provide the response time required for rapidly developing situations.

RWCP-S addresses this challenge through an **edge-based intelligent monitoring architecture**.

The system continuously monitors railway tracks using a stereo depth camera and processes the captured data locally using AI models.

The system can:

- Detect humans, animals, and obstacles
- Estimate object distance using stereo vision
- Track object movement
- Analyze potential collision risks
- Classify risk levels
- Generate real-time alerts
- Transmit critical information through 5G
- Provide centralized monitoring through a web dashboard

---

## 🎯 Objectives

The primary objectives of RWCP-S are:

1. Develop a real-time railway track monitoring system.
2. Detect humans, animals, and obstacles using AI.
3. Estimate object distance using stereo depth information.
4. Predict potential collision risks.
5. Classify threats into different risk levels.
6. Provide low-latency alerts using 5G communication.
7. Enable edge-based AI processing with minimal cloud dependency.
8. Provide railway authorities with a centralized monitoring dashboard.
9. Reduce false positives using multi-frame validation.
10. Support future integration with railway safety and signaling systems.

---

## 🧠 Core Technologies

### Artificial Intelligence

- YOLO Nano
- TensorFlow Lite
- Scikit-learn
- Predictive analytics
- Object classification
- Risk prediction

### Computer Vision

- OpenCV
- Stereo vision
- Depth estimation
- Object tracking
- Image enhancement
- Real-time video processing

### Edge Computing

- Raspberry Pi 4 (4GB)
- INT8 model quantization
- On-device AI inference
- Low-latency processing

### IoT

- Stereo depth camera
- Temperature sensor
- Humidity sensor
- Light sensor
- Battery and power management

### Communication

- 5G connectivity
- REST APIs
- WebSockets
- Real-time alert transmission

### Backend

- Python
- Django
- REST API
- Authentication
- Alert management
- Administrative controls

### Frontend

- React.js
- HTML5
- CSS3
- JavaScript

### Database

- SQLite for prototype development
- PostgreSQL / MongoDB for future production deployment

---

## 🏗️ System Architecture

RWCP-S follows a three-layer distributed architecture.

```text
                    ┌──────────────────────────┐
                    │     Railway Track        │
                    │  Humans / Animals /      │
                    │       Obstacles          │
                    └────────────┬─────────────┘
                                 │
                                 ▼
                 ┌──────────────────────────────┐
                 │          EDGE LAYER           │
                 │                              │
                 │   Stereo Depth Camera        │
                 │            │                 │
                 │            ▼                 │
                 │     Raspberry Pi 4           │
                 │            │                 │
                 │       YOLO Nano              │
                 │            │                 │
                 │   Object Detection           │
                 │   Distance Estimation        │
                 │   Risk Assessment            │
                 └──────────────┬───────────────┘
                                │
                              5G
                                │
                                ▼
                 ┌──────────────────────────────┐
                 │      COMMUNICATION LAYER     │
                 │                              │
                 │       REST API               │
                 │       WebSockets             │
                 │       5G Network             │
                 └──────────────┬───────────────┘
                                │
                                ▼
                 ┌──────────────────────────────┐
                 │    CONTROL & APPLICATION     │
                 │           LAYER              │
                 │                              │
                 │       Django Backend         │
                 │            │                 │
                 │            ▼                 │
                 │      React Dashboard         │
                 │            │                 │
                 │      Alerts / Analytics      │
                 │      Risk Visualization      │
                 └──────────────────────────────┘
```

---

## 🔄 System Workflow

```text
Camera Capture
      ↓
Edge Processing
      ↓
AI Object Detection
      ↓
Object Classification
      ↓
Stereo Depth Estimation
      ↓
Distance Calculation
      ↓
Motion Tracking
      ↓
Collision Risk Prediction
      ↓
Risk Classification
      ↓
Decision Engine
      ↓
5G Alert Transmission
      ↓
Control Center Dashboard
      ↓
Action / Response
```

---

## 🚨 Risk Classification

RWCP-S categorizes detected situations into four risk levels:

| Risk Level | Description |
|------------|-------------|
| 🟢 Low | Object detected but collision probability is low |
| 🟡 Medium | Object approaching a potentially unsafe zone |
| 🟠 High | Significant collision probability detected |
| 🔴 Critical | Immediate collision threat requiring urgent action |

The final risk assessment can consider:

- Object type
- Object distance
- Object movement
- Train speed
- Track position
- Environmental conditions
- Estimated stopping distance
- Time-to-collision

---

## 🔍 Key Features

### AI-Based Detection

Real-time identification of:

- Humans
- Animals
- Railway obstacles
- Other relevant objects

### Stereo Vision

Stereo cameras provide depth information for estimating the distance between detected objects and the railway environment.

### Predictive Collision Analysis

The system combines distance, movement, and train-related parameters to estimate collision probability.

### Edge AI

AI inference is performed locally on the edge device to reduce latency and dependency on cloud processing.

### 5G Communication

Critical alerts and processed information can be transmitted to a centralized control center using low-latency communication.

### Smart Alert System

The system can generate different levels of warnings depending on the estimated risk.

### Environmental Awareness

Environmental sensors can provide:

- Temperature
- Humidity
- Light conditions

This information can be incorporated into risk analysis.

### Multi-Frame Validation

Multiple frames can be analyzed before generating an alert to reduce false positives.

### Centralized Dashboard

The proposed dashboard provides:

- Live monitoring
- Alerts
- Risk levels
- Analytics
- Risk-zone visualization
- System status

---

## 🛑 Braking Assistance

RWCP-S includes a proposed decision-support mechanism based on estimated stopping distance.

A simplified conceptual model is:

```text
Detection
    ↓
Distance Estimation
    ↓
Train Speed
    ↓
Stopping Distance
    ↓
Time-to-Collision
    ↓
Risk Evaluation
    ↓
Warning / Emergency Recommendation
```

> **Important:** The prototype is intended as a research and decision-support system. Any real-world automated braking or railway signaling integration would require rigorous safety validation, certification, redundancy, and approval by the relevant railway authorities.

---

## 📡 5G Communication

5G connectivity is proposed to provide rapid communication between distributed railway monitoring units and centralized control infrastructure.

The communication architecture can support:

```text
Edge Device
     │
     │ 5G
     ▼
Communication Gateway
     │
     ▼
Backend API
     │
     ├── Alert Service
     ├── Analytics
     └── Database
     │
     ▼
Control Center Dashboard
```

---

## 🖥️ Dashboard

The planned monitoring dashboard can provide railway authorities with:

- Live system status
- Detected objects
- Risk levels
- Real-time alerts
- Incident history
- Risk heatmaps
- Environmental information
- Device status
- Analytics

---

## 📦 Hardware Prototype

The proposed prototype uses relatively affordable hardware:

| Component | Purpose |
|-----------|---------|
| Raspberry Pi 4 (4GB) | Edge computing |
| Stereo Depth Camera | Object and depth detection |
| Temperature Sensor | Environmental monitoring |
| Humidity Sensor | Environmental monitoring |
| Light Sensor | Visibility estimation |
| 5G Module | Communication |
| Battery | Portable power |
| Optional Solar Panel | Sustainable power |

Estimated prototype cost:

**₹19,000 – ₹21,000 per monitoring unit**

---

## 📁 Proposed Repository Structure

```text
RWCP-S/
│
├── README.md
├── LICENSE
├── .gitignore
│
├── backend/
│   ├── manage.py
│   ├── api/
│   ├── alerts/
│   ├── authentication/
│   └── risk_engine/
│
├── frontend/
│   ├── src/
│   ├── public/
│   └── package.json
│
├── edge/
│   ├── detection/
│   ├── tracking/
│   ├── depth_estimation/
│   ├── sensors/
│   └── communication/
│
├── models/
│   ├── yolo/
│   └── tensorflow_lite/
│
├── datasets/
│   └── README.md
│
├── notebooks/
│   ├── data_analysis/
│   └── model_training/
│
├── docs/
│   ├── architecture/
│   ├── research/
│   └── diagrams/
│
├── tests/
│
└── requirements.txt
```

---

## ⚙️ Development Setup

### Clone the Repository

```bash
git clone https://github.com/<your-username>/RWCP-S.git
cd RWCP-S
```

### Backend

Create a Python virtual environment:

```bash
python -m venv venv
```

Activate it on Linux:

```bash
source venv/bin/activate
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Run the Django development server:

```bash
python manage.py runserver
```

### Frontend

```bash
cd frontend
npm install
npm run dev
```

> The commands above represent the planned development setup and may need to be updated as the implementation evolves.

---

## 🤖 AI Pipeline

The proposed AI pipeline follows:

```text
Video Stream
     ↓
Frame Extraction
     ↓
Image Preprocessing
     ↓
YOLO Nano Detection
     ↓
Object Classification
     ↓
Object Tracking
     ↓
Stereo Depth Estimation
     ↓
Distance Calculation
     ↓
Risk Prediction
     ↓
Alert Generation
```

---

## 📊 Risk Prediction Concept

A potential risk engine can combine multiple parameters:

```text
Risk Score =
    Distance Factor
  + Speed Factor
  + Object Movement Factor
  + Track Position Factor
  + Environmental Factor
```

The resulting score can be mapped to:

```text
Low
 ↓
Medium
 ↓
High
 ↓
Critical
```

The exact scoring methodology should be calibrated and validated using real-world or appropriately simulated railway safety datasets.

---

## 🌍 Deployment Strategy

RWCP-S is designed for deployment in high-risk areas such as:

- Forest railway corridors
- Unmanned crossings
- Wildlife zones
- Low-visibility areas
- Accident-prone railway sections
- High-risk track segments

The architecture allows multiple monitoring units to communicate with a centralized platform.

```text
Unit 01 ─┐
Unit 02 ─┤
Unit 03 ─┼──► 5G Network ───► Central Platform
Unit 04 ─┤
Unit N  ─┘
```

---

## 📈 Scalability

The system is designed to scale from a prototype into a larger distributed railway monitoring platform.

Future deployments could include:

- Additional monitoring units
- Cloud-based analytics
- Advanced AI models
- Additional environmental sensors
- Mobile applications
- Railway signaling integration
- Centralized nationwide analytics

---

## 🔮 Future Scope

### Advanced AI

Future versions may incorporate:

- Animal behavior prediction
- Human behavior prediction
- Trajectory forecasting
- Temporal deep learning
- Anomaly detection
- Advanced risk prediction

### Railway Integration

Potential future integration includes:

- Railway signaling systems
- Control centers
- Automated speed regulation
- Braking assistance
- Smart railway infrastructure

### Edge-Cloud Architecture

A hybrid architecture could combine:

```text
Edge
 ↓
Fast Local Decisions
 ↓
Cloud
 ↓
Large-Scale Analytics
 ↓
Model Updates
 ↓
Edge Deployment
```

### Smart Transportation

The underlying architecture could potentially be adapted for:

- Metro systems
- Highways
- Industrial safety
- Logistics infrastructure
- Smart city applications

---

## 🌱 Sustainability

RWCP-S aims to support sustainable infrastructure through:

- Low-power edge computing
- Optional solar-powered deployment
- Reduced cloud dependency
- Wildlife protection
- Reduced accident-related resource consumption

---

## 📌 Project Status

**Status:** 🚧 Research / Prototype Development

The repository represents an academic research and prototype project. Hardware integration, AI model training, real-world testing, 5G communication, and railway-system integration may be developed incrementally.

---

## ⚠️ Safety Disclaimer

RWCP-S is an academic research and prototype project.

It is **not a certified railway safety system** and should not be connected directly to operational railway signaling, braking, or control systems without appropriate engineering validation, redundancy, cybersecurity assessment, regulatory approval, and safety certification.

Any automated intervention proposed by the project should initially be treated as **decision support** rather than a replacement for certified railway safety systems.

---

## 📚 Research Documentation

The complete project proposal is available in this repository:

**`RWCP-S Project Proposal.pdf`**

The proposal covers:

- Problem statement
- Proposed solution
- System architecture
- Technology stack
- Workflow
- Key capabilities
- Impact and benefits
- Deployment strategy
- Scalability
- Future scope
- Conclusion

---

## 🎓 Academic Context

**Institution:** SRM Institute of Science and Technology

**Project:** RWCP-S — Railway Collision Prevention System

**Domains:**

- Artificial Intelligence
- Machine Learning
- Computer Vision
- Internet of Things
- Edge Computing
- 5G Networks
- Predictive Analytics
- Smart Transportation
- Railway Safety

---

## 👨‍💻 Contributors

### Manasi Baranidharan

SRM Institute of Science and Technology

### Nithveen Kavi P

SRM Institute of Science and Technology

---

## ⭐ Vision

> **Making railway safety proactive, predictive, intelligent, and connected.**

RWCP-S aims to demonstrate how AI, IoT, edge computing, and modern communication technologies can work together to create safer and smarter transportation infrastructure.

---

## 📄 License

This project is intended for **academic and research purposes**.

Add an appropriate open-source license to this repository if the project is later released for public reuse.

---

## 🔗 Project Links

- **Research Proposal:** `RWCP-S Project Proposal.pdf`
- **GitHub Repository:** Add repository URL
- **Project Demo:** Add demo URL when available
- **Research Paper:** Add publication link when available

---

### Keywords

`AI` `Machine Learning` `Computer Vision` `YOLO` `TensorFlow Lite` `OpenCV` `IoT` `Edge Computing` `Raspberry Pi` `5G` `Railway Safety` `Collision Prevention` `Predictive Analytics` `Stereo Vision` `Object Detection` `Smart Transportation` `Railway Technology`
