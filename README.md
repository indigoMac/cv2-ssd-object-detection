# Real-time Object Detection with MobileNet SSD
## Overview
This repository contains a Python script for real-time object detection using a pre-trained MobileNet SSD model implemented with OpenCV. The MobileNet SSD (Single Shot MultiBox Detector) is a deep learning model that has been trained to detect objects in images efficiently. This model is designed for mobile and edge devices, prioritizing speed and efficiency while maintaining competitive accuracy. Our implementation processes video input to detect and label predefined objects in real time.

## MobileNet SSD
MobileNet SSD is an architecture that combines a streamlined deep neural network, MobileNet, with a Single Shot Detector (SSD) framework. The model detects objects by evaluating a single deep neural network pass, making it faster than systems that apply detectors or classifiers at different region proposals. Here's a brief rundown of the technology and method:

- MobileNet: Uses depthwise separable convolutions to build a lightweight deep neural network.
- SSD: Predicts bounding boxes and class probabilities in a single pass, reducing computational demand.

This combination allows for running object detection in real-time on less powerful devices, such as mobile phones or single-board computers.

## Features
- Real-time Video Processing: The script processes an input video file, detects objects frame by frame, and annotates the frames with bounding boxes and labels.
- Output Display and Saving: Processed video can be viewed in real-time and saved to a specified output file.
- GPU Acceleration Support: If available, the script can leverage GPU acceleration to improve performance, configurable through a simple script flag.

## Requirements
- Python 3.6+
- OpenCV 4.x (cv2)
- NumPy

## Installation
To run this script, you will need to install the required Python libraries. You can install these using pip:

```bash
pip install numpy opencv-python
```
## Usage

1. Set Up Your Environment: Ensure that the required files (MobileNetSSD_deploy.prototxt, MobileNetSSD_deploy.caffemodel, and the input video file funny_dog.mp4) are in the project directory or specify their paths in the script.

2. Configure the Script: You can modify the GPU_SUPPORT flag in the script to enable or disable GPU processing.

3. Run the Script: Execute the script with Python.
```bash
   python object_detection.py
```
4. Output: The script will display the video in a window and save the output in the specified file. Press 'q' to quit the video window.

## File Descriptions
- 'object_detection.py': The main Python script for object detection.
- 'MobileNetSSD_deploy.prototxt': Configuration file that describes the network architecture.
- 'MobileNetSSD_deploy.caffemodel': Pre-trained model weights.

## Contributions

This is a simple project to make use of open-cv and I have other projects that also use SSD for object detection using Pytorch and Tensorflow, so this is really just for a quick example of how good it is. However, Contributions to this project are of course welcome. Please consider the following ways to contribute:

- Enhancing performance
- Adding additional features
- Improving the robustness and error handling
- For major changes, please open an issue first to discuss what you would like to change.

## License
This project is licensed under the MIT License.
