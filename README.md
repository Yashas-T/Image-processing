# Virtual V-0: Gesture Control System

A Python-based gesture control system that allows you to control your computer using hand gestures and eye blinks. This application combines hand tracking, face tracking, and audio control to create an intuitive interface for computer interaction.

## Features

- *Mouse Control*: Control mouse cursor using your index finger
- *Click Detection*: Perform clicks by blinking your eyes
- *Scrolling*: Scroll up/down using hand gestures
- *Volume Control*: Adjust system volume using hand gestures
- *Smooth Tracking*: Implemented smoothing for precise control
- *Real-time Feedback*: Visual feedback for gesture recognition
- *Gesture Recognition*: Advanced hand and face tracking using MediaPipe
- *Customizable Settings*: Adjustable parameters for sensitivity and control

## Requirements

- Python 3.7-3.10
- Webcam (720p or higher recommended)
- Windows OS (for audio control features)
- Minimum 4GB RAM
- DirectX 11 compatible graphics card

## Installation

1. Clone this repository or download the source code
2. Create a virtual environment (recommended):
bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

3. Install the required dependencies:
bash
pip install -r requirements.txt


## Usage

1. Run the application:
bash
python G_ESTERS_V-0.py


2. *Hand Gestures*:
   - Use your right index finger to control the mouse cursor
   - Show all fingers up to scroll up
   - Show all fingers down to scroll down
   - Keep your hand in the green zone (indicated on screen) for click detection

3. *Eye Control*:
   - Blink your eyes to perform clicks (when hand is in the click zone)
   - The system will show your eye aspect ratio (EAR) on screen

4. *Volume Control*:
   - Use your left hand to control system volume
   - Show 2 fingers to activate volume control
   - Adjust volume by moving your index finger up/down

5. To exit the application, press 'q' or close the window

## Controls Summary

- *Right Hand*:
  - Index finger: Mouse movement
  - All fingers up: Scroll up
  - All fingers down: Scroll down
  - Hand in green zone + blink: Click

- *Left Hand*:
  - Two fingers up: Volume control
  - Index finger movement: Adjust volume

## Technical Details

- Uses MediaPipe for hand and face tracking
- OpenCV for camera handling and visual feedback
- PyAutoGUI for mouse control
- PyCAW for Windows audio control
- Implements smoothing for stable cursor movement
- Includes cooldown periods for gesture recognition

### Key Parameters

- *Hand Tracking*:
  - Detection Confidence: 0.7
  - Tracking Confidence: 0.7
  - Maximum Hands: 2

- *Face Tracking*:
  - Detection Confidence: 0.5
  - Tracking Confidence: 0.5
  - Maximum Faces: 1

- *Gesture Settings*:
  - Blink Threshold: 0.25
  - Minimum Blink Interval: 0.3 seconds
  - Scroll Cooldown: 0.2 seconds
  - Scroll Amount: 50 pixels

## Development Setup

1. *IDE Setup*:
   - Recommended: VS Code or PyCharm
   - Install Python extension
   - Configure virtual environment

2. *Debugging*:
   - Enable debug mode in IDE
   - Set breakpoints in gesture detection functions
   - Monitor frame rate and performance

3. *Testing*:
   - Test in different lighting conditions
   - Verify gesture recognition accuracy
   - Check system resource usage

## Troubleshooting

### Common Issues

1. *Camera Not Detected*:
   - Check camera permissions
   - Verify camera is properly connected
   - Try different camera index in code

2. *Gesture Recognition Issues*:
   - Ensure good lighting
   - Check camera resolution
   - Verify hand/face visibility

3. *Performance Problems*:
   - Reduce camera resolution
   - Close background applications
   - Update graphics drivers

4. *Audio Control Not Working*:
   - Verify Windows audio settings
   - Check PyCAW installation
   - Run as administrator

### Performance Optimization

- Adjust smoothing variable for cursor movement
- Modify SCROLL_COOLDOWN_TIME for scroll sensitivity
- Change BLINK_THRESHOLD for click detection
- Update HAND_HEIGHT_MIN/MAX for click zone

## Notes

- Ensure good lighting for optimal gesture recognition
- Keep your face and hands visible to the camera
- The application works best with a stable frame rate
- Some features may require Windows-specific dependencies
- Regular calibration may improve accuracy

## Future Enhancements

- Multi-monitor support
- Custom gesture mapping
- Machine learning for improved recognition
- Cross-platform compatibility
- Gesture recording and playback

## License

This project is open source and available under the MIT License.

## Contributing

Feel free to submit issues and enhancement requests!

### Development Guidelines

1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Push to the branch
5. Create a Pull Request

### Code Style

- Follow PEP 8 guidelines
- Add comments for complex logic
- Update documentation for new features
- Include test cases for new functionality

## Notes

- Ensure good lighting for optimal gesture recognition
- Keep your face and hands visible to the camera
- The application works best with a stable frame rate
- Some features may require Windows-specific dependencies

## License

This project is open source and available under the MIT License.

## Contributing

Feel free to submit issues and enhancement requests!
