Gesture Tracking Tool – Short README

*Overview*

This Python application uses MediaPipe to detect and track hand landmarks from a webcam feed. A Kivy-based GUI allows you to start and stop video capture and displays live hand-landmark overlays in real time.


*Features*

Hand Detection & Tracking: Uses MediaPipe’s Hands solution to detect landmarks on one or multiple hands.
Live Video Feed: Captures frames from your chosen webcam and overlays detected landmarks.

Clone or download this repository.

Install dependencies:
python -m venv venvname
./venv/source/activate 
OR 
./venv/bin/activate

pip install -r requirements.txt

Usage:

Run the script with optional command-line arguments for camera index and confidence thresholds:

python gestures.py \
    --camera-index 1 \
    --detection-confidence 0.7 \
    --tracking-confidence 0.7
--camera-index: Which camera to use (default = 0).
--detection-confidence: Minimum confidence threshold for hand detection (default = 0.5).
--tracking-confidence: Minimum confidence threshold for landmark tracking (default = 0.5).

How It Works

Initialization: A GestureTracker object opens the specified webcam and initializes the MediaPipe Hands module.

Processing: Each frame is converted from BGR to RGB, passed to MediaPipe for landmark detection, and updated in the GUI.

UI Controls:
Start: Begins live detection from the camera.
Stop: Releases resources and halts the video feed.

Contributing

Feel free to fork this project and open pull requests with improvements or additional gesture classification logic.

License

Distributed under the MIT License. See LICENSE file for more information.#   




g e s t u r e 
 
 
