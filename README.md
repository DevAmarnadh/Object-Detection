Here's a shorter version of the README file:

# Object Detection and Tracking with YOLOv8 and OpenCV

## Prerequisites

- Python 3.6+
- OpenCV
- Ultralytics YOLO

## Installation

1. **Clone the Repository**
    ```bash
    git clone https://github.com/your-repository.git
    cd your-repository
    ```

2. **Install Dependencies**
    ```bash
    pip install opencv-python-headless ultralytics
    ```

3. **Download the YOLOv8 Model**
    - Place `yolov8n (2).pt` in the project directory.

## Usage

Run the following command to start the webcam and perform object detection and tracking:

```bash
python your_script_name.py
```

## Code Overview

1. **Import Libraries**
    ```python
    import cv2
    from ultralytics import YOLO
    ```

2. **Load YOLOv8 Model**
    ```python
    model = YOLO("yolov8n (2).pt")
    ```

3. **Open Webcam**
    ```python
    cap = cv2.VideoCapture(0)
    if not cap.isOpened():
        print("Error: Could not open webcam.")
        exit()
    ```

4. **Initialize Variables**
    ```python
    tracker = None
    initBB = None
    CONFIDENCE_THRESHOLD = 0.5
    ```

5. **Main Loop**
    - Capture frame, perform detection if not tracking, initialize tracker.
    - Update tracker if tracking, draw bounding box.
    - Display frame, exit on 'q' press.

6. **Cleanup**
    ```python
    cap.release()
    cv2.destroyAllWindows()
    ```

## Notes

- Adjust `CONFIDENCE_THRESHOLD` as needed.
- Ensure `yolov8n (2).pt` is in the working directory.

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.

---

This concise README provides the essential information to set up, run, and understand the project.
