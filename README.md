# Smart-Parking-Vision-YOLOv8
A hardware-free AI smart parking detection system built with YOLOv8 and custom OpenCV spatial geometry.
# 🚗 AI Smart Parking Management System

An automated, hardware-free parking detection system built using Deep Learning and Computer Vision. This project was developed as a working AI prototype to solve real-world parking congestion using standard CCTV/camera feeds.

## 🛠️ Tech Stack
* **Domain:** Artificial Intelligence & Machine Learning
* **Object Detection:** YOLOv8 (PyTorch)
* **Spatial Geometry Logic:** Custom OpenCV mathematics (`cv2.pointPolygonTest`)
* **Development Environment:** Google Colab (NVIDIA T4 GPU)

## 🧠 Pipeline Architecture
This system replaces expensive hardware sensors (like ultrasonic or infrared sensors) with a two-stage computer vision pipeline:

1. **Auto-Initialization:** The AI runs YOLOv8 on the initial video frame to detect parked vehicles and automatically maps their bounding boxes into a JSON polygon array.
2. **Geometric Inference:** For live video tracking, the system extracts the exact center coordinate (X, Y) of every detected vehicle. It then cross-references those coordinates with the mapped polygons using custom OpenCV intersection math to determine live spot availability in real-time.

## 📂 Repository Contents
* `smart_parking_yolov8.ipynb`: The core Python processing pipeline.
* `bounding_boxes.json`: The auto-generated polygon coordinates.
* `parking_video.mp4`: The raw input video footage.
* `smart_parking_output.mp4`: The final processed video demonstrating dynamic bounding boxes and live counting.

## 🚀 Phase 2 (Future Scope)
The next iteration of this project will extract the live `available_spots` data feed and push it to a cloud database to power a real-time web application, allowing drivers to check parking availability remotely from their phones.

---
**Developed by:** Anshita 
**Program:** B.Tech Computer Science (AI/ML) | COER University
