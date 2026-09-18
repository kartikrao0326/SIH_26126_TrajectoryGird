# 🚦 TrajGrid

### City-Wide AI Engine for Multi-Camera ANPR Trajectory Tracking and Urban Traffic Analytics

**Problem Statement ID:** SIH26127  
**Organization:** Bharat Electronics Limited (BEL)  
**Theme:** Smart Automation  
**Category:** Software

---

## 📌 Overview

TrajGrid is a multi-camera vehicle tracking and urban traffic analytics system designed to connect vehicle sightings from different ANPR/CCTV cameras into a single, ordered vehicle trajectory.

Traditional ANPR systems can identify a vehicle at an individual camera, but they do not automatically answer:

> **"Where did this vehicle go after leaving this camera?"**

TrajGrid solves this problem by collecting plate sightings from multiple cameras and linking them using:

- Vehicle number plate information
- Timestamp
- Camera location
- Road-network connectivity
- Physically plausible travel time
- Direction of travel

The same trajectory data is then used for traffic analytics and real-time alerts.

---

## 🎯 Problem Statement

City-wide ANPR and CCTV cameras operate independently.

Each camera can detect and read a vehicle's number plate, but there is usually no unified layer that can:

- Link the same vehicle across multiple cameras
- Reconstruct the vehicle's complete route
- Handle missed camera detections
- Detect physically impossible vehicle movements
- Calculate actual corridor travel time
- Generate real-time watchlist alerts
- Provide city-wide traffic analytics

TrajGrid acts as the linking and analytics layer between independent camera systems.

---

## 💡 Our Solution

TrajGrid follows a multi-stage pipeline:

```text
Camera
   ↓
Plate Detection
   ↓
OCR
   ↓
Format Validation & Repair
   ↓
Multi-Frame Voting
   ↓
Sighting Event
   ↓
Deduplication
   ↓
Trajectory Stitching
   ↓
Traffic Analytics
   ↓
Alerts
   ↓
Dashboard
