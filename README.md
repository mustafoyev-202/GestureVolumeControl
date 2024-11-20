# 🖐️ Hand Gesture Volume Control

A Python-based computer vision project that allows you to control your system's volume using hand gestures. Using
MediaPipe for hand tracking, this application enables intuitive volume control through simple hand movements captured by
your webcam.

## ✨ Features

- Real-time hand tracking and gesture recognition
- Volume control using pinch gestures (thumb and index finger)
- Visual feedback with:
    - FPS counter
    - Volume percentage display
    - Volume level bar
    - Hand landmark visualization
    - Gesture tracking lines and points
- Smooth volume interpolation
- Support for multiple hand tracking

## 🛠️ Technologies Used

- Python 3.x
- OpenCV (cv2)
- MediaPipe
- NumPy
- pycaw (Windows Audio Control)
- Computer Vision and Machine Learning techniques

## 📋 Prerequisites

Before running this application, ensure you have the following installed:

```bash
pip install opencv-python
pip install mediapipe
pip install numpy
pip install pycaw
```

## 🚀 Getting Started

1. Clone this repository:

```bash
git clone <repository-url>
cd hand-gesture-volume-control
```

2. Run the main application:

```bash
python main.py
```

## 💻 How to Use

1. Run the application and position yourself in front of your webcam
2. Show your hand to the camera
3. Pinch your thumb and index finger together
4. Control volume by:
    - Increasing the distance between fingers to increase volume
    - Decreasing the distance between fingers to decrease volume
5. Visual feedback will show current volume level and hand tracking

## 🗂️ Project Structure

```
hand-gesture-volume-control/
│
├── main.py                    # Main application file
├── HandTrackingModule.py      # Hand tracking module
└── README.md                  # Project documentation
```

## 📝 Code Components

### HandTrackingModule.py

- `handDetector` class with methods:
    - `findHands()`: Detects and draws hand landmarks
    - `findPosition()`: Finds position of hand landmarks
    - `fingersUp()`: Detects raised fingers
    - `findDistance()`: Calculates distance between points

### main.py

- Initializes video capture and audio control
- Implements volume control logic
- Provides visual feedback and UI elements

## ⚙️ Customization

You can modify various parameters in the code:

- `detectionCon`: Hand detection confidence threshold
- `maxHands`: Maximum number of hands to detect
- Volume range interpolation values
- UI element positions and colors

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📜 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🔍 Troubleshooting

Common issues and solutions:

1. **No webcam detected**: Ensure your webcam is properly connected and not in use by another application
2. **Audio control not working**: Check if pycaw is properly installed and you have necessary permissions
3. **Low FPS**: Reduce the camera resolution or detector confidence threshold

## 🙏 Acknowledgments

- MediaPipe team for their hand tracking solution
- OpenCV community for computer vision tools
- pycaw developers for Windows audio control functionality

## ⚠️ Note

This project currently supports Windows for volume control functionality. For other operating systems, you'll need to
modify the audio control implementation accordingly.