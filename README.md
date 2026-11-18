
# AI-Powered Vehicle Counting System

An AI-powered vehicle detection, tracking, and counting system designed to analyze traffic videos and camera streams.

## Project Overview

This project uses computer vision techniques to detect vehicles, track their movement, assign tracking IDs, and count vehicles crossing predefined counting lines.

The project was developed as part of a university team project.

## Key Features

- Vehicle detection using YOLOv8.
- Vehicle tracking using tracking algorithms, including DeepSORT, SORT, and IoU with Kalman filtering.
- Unique IDs assigned to detected vehicles.
- Vehicle counting using configurable counting lines.
- Support for video files and camera input.
- Backend communication through FastAPI.
- REST API and WebSocket communication.
- MySQL database integration.
- Mobile application developed using .NET MAUI.

## Technologies Used

**Computer Vision and AI**
- Python
- YOLOv8
- OpenCV
- DeepSORT
- SORT
- Kalman Filtering

**Backend and Database**
- FastAPI
- REST API
- WebSocket
- MySQL

**Mobile Development**
- .NET MAUI

## System Architecture

The system combines vehicle detection and tracking with backend services and a mobile application.

1. Video or camera input is processed.
2. YOLOv8 detects vehicles.
3. Tracking algorithms associate detections across frames.
4. Vehicles receive tracking IDs and are counted when crossing configured lines.
5. The backend communicates system information to the application.

## Project Structure

The repository contains the vehicle detection application and its related backend/mobile application components.

## Installation and Usage

Please refer to the installation instructions and requirements in the individual project directories.

## Team Project

This project was developed collaboratively as a university group project.

**My contribution:** [Add your actual responsibilities here.]

## Future Improvements

- Improve vehicle tracking consistency.
- Enhance detection performance under different traffic and lighting conditions.
- Improve system performance for real-time processing.
- Expand application monitoring and reporting features.
