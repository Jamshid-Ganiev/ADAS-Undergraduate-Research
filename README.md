# ADAS-Undergraduate-Research
Lane detection, steering control, obstacle recognition, and traffic sign detection.

## Project Description & Objective
This project showcases a lane detection system for vehicles with front-facing cameras, a crucial part of advanced driver assistance systems (ADAS) in autonomous and semi-autonomous vehicles. It detects lanes, measures curve radius, and monitors center offset, enhancing safety and comfort. The repository provides dashcam footage for testing and development.


## Get This Project Up and Running

## Setting up a Python Virtual Environment for "ADAS-Undergraduate-Research"

To maintain a clean and isolated Python environment for your "ADAS-Undergraduate-Research" project, follow these steps in your terminal:

## Navigate to the Project Directory
cd ADAS-Undergraduate-Research/

## Create a Virtual Environment

```
python -m venv venv
```

## Activate the Virtual Environment
### On Windows:

```
.\<env_name>\Scripts\activate
```

## On macOS and Linux:
```
source venv/bin/activate
```

## Install Project Dependencies from requirements.txt
```
pip install -r requirements.txt
```

This project follows a simplistic approach in terms of how to run it. Only 2 files are needed in order to get it running.
* [laneDetection](laneDetection.py) is the only file to perform image processing nad detecting lanes
* [drive](drive.mp4) is the video file on which image processing is performed.

Simply clone this repository to desired path by launching command prompt and running
```
https://github.com/Jamshid-Ganiev/ADAS-Undergraduate-Research
```
Make sure both files (laneDetection.py & drive.mp4) are in the same directory.

## How the Code Works

The Python script `laneDetection.py` processes a provided dashcam footage of a car cruising on the highway. The code follows a modular approach with several functions for lane detection.

### Image Processing

- **readVideo()**: Reads the video file `drive.mp4` from the same directory.

- **processImage()**: Applies HLS color filtering, grayscale conversion, thresholding, blurring, and edge extraction to isolate white lane lines.

- **perspectiveWarp()**: Performs a perspective warp by defining 4 points around the lane area, creating a bird's-eye view for accurate lane curvature detection. Note that the warp parameters may need adjustment for different camera angles or videos.


