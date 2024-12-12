# invisbilitycloak

## A Harry Potter Inspired Project

# Invisible Cloak Effect

This project demonstrates the "invisible cloak" effect using OpenCV, inspired by the magical invisibility cloaks from fictional worlds. The program replaces a user-defined color in the video feed with a pre-captured background, creating the illusion of invisibility.

# Features

1. Captures the background from the webcam.

2. Detects a specific color (default: blue) in the video feed.

3. Replaces the detected color region with the pre-captured background.

4. Real-time processing using OpenCV.

# Requirements

Python 3.6+

OpenCV 4.x

NumPy

# Installation

Clone the repository or download the script.

Install the required Python libraries:

'''pip install opencv-python numpy'''

# How to Run

Connect a webcam to your computer.

Run the script:

'''python invisbilitycloak/main.py'''

Let the camera capture just the background first.

Use a blue cloth to see the invisibility effect.

Press q to exit the program.

# Configuration

1. Change Cloak Color

To change the color of the cloak, modify the lower_blue and upper_blue variables in the script:
'''
lower_blue = np.array([90, 50, 50])
upper_blue = np.array([130, 255, 255])
'''

Replace these values with the HSV range of your desired color.

2. Adjust Background Capture

You can adjust the number of frames used for background capture by modifying the num_frames parameter in the create_background function.

# Code Overview

create_background: Captures multiple frames to calculate the background using the median.

create_mask: Generates a mask to isolate the specified color.

apply_cloak_effect: Combines the current frame and background to create the invisibility effect.

main: Handles the main program flow, including capturing video frames and applying the cloak effect.

# Controls

q: Quit the program.

# Known Issues

The effect may not work well under poor lighting conditions.

Colors similar to the cloak color may also be replaced.

# Future Improvements

1. Add support for dynamic color selection via a GUI.

2. Optimize the performance for smoother real-time processing.

3. Improve color detection with advanced filtering techniques.


