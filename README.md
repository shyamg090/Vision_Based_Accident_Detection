# Vision-Based Accident Detection System

This project is a vision-based accident detection system that utilizes the YOLOv8 model for real-time accident detection. The system detects accidents in video footage or live camera feeds and triggers an alarm sound when an accident is detected. The model has been trained on thousands of images and videos to accurately identify accidents.

## Features

- **Real-time accident detection:** Detects accidents using the YOLOv8 model.
- **Alarm Trigger:** Plays an alarm sound when an accident is detected.
- **Video Recording:** Saves the processed video with bounding boxes showing detected accidents.
- **Configurable Input:** Use either a video file or live camera feed for detection.

## Prerequisites

Before running the project, make sure you have the following installed:

- Python 3.8 or higher
- OpenCV
- Ultralytics YOLOv8
- Pygame

## Installation

1. Clone the repository:

    ```bash
    git clone https://github.com/shyamg090/accident-detection-system.git
    cd accident-detection-system
    ```

2. Install the required Python packages:

    ```bash
    pip install -r requirements.txt
    ```

3. Download the YOLOv8 model file (`best.pt`) and place it in the project directory.

4. Place the alarm sound file (`alarm.wav`) in the project directory.

## Usage

1. **Configure Input Source:**  
   - To use a video file, set `use_video_file = True` and provide the path to the video file.
   - To use a live camera feed, set `use_video_file = False`.

2. **Run the System:**

    ```bash
    python accident_detection.py
    ```

3. The output video with detected accidents will be saved in the `outputs` folder.

## Code Explanation

- `YOLO('best.pt')`: Initializes the YOLO model with the pre-trained weights.
- `cv2.VideoCapture()`: Captures video from the specified source (file or camera).
- `pygame.mixer.Sound()`: Loads the alarm sound file to be played when an accident is detected.
- `output_video.write(frame)`: Saves the processed frames with bounding boxes into the output video file.
- `cv2.imshow()`: Displays the video with detected bounding boxes.

## Folder Structure

```bash
Final Year Project Basics Of Machine Learning-Project/
│
├── .ipynb_checkpoints/                  # Checkpoint files for Jupyter Notebook
│
├── data/                                # Folder containing datasets and related files
│
├── runs/                                # Folder to store outputs such as saved videos
│
├── .DS_Store                            # macOS system file, typically hidden
│
├── accident_detection.ipynb             # Jupyter Notebook containing the main code
│
├── alarm.wav                            # Alarm sound file played when an accident is detected
│
├── best.onnx                            # ONNX version of the YOLOv8 model weights
│
├── best.pt                              # YOLOv8 trained weights for accident detection
│
├── data.yaml                            # Configuration file containing dataset paths and settings
│
├── testing.jpg                          # Test image used for model evaluation
│
├── testing1.mp4                         # Test video file 1 for accident detection
│
├── testing2.mp4                         # Test video file 2 for accident detection
│
└── yolov8s.pt                           # YOLOv8 small version weights for testing purposes
```

## Dependencies

- **Ultralytics:** YOLOv8 model used for detection.
- **OpenCV:** For video processing and displaying frames.
- **Pygame:** To play the alarm sound when an accident is detected.

## Output

Add images or video clips here showing the detection results. This section can be filled with screenshots or video files demonstrating how the system identifies accidents.

[Sample Output Video]([path/to/output-video.mp4](https://github.com/shyamg090/Vision_Based_Accident_Detection/blob/main/runs/detect/outputs/output_video.avi))

## Future Improvements

- Add email or SMS notifications when an accident is detected.
- Implement a web interface to monitor live accident detection.
- Enhance model accuracy with more diverse datasets.

## License

This project is licensed under the MIT License.

## Acknowledgments

- Special thanks to the creators of YOLOv8 for their incredible work on object detection models.
- Thanks to the contributors who helped improve this project.

## Contact

For any inquiries or feedback, please contact [shyamg3000@gmail.com].

