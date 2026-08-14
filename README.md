# 🚧 IRIS — Intelligent Road Inspection System

<p align="center">
  <b>AI-Powered Road Inspection & Pothole Detection System</b>
</p>

<p align="center">
  Detect • Classify • Locate • Review • Improve
</p>

---

## 📌 About IRIS

**IRIS (Intelligent Road Inspection System)** is an AI-powered road inspection platform designed to detect potholes and road damage using **computer vision and YOLOv8**.

The system processes live camera, video, or IP-camera input, detects potholes in real time, classifies their severity, records inspection data, and provides dashboards for field operators and municipal authorities.

IRIS aims to make road inspection **faster, smarter, and more data-driven**.

---

## 🎯 Problem

Traditional road inspection depends heavily on manual surveys, making large-scale monitoring time-consuming and difficult to manage.

IRIS addresses this by using AI to:

* Detect road damage automatically
* Identify pothole severity
* Record inspection sessions
* Capture supporting evidence
* Associate detections with location data
* Provide a centralized review dashboard

---

## 💡 How IRIS Works

```text
Camera / Video / IP Camera
            ↓
       YOLOv8 Model
            ↓
    Pothole Detection
            ↓
 Duplicate Detection Check
            ↓
   Severity Classification
            ↓
   ┌────────┴────────┐
   ↓                 ↓
Dashboard       High Severity
                     ↓
              Snapshot + GPS
                     ↓
             Data Persistence
                     ↓
            Municipal Dashboard
                     ↓
             Review / Approval
                     ↓
              PDF Reporting
```

---

## ✨ Key Features

### 🤖 AI-Based Detection

* Real-time pothole detection
* YOLOv8 object detection
* OpenCV-based image processing
* Detection confidence tracking
* Duplicate detection filtering using IoU

### 🚧 Severity Classification

Road damage can be categorized as:

* 🟢 Low
* 🟡 Medium
* 🔴 High

### 📍 GPS Integration

High-severity detections can be associated with GPS information to help identify the location of road damage.

### 🚗 Driver / Field Dashboard

* Live camera feed
* Inspection session controls
* Detection counters
* Detection feed
* Charts and analytics
* Alert states

### 🏛️ Municipal Dashboard

Municipal users can:

* Review high-severity detections
* Approve detections
* Decline detections
* View locations on a map
* Generate PDF reports

### 🔔 Alert Integration

Optional hardware and voice alerts can be used for high-severity detections.

### 🧠 AI Analysis

Optional Google Gemini integration can provide additional analysis and prioritization context.

### ☁️ Cloud Integration

Optional Firebase / Firestore integration can be used for cloud-backed records.

---

## 🧠 AI Pipeline

```text
Road Frame
    ↓
OpenCV Processing
    ↓
YOLOv8 Inference
    ↓
Pothole Detection
    ↓
Confidence Evaluation
    ↓
IoU-Based Deduplication
    ↓
Severity Classification
    ↓
GPS + Evidence
    ↓
Database
    ↓
Municipal Review
```

---

## 🛠️ Technology Stack

| Category                | Technology              |
| ----------------------- | ----------------------- |
| Programming Language    | Python                  |
| AI / Object Detection   | YOLOv8 / Ultralytics    |
| Computer Vision         | OpenCV                  |
| Backend                 | Flask                   |
| Real-Time Communication | Flask-SocketIO          |
| Database                | SQLite                  |
| Frontend                | HTML, CSS, JavaScript   |
| Charts                  | Chart.js                |
| Maps                    | Leaflet + OpenStreetMap |
| PDF Reports             | ReportLab               |
| GPS                     | Windows Location API    |
| Hardware Alerts         | Arduino + PySerial      |
| Voice Alerts            | pyttsx3                 |
| Optional AI             | Google Gemini           |
| Optional Cloud          | Firebase / Firestore    |
| Version Control         | Git + GitHub            |

---

## 🏗️ System Architecture

```text
                    ┌─────────────────┐
                    │ Camera / Video  │
                    └────────┬────────┘
                             ↓
                    ┌─────────────────┐
                    │     YOLOv8      │
                    │ Detection Engine│
                    └────────┬────────┘
                             ↓
              ┌────────────────────────────┐
              │ Detection Processing       │
              │ • Confidence               │
              │ • Deduplication             │
              │ • Severity Classification  │
              └─────────────┬──────────────┘
                            ↓
                    ┌───────────────┐
                    │   Dashboard   │
                    └───────┬───────┘
                            ↓
                    High Severity
                            ↓
             ┌──────────────┼──────────────┐
             ↓              ↓              ↓
           GPS          Snapshot        Alerts
             └──────────────┼──────────────┘
                            ↓
                     SQLite Database
                            ↓
                 Municipal Dashboard
                            ↓
              Review / Approve / Decline
                            ↓
                      PDF Reports
```

---

## 📊 Project Workflow

### 1️⃣ Start Inspection

A field operator starts an inspection session using a camera, video, or IP camera.

### 2️⃣ Detect Road Damage

The YOLOv8 model analyzes incoming frames and identifies potholes.

### 3️⃣ Process Detection

The system evaluates confidence and filters duplicate detections.

### 4️⃣ Classify Severity

Detected potholes are classified according to their severity.

### 5️⃣ Record Evidence

High-severity detections can trigger snapshot capture and GPS collection.

### 6️⃣ Store Data

Inspection information is stored using the local SQLite database.

### 7️⃣ Municipal Review

Authorities can review detections through the municipal dashboard.

### 8️⃣ Generate Reports

Approved detections can be included in PDF reports for further action.

---

## 📸 Screenshots

Project screenshots are available in the `screenshots/` folder.

> Add the actual screenshot filenames here after checking your folder.

---

## 📂 Project Structure

```text
IRIS/
│
├── database/
├── detector/
├── docs/
├── face_scan/
├── web/
├── arduino/
│
├── main.py
├── config.py
├── auth.py
├── gps.py
├── session_manager.py
├── vehicles.py
├── voice_alert.py
├── gemini_analyzer.py
├── arduino_controller.py
│
├── requirements.txt
├── Dockerfile
├── README.md
└── ...
```

---

## 🚀 Getting Started

### Clone the Project

```bash
git clone https://github.com/itsaddyon/IRIS.git
cd IRIS
```

### Create Virtual Environment

```bash
python -m venv .venv
```

### Activate Environment

**Windows:**

```bash
.venv\Scripts\activate
```

### Install Dependencies

```bash
pip install -r requirements.txt
```

### Start Application

```bash
python main.py
```

The application can then be accessed through the configured local dashboard.

---

## 🔐 Security

Sensitive information should never be committed to GitHub.

This includes:

* API keys
* Passwords
* Firebase service-account files
* `.env` files
* Private credentials
* Private biometric information

Use environment variables for sensitive configuration.

---

## 🔮 Future Scope

IRIS can be further enhanced with:

* 📱 Dedicated mobile application
* 🛰️ Improved GPS and road mapping
* 🏙️ City-wide road monitoring
* 📹 Multi-camera support
* 🧠 Improved AI models
* 📈 Predictive maintenance
* 🚨 Automated authority notifications
* ☁️ Scalable cloud infrastructure
* 🗺️ Road-condition heatmaps
* 📊 Long-term road-condition analytics
* 🧪 Automated testing and model evaluation

---

## 👥 Team Contribution

IRIS is developed as a **team project**.

### Project Lead

**Adarsh Arya**

GitHub:
https://github.com/itsaddyon

### Team Member

**Saumay Raj**

GitHub:
https://github.com/saumayraj621-sudo

### My Role

As a team member, my contribution to IRIS includes supporting the project's:

* Development
* Testing and debugging
* Documentation
* UI / presentation improvements
* Feature integration
* Project refinement

> This section should be updated with the exact modules/features personally contributed by each team member.

---

## 🌍 Vision

IRIS aims to transform traditional road inspection into an intelligent workflow:

```text
Detect → Locate → Classify → Review → Maintain
```

By combining **Artificial Intelligence, Computer Vision, GPS, dashboards, and analytics**, IRIS provides a foundation for smarter road infrastructure monitoring.

---

## ⭐ IRIS

### Smarter Roads. Faster Detection. Better Infrastructure.

---

## 📜 Project Information

**Project:** IRIS — Intelligent Road Inspection System
**Domain:** Artificial Intelligence & Machine Learning
**Focus:** Computer Vision & Smart Infrastructure
**Application:** Road Safety & Automated Inspection
**Development:** Team Project
