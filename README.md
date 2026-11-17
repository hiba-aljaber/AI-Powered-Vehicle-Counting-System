# AI-Powered Vehicle Counting System

An end-to-end vehicle detection, tracking, and counting platform combining computer vision, machine learning, backend services, and mobile application development.

The system uses **YOLOv8** for vehicle detection, multiple tracking algorithms for object tracking, **FastAPI** for backend communication, and **.NET MAUI** for mobile monitoring.

## Project Overview

The project consists of three integrated components:

| Component | Technology | Description |
|---|---|---|
| Vehicle Detection | Python, YOLOv8 | Detects vehicles in video streams |
| Tracking & Counting | DeepSORT, IOU-Kalman, SORT | Tracks vehicles and maintains object identities |
| Backend API | FastAPI, MySQL | Receives, stores, and broadcasts detection events |
| Mobile Application | C#, .NET MAUI | Displays vehicle information and statistics |

## System Architecture

1. A camera or video source provides input to the detection pipeline.
2. YOLOv8 identifies vehicles in each frame.
3. The selected tracking algorithm assigns and maintains vehicle IDs.
4. The counting component detects vehicles crossing predefined virtual lines.
5. Detection events are optionally transmitted to the backend through HTTP.
6. FastAPI stores the information in MySQL and broadcasts real-time updates through WebSockets.
7. The mobile application displays live vehicle information and historical statistics.

## Repository Structure

```text
AI-Powered-Vehicle-Counting-System/
│
├── AracSayar Detection/
│   └── Python-based vehicle detection,
│       tracking, and counting pipeline
│
├── API-AI-vehicle-project/
│   └── FastAPI backend and database integration
│
├── AracSayar Mobile/
│   └── .NET MAUI mobile application
│
└── README.md
```

## Technologies Used

**Machine Learning & Computer Vision**
- Python
- YOLOv8
- Ultralytics
- DeepSORT
- IOU-Kalman
- SORT
- OpenCV

**Backend Development**
- FastAPI
- REST API
- WebSockets
- MySQL

**Mobile Development**
- C#
- .NET MAUI

## Main Features

- Real-time vehicle detection.
- Multiple object-tracking algorithm options.
- Vehicle identification and tracking across video frames.
- Vehicle counting using virtual counting lines.
- Integration between the AI pipeline and backend API.
- Real-time event communication through WebSockets.
- Mobile monitoring and historical statistics.

## My Contribution

This project was developed collaboratively as a university team project.

My primary area of contribution was the **Machine Learning and Computer Vision component**, particularly the AI-based vehicle detection and tracking system.

The project is presented as a collaborative development effort, with individual contributions distinguished from the work of other team members.

## Running the Project

### Requirements

- Python 3.10 or later
- .NET 9 SDK
- MySQL
- Git

### 1. Vehicle Detection Pipeline

Navigate to the `AracSayar Detection` directory.

Create and activate a virtual environment:

```bash
python -m venv .venv
```

Windows:

```powershell
.venv\Scripts\Activate.ps1
```

Install dependencies:

```bash
pip install -r deep_sort/requirements.txt
pip install ultralytics
```

Run the detection pipeline:

```bash
python main.py --source testVideo.mp4 --display --tracker deepsort
```

Available tracker options include:

- `deepsort`
- `ioukalman`
- `sort`

### 2. Backend API

Navigate to the backend directory and install its dependencies:

```bash
pip install -r requirements.txt
```

Configure the MySQL database connection using the `DATABASE_URL` environment variable.

Start the FastAPI server:

```bash
uvicorn main:app --reload --port 8000
```

API documentation:

```text
http://localhost:8000/docs
```

### 3. Mobile Application

Navigate to the mobile application directory:

```bash
dotnet restore
dotnet build
```

Configure the backend URL before running the application on your selected platform.

## Future Improvements

Potential improvements include:
- Improving detection accuracy in challenging traffic conditions.
- Optimizing real-time processing performance.
- Expanding vehicle classification capabilities.
- Enhancing the mobile monitoring interface.

## Acknowledgements

Developed collaboratively as a university team project.

This repository is intended to showcase the project and the individual contributions made during its development.

