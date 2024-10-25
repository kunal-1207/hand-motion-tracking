## Hand Tracking Program using OpenCV and MediaPipe

#### Overview:
This program implements real-time hand tracking using OpenCV and MediaPipe. It captures live video feed from a webcam, detects up to two hands, and displays the hand landmarks with connections in real time. The program is designed to provide developers and researchers with a simple, extensible base for creating applications involving hand gesture recognition, movement analysis, and other interactive hand-based controls.
## Features

- Real-time Hand Detection: Detects up to two hands in the camera feed, drawing landmarks and connections.
- Landmark Extraction: Outputs the X and Y coordinates for each hand landmark for further processing or analysis.
- Selfie Mode: The camera feed is flipped horizontally for a selfie-style view.
- Customizable Parameters: Easily adjust the maximum number of hands, detection confidence, and tracking confidence in the configuration.

## Requirement

This program is built with the following dependencies:
- Python 3.x
- OpenCV for Python (cv2)
- MediaPipe (mediapipe)

To install the dependencies, you can use the following command:

pip install opencv-python mediapipe

## Installation

1. Clone the repository and navigate to the project directory.


2. Run the program using::
 python hand_tracking.py



3. Interactive Controls:
- Press 'q' to quit the program.

    
## Code Overview 

1. Initialization: Sets up MediaPipe's Hand solution with configurations for detecting and tracking up to two hands.
2. Video Capture: Captures frames from the webcam, flips them horizontally, and converts them to RGB for processing.
3. Hand Detection: Detects hand landmarks using MediaPipe and draws them on the frame.
4. Landmark Extraction: Outputs the coordinates of each landmark for potential debugging or further customization.
5. Display: Shows the processed frames with landmark drawings.
## Example code Snippet

#### Initialize MediaPipe Hands

    mp_hands = mp.solutions.hands
    hands = mp_hands.Hands(
    max_num_hands=2,
    min_detection_confidence=0.7,
    min_tracking_confidence=0.7)
#### Initialize webcam and start capturing video
    cap = cv2.VideoCapture(0)

## Troubleshooting 

- No Camera Detected: Ensure your camera is enabled and properly connected. You may need to change the camera index in cv2.VideoCapture(0).
- Empty Frames: If you see the "Ignoring empty camera frame" message frequently, try adjusting the camera resolution or testing with another camera.
## Contribution

Feel free to fork this repository, suggest improvements, and submit pull requests for features or bug fixes.


## License

[MIT](https://choosealicense.com/licenses/mit/)

