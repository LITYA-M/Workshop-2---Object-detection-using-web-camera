# Workshop-2---Object-detection-using-web-camera
# Objective

Perform real-time object detection using a trained YOLOv4 model through a laptop webcam.

# Technologies Used
1.Python
2.OpenCV
3.NumPy
4.Jupyter Notebook
5.YOLOv4
6.COCO Dataset
7.Environment
8.Anaconda
9.Conda environment: opencv
10.Python 3
11.OpenCV 4.10.0
12.Jupyter Notebook

# Program

Name : LITYA M Registration Number : 212225230152

```
%pip install ultralytics
from ultralytics import YOLO
import cv2
import matplotlib.pyplot as plt

model = YOLO("yolov8n.pt")

cap = cv2.VideoCapture(0)

ret, frame = cap.read()

if ret:
    results = model(frame, imgsz=320, conf=0.5, verbose=False)

    annotated = results[0].plot()
    annotated = cv2.cvtColor(annotated, cv2.COLOR_BGR2RGB)

    plt.figure(figsize=(10, 6))
    plt.imshow(annotated)
    plt.title("Real-Time Object Detection")
    plt.axis("off")
    plt.show()

cap.release()
```
## OUTPUT

<img width="811" height="673" alt="Screenshot 2026-09-16 123635" src="https://github.com/user-attachments/assets/40d3417b-889e-4fc1-8199-64ad844369df" />

## RESULT

The YOLOv4-based real-time object detection system was successfully implemented using OpenCV and a laptop webcam. The system successfully captured live video frames, detected objects using the trained YOLOv4 model, and displayed bounding boxes, object labels, and confidence scores for the detected objects.




















...








..










..














..



...
.






..
...
