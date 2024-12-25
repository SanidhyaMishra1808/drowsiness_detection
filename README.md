# Drowsiness Detection

This project is a drowsiness detection system that uses a webcam to monitor the user's eye aspect ratio (EAR) and trigger an alarm if the user's eyes remain closed for a certain number of consecutive frames, indicating potential drowsiness.

## Features

- Real-time eye aspect ratio calculation
- Drowsiness detection based on EAR
- Audible alarm when drowsiness is detected
- Customizable detection parameters
- High-resolution video capture

## Requirements

- Python 3.x
- OpenCV
- face_recognition
- scipy
- numpy
- pygame

## Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/SanidhyaMishra1808/drowsiness_detection.git
    cd drowsiness_detection
    ```

2. Install the required Python packages:
    ```bash
    pip install opencv-python face_recognition scipy numpy pygame
    ```

## Usage

1. Navigate to the project directory:
    ```powershell
    cd E:\python
    ```

2. Run the drowsiness detection script:
    ```powershell
    python drowsiness_detection.py
    ```

## Customization

You can customize the following parameters in the `drowsiness_detection.py` script:

- `MIN_AER`: Minimum eye aspect ratio to indicate drowsiness.
- `EYE_AR_CONSEC_FRAMES`: Number of consecutive frames the EAR must be below `MIN_AER` to trigger the alarm.

Additionally, you can change the video capture resolution by modifying these lines:
```python
video_capture.set(3, 1280)  # Set width to 1280
video_capture.set(4, 720)   # Set height to 720
```

Script Explanation
main()
Initialization:

Initializes Pygame for playing alarm sounds.
Sets up the video capture with a resolution of 1280x720.
Frame Processing Loop:

Captures frames from the webcam.
Detects facial landmarks using the face_recognition library.
Calculates the EAR for both eyes.
Draws polygons around the detected eyes.
Checks if the EAR is below the minimum threshold (MIN_AER) for a certain number of consecutive frames (EYE_AR_CONSEC_FRAMES).
If drowsiness is detected, an alarm is triggered.
Displays the EAR and alert status on the frame.
Exit Condition:

Stops the video capture and closes all windows when 'q' is pressed.
License
This project is licensed under the MIT License. See the LICENSE file for details.

Acknowledgments
OpenCV
face_recognition
scipy
numpy
pygame
vbnet
Copy code
