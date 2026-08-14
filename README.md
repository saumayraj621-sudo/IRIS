# 🚧 IRIS — Intelligent Road Inspection System

> **AI-powered road inspection and pothole detection system for smarter, faster, and data-driven road maintenance.**

**Detect • Classify • Locate • Review • Improve**

---

## 📌 About IRIS

**IRIS (Intelligent Road Inspection System)** is an AI-powered road monitoring and inspection platform designed to automate pothole detection and improve road-maintenance workflows.

The system uses computer vision and **YOLOv8** to identify road damage, classify its severity, reduce duplicate detections, capture GPS-tagged inspection events, and present useful information through an operations dashboard.

IRIS combines **AI, computer vision, GPS data, backend processing, and dashboard-based visualization** to support faster and more organized road inspection.

---

## 🎯 Problem Statement

Traditional road inspection can be:

- Manual and time-consuming
- Difficult to scale across large road networks
- Dependent on periodic physical surveys
- Difficult to monitor continuously
- Challenging to prioritize based on severity and location

IRIS aims to provide a more automated and data-driven approach to road-condition monitoring.

---

## 🚀 Key Features

### 🤖 AI-Powered Pothole Detection

- YOLOv8-based object detection
- Real-time road inspection
- Detection confidence tracking
- Pothole severity classification
- Duplicate detection handling using IoU

### 📍 GPS-Based Inspection

- GPS-tagged road events
- Location-aware detection records
- Road inspection mapping
- Location-based review and analysis

### 📊 Operations Dashboard

- Inspection session overview
- Detection statistics
- Pothole review interface
- Severity information
- Inspection data visualization
- Dashboard-based monitoring

### 🗺️ GIS & Road Visualization

- Pothole locations on maps
- Road inspection visualization
- Location-based analysis
- Visual representation of detected road issues

### 📄 Reporting

- Inspection records
- Detection information
- Report generation
- PDF reporting support

### 🔧 Hardware Integration

The project also supports a physical inspection setup involving camera-based road monitoring and an Arduino-based alert mechanism for high-severity detections.

---

## 🎨 My Contribution — Frontend & Dashboard

I contributed to IRIS as a **team member**, with my primary focus on **Frontend Development and Dashboard implementation**.

### Frontend Development

- Worked on the user-facing interface
- Improved frontend layout and presentation
- Worked on interface components
- Improved usability and visual organization
- Supported integration of frontend components with project functionality

### Dashboard Development

- Worked on the operations dashboard interface
- Organized inspection and detection information
- Improved dashboard presentation
- Worked on data visualization and monitoring views
- Supported the presentation of road-inspection information

### Relevant Code

My primary contribution is represented in the `web/` directory:

```text
web/
├── static/
├── templates/
├── __init__.py
├── app.py
├── index.html
└── report.py
---

## 🔄 System Workflow

Camera / Video Feed
        ↓
YOLOv8 Detection
        ↓
Pothole Identification
        ↓
Severity Classification
        ↓
Duplicate Detection Handling
        ↓
GPS / Inspection Data
        ↓
Flask Backend
        ↓
Operations Dashboard
        ↓
Review & Reporting

---

## 🏗️ System Architecture

```text
┌──────────────────────┐
│   Camera / Video     │
└──────────┬───────────┘
           ↓
┌──────────────────────┐
│       YOLOv8         │
│   Object Detection   │
└──────────┬───────────┘
           ↓
┌──────────────────────┐
│ Severity + IoU       │
│     Processing       │
└──────────┬───────────┘
           ↓
┌──────────────────────┐
│ GPS / Inspection     │
│       Data           │
└──────────┬───────────┘
           ↓
┌──────────────────────┐
│    Flask Backend     │
└──────────┬───────────┘
           ↓
┌──────────────────────┐
│ Operations Dashboard │
└──────────┬───────────┘
           ↓
┌──────────────────────┐
│  Review & Reporting  │
└──────────────────────┘
