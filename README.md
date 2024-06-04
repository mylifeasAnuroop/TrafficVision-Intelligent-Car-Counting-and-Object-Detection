# TrafficVision-Intelligent-Car-Counting-and-Object-Detection

**Author:** Anuroop Arya

## Overview

TrafficVision is an intelligent car counting and object detection system that leverages the YOLOv8 model for real-time traffic monitoring. This project aims to accurately count the number of cars crossing a specific line in a video feed, providing valuable data for traffic analysis and management.

## Approach

The project utilizes a pre-trained YOLOv8 model to detect and track objects in a video stream. The main features of the project include:

1. **Object Detection:** Using YOLOv8 to identify vehicles in the video.
2. **Object Tracking:** Tracking the movement of vehicles across frames.
3. **Line Crossing Detection:** Counting vehicles that cross a specified line.
4. **Annotated Output:** Producing a video with annotated frames showing detected vehicles, the tracking history, and the count of vehicles that have crossed the line.

## Tools and Technologies

- **Programming Languages:**
  - Python

- **Libraries and Frameworks:**
  - [Ultralytics YOLO](https://github.com/ultralytics/yolov8): For object detection and tracking.
  - [OpenCV](https://opencv.org/): For video processing and handling.

- **Environment:**
  - Google Colab (for development and testing)
  - TPU (if available) or CPU for computation

## Installation

To set up the project, run the following command to install the necessary libraries:

```bash
pip install ultralytics supervision opencv-python-headless
```

## Methodology

1. **Model Loading:** Load the pre-trained YOLOv8 model.
2. **Video Processing:** Capture frames from the video input.
3. **Object Detection and Tracking:** Detect objects in each frame and track their movement.
4. **Line Crossing Detection:** Track the history of object positions and detect when they cross a predefined line.
5. **Annotation:** Annotate the frames with bounding boxes, tracking history, and the count of crossed vehicles.
6. **Output Generation:** Write the annotated frames to an output video file.

## Pipeline

1. **Setup:**
   - Import required libraries.
   - Define line coordinates for vehicle counting.
   - Initialize video capture and output settings.

2. **Processing Loop:**
   - For each frame in the video:
     - Apply YOLOv8 model to detect and track vehicles.
     - Update the tracking history for each detected vehicle.
     - Check for line crossing and update the count.
     - Annotate the frame with detection results and the vehicle count.
     - Write the annotated frame to the output video.

3. **Finalization:**
   - Release video capture and output resources.

## Usage

To use the TrafficVision system, follow these steps:

1. Ensure you have the required libraries installed.
2. Place your video file in the specified path (e.g., `/content/d.mp4`).
3. Run the provided Python script.
4. The annotated output video will be saved as `output_single_line.mp4`.

## Real-World Applications

TrafficVision can be used in various real-world scenarios, including:

- **Traffic Monitoring:** Real-time monitoring and analysis of traffic flow.
- **Smart Traffic Management:** Enhancing traffic signal control systems.
- **Urban Planning:** Providing data for infrastructure development and planning.
- **Security and Surveillance:** Monitoring vehicles in restricted areas.

---

By implementing TrafficVision, you can gain valuable insights into traffic patterns and improve traffic management strategies.
