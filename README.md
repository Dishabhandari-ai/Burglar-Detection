# Burglar Detection using OpenCV

## Overview

This project implements a simple burglar detection system using OpenCV and frame differencing. The program analyzes a video feed, detects motion between frames, highlights suspicious movement with bounding boxes, and saves snapshots when motion is detected.

## Features

* Motion detection using frame differencing
* Conversion of frames to grayscale for efficient processing
* Detection of moving objects using contours
* Bounding box visualization around detected objects
* Automatic screenshot capture of detected intrusions
* Detection counter to track the number of events

## Technologies Used

* Python
* OpenCV (cv2)

## Project Workflow

1. Load the input video.
2. Convert each frame to grayscale.
3. Store a buffer of previous frames.
4. Compute the difference between frames separated by a fixed gap.
5. Apply thresholding to identify motion regions.
6. Find contours around moving objects.
7. Draw bounding boxes around detected movement.
8. Save images whenever a potential burglar is detected.

## Requirements

Install OpenCV:

```bash
pip install opencv-python
```

## Usage

1. Place the input video in the project directory.
2. Rename the video file as:

```text
theft.mp4
```

3. Run the program:

```bash
python burglar_detection.py
```

4. Press `q` to stop the program.

## Output

* Red bounding boxes around detected motion.
* "Burglar Detected!" alert message displayed on screen.
* Captured images saved as:

```text
burglar_1.jpg
burglar_2.jpg
burglar_3.jpg
...
```

## Parameters

| Parameter    | Value | Description                                    |
| ------------ | ----- | ---------------------------------------------- |
| gap          | 5     | Number of frames used for comparison           |
| threshold    | 30    | Pixel intensity threshold for motion detection |
| contour area | 500   | Minimum contour area considered as motion      |
| max captures | 100   | Maximum number of saved detection images       |


## Author

Disha Bhandari
