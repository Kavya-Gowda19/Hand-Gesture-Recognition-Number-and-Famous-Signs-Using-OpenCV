# Hand Gesture Recognition (Number and Famous Signs) Using OpenCV

This project is a Python-based hand gesture recognition system that detects and identifies numbers and famous signs using a webcam. The system leverages OpenCV for image processing and computer vision tasks.

## Features

- **Real-Time Gesture Recognition**: Recognizes hand gestures such as numbers (0-5) and famous signs like "OK" and "Best of Luck" in real-time.
- **Customizable**: The code can be extended to recognize more gestures by modifying the detection logic.
- **Interactive Interface**: The application requests camera access from the user and provides real-time feedback on the detected gestures.

## How It Works

1. **Camera Capture**: The application captures video from the default camera using OpenCV.
2. **Region of Interest (ROI)**: A specific area of the video frame is designated as the region of interest where hand gestures are detected.
3. **Skin Detection**: The ROI is converted to the HSV color space to detect skin-like colors.
4. **Contour Detection**: The skin region is processed to find contours, which are then used to identify the hand.
5. **Convex Hull and Defects**: The convex hull is calculated for the hand contour, and defects in the hull are analyzed to recognize the number of fingers and specific gestures.
6. **Gesture Recognition**: Based on the number of detected defects and the area of the hand, the system recognizes specific gestures and displays corresponding messages.

## Usage

- Run the script, and you will be prompted to allow camera access.
- Position your hand in the green box on the screen.
- The system will recognize the number of fingers and famous signs like "OK" and "Best of Luck" and display the corresponding gesture on the screen.

## Example Output

- **0 Fingers**: Displays "0"
- **1 Finger**: Displays "1"
- **2 Fingers**: Displays "2"
- **3 Fingers**: Displays "3" or "OK" (depending on the area ratio)
- **4 Fingers**: Displays "4"
- **5 Fingers**: Displays "5"
- **"Best of Luck"**: Recognized based on the area ratio

## Troubleshooting

- **No Camera Access**: If you deny camera access, the application will not run.
- **Gesture Not Detected**: Ensure your hand is within the ROI and is clearly visible.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request or open an issue.

## License

This project is licensed under the MIT License.
