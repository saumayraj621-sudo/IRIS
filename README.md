# 🚧 IRIS — Intelligent Road Inspection System

> **AI-powered road inspection and pothole detection system for smarter, faster, and data-driven road maintenance.**

[![AI](https://img.shields.io/badge/AI-YOLOv8-blue)]()
[![Python](https://img.shields.io/badge/Python-3.11+-yellow)]()
[![Computer Vision](https://img.shields.io/badge/Computer%20Vision-OpenCV-green)]()
[![Backend](https://img.shields.io/badge/Backend-Flask-red)]()
[![Database](https://img.shields.io/badge/Database-SQLite-lightgrey)]()

---

## 📌 About IRIS

**IRIS (Intelligent Road Inspection System)** is an AI-powered road monitoring and inspection platform designed to automate pothole detection and improve road-maintenance workflows.

The system uses a live camera, video input, and **YOLOv8-based computer vision** to detect potholes in real time. Detected incidents can be classified by severity, stored with supporting information, and reviewed through a municipal dashboard.

IRIS is designed to connect **field-level road inspection with municipal decision-making**.

---

## 🎯 Problem Statement

Traditional road inspection often depends heavily on manual surveys.

This can lead to:

* ⏳ Slow inspection processes
* 👷 High dependence on manual effort
* 📍 Difficulty tracking exact locations
* 📊 Poorly structured inspection data
* 🚧 Delayed identification of serious road damage
* 💰 Increased maintenance costs

### Our Goal

Use **Artificial Intelligence + Computer Vision + Location Data + Analytics** to make road inspection faster and more systematic.

---

## 💡 How IRIS Works

```text
Camera / Video / IP Camera
            ↓
      YOLOv8 Detection
            ↓
     Pothole Detection
            ↓
   Duplicate Detection Check
            ↓
   Severity Classification
            ↓
 ┌──────────┴──────────┐
 ↓                     ↓
Dashboard         High Severity
                       ↓
              Snapshot + GPS
                       ↓
              Data Persistence
                       ↓
             Municipal Dashboard
                       ↓
          Review / Approve / Decline
                       ↓
                 Reports
```

---

## ✨ Key Features

### 🤖 AI-Powered Detection

* Real-time pothole detection
* YOLOv8-based object detection
* Computer vision processing using OpenCV
* Detection confidence tracking
* Duplicate detection handling

### 🚧 Severity Classification

Detected road damage can be categorized into:

* 🟢 Low
* 🟡 Medium
* 🔴 High

High-severity incidents can receive additional processing and evidence capture.

### 📍 GPS-Based Inspection

The system can optionally capture location information for detected road incidents.

This helps authorities understand **where road damage is occurring**.

### 📊 Driver Dashboard

The field/driver dashboard provides:

* Live camera feed
* Inspection session controls
* Detection counters
* Detection information
* Charts and analytics
* Alert states

### 🏛️ Municipal Dashboard

The municipal interface allows authorized reviewers to:

* Review high-severity detections
* Approve incidents
* Decline incidents
* View locations on a map
* Generate reports

### 💾 Data Management

IRIS uses **SQLite** for local persistence of inspection sessions, detections, approval status, and related metadata.

### 🔔 Alert System

The system can optionally provide:

* Voice alerts
* Arduino LED/buzzer alerts
* High-severity notifications

### 🧠 Optional AI Analysis

Google Gemini can optionally be integrated for additional incident analysis and prioritization.

### ☁️ Optional Cloud Integration

Firebase/Firestore support can be used for cloud-backed data synchronization.

---

## 🧠 AI / ML Pipeline

```text
Road Image / Video
        ↓
Image Processing
        ↓
YOLOv8 Model
        ↓
Pothole Detection
        ↓
Confidence Evaluation
        ↓
Duplicate Filtering
        ↓
Severity Classification
        ↓
Incident Storage
```

---

## 🛠️ Technology Stack

| Category                | Technology              |
| ----------------------- | ----------------------- |
| Programming             | Python                  |
| AI / Object Detection   | YOLOv8 / Ultralytics    |
| Computer Vision         | OpenCV                  |
| Backend                 | Flask                   |
| Real-Time Communication | Flask-SocketIO          |
| Database                | SQLite                  |
| Frontend                | HTML, CSS, JavaScript   |
| Charts                  | Chart.js                |
| Maps                    | Leaflet + OpenStreetMap |
| Reports                 | ReportLab               |
| GPS                     | Windows Location API    |
| Hardware                | Arduino + PySerial      |
| Voice Alerts            | pyttsx3                 |
| Optional AI             | Google Gemini           |
| Optional Cloud          | Firebase / Firestore    |
| Version Control         | Git + GitHub            |

---

## 🏗️ System Architecture

```text
                   CAMERA / VIDEO
                         │
                         ▼
                 ┌───────────────┐
                 │    YOLOv8     │
                 │ Detection     │
                 └───────┬───────┘
                         │
                         ▼
              ┌─────────────────────┐
              │ Detection Processing │
              │ + Deduplication      │
              │ + Severity           │
              └──────────┬──────────┘
                         │
              ┌──────────┴──────────┐
              ▼                     ▼
       DRIVER DASHBOARD       HIGH SEVERITY
                                    │
                    ┌───────────────┼───────────────┐
                    ▼               ▼               ▼
                 Snapshot          GPS          Alerts
                    │               │               │
                    └───────────────┼───────────────┘
                                    ▼
                              SQLite Storage
                                    │
                                    ▼
                         MUNICIPAL DASHBOARD
                                    │
                    ┌───────────────┼───────────────┐
                    ▼               ▼               ▼
                 Review           Map            Reports
                    │
              Approve / Decline
```

---

## 📸 Project Screenshots

Screenshots from the project are available in the [`screenshots`](screenshots) folder.

### 🚗 Driver Dashboard

![Driver Dashboard](screenshots/driver-dashboard.png)

### 🏛️ Municipal Dashboard

![Municipal Dashboard](screenshots/municipal-dashboard.png)

### 🚧 Pothole Detection

![Pothole Detection](screenshots/pothole-detection.png)

> Replace the filenames above with the **actual filenames** inside your `screenshots` folder.

---

## 👨‍💻 My Role

### Team Member

I am contributing to the **IRIS team project** as a team member.

My contribution areas include:

* 💻 Development and implementation support
* 🧪 Testing and debugging
* 📚 Project documentation
* 🖥️ Interface / presentation improvements
* 🔧 Feature integration and project refinement

> **Note:** Update this section with your exact contribution before publishing. Do not claim features that you did not personally work on.

---

## 👥 Team

### Project Lead

**Adarsh Arya**

Repository:
https://github.com/itsaddyon/IRIS

### Team Member

**Saumay Raj**

Repository:
https://github.com/saumayraj621-sudo

---

## 📂 Project Structure

```text
IRIS/
│
├── .github/
├── arduino/
├── database/
├── detector/
├── docs/
├── face_scan/
├── web/
│
├── auth.py
├── config.py
├── gps.py
├── main.py
├── vehicles.py
├── voice_alert.py
├── gemini_analyzer.py
│
├── requirements.txt
├── Dockerfile
├── firebase.json
├── README.md
└── ...
```

---

## 🚀 Installation

### 1. Clone the repository

```bash
git clone https://github.com/itsaddyon/IRIS.git
cd IRIS
```

### 2. Create a virtual environment

```bash
python -m venv .venv
```

### 3. Activate the environment

**Windows:**

```bash
.venv\Scripts\activate
```

### 4. Install dependencies

```bash
pip install -r requirements.txt
```

### 5. Configure the required environment variables

Keep API keys, passwords, service-account credentials, and other secrets outside the public repository.

### 6. Start the application

Follow the project's current setup instructions and configuration requirements.

---

## 🔐 Security

IRIS keeps sensitive credentials outside the public repository.

Examples include:

* API keys
* Secret keys
* Database credentials
* Firebase service-account credentials
* Administrative passwords

Never commit real credentials to GitHub.

---

## 🔮 Future Scope

IRIS can be further improved through:

* 📱 Dedicated mobile application
* 🛰️ More accurate GPS-based road mapping
* 🏙️ City-wide road-condition monitoring
* 📹 Multiple-camera integration
* 🧠 Improved detection models
* 📈 Predictive road-maintenance analytics
* 🚨 Automated authority notifications
* ☁️ Scalable cloud infrastructure
* 🗺️ Road-condition heatmaps
* 📊 Long-term infrastructure analytics

---

## 🌍 Impact

IRIS aims to support a shift from:

**Manual Inspection → Intelligent Inspection**

By combining AI, computer vision, location information, and digital dashboards, the system can help create a more structured approach to identifying and managing road damage.

---

## ⭐ Project Vision

> **Detect earlier. Locate accurately. Respond faster.**

IRIS aims to make road inspection more intelligent, scalable, and data-driven.

---

## 📜 Project Information

**Project:** IRIS — Intelligent Road Inspection System
**Domain:** Artificial Intelligence / Machine Learning / Computer Vision
**Application:** Smart Infrastructure & Road Safety
**Development:** Team Project
