# MoodMetric AI

## Description
MoodMetric AI leverages YOLOv8 for facial detection and FER (Facial Emotion Recognition) for real-time emotion analysis in videos. This project is designed to enhance user interaction and behavioral analysis by providing insights into emotional responses through advanced video processing techniques in Python.

## Features
- **Facial Detection**: Utilizes YOLOv8 to detect faces in video streams accurately.
- **Emotion Recognition**: Employs the FER model to identify and track emotions on detected faces, offering real-time emotional analysis.
- **Video Output**: Processes and annotates videos with emotional data, saving output for review or further analysis.

## Installation
First, install the required libraries using the following pip command:
```bash
pip install fer ultralytics
```

## Setup and Usage
### Google Colab Setup
Mount Google Drive to access video files and model weights:
```python
from google.colab import drive
drive.mount('/content/drive')
```

### Video Processing
Load the YOLOv8 model and video files, then initiate emotion recognition:
1. **Initialize models**:
   ```python
   from ultralytics import YOLO
   from fer import FER
   model = YOLO('/content/drive/MyDrive/archive/face_yolov8n.pt')
   emotion_recognition_model = FER(mtcnn=True)
   ```

2. **Video capture and processing**:
   - Open video file and set up video writer.
   - Detect faces and recognize emotions frame by frame.
   - Annotate video with emotion data and save the output.

### Output
Save processed video to Google Drive or specified path:
```bash
!cp /content/3_out_FER.mp4 /content/drive/MyDrive/emotion_output
```

## Contributing
Contributions to MoodMetric AI are welcome. Please feel free to fork the repository, make improvements, and submit a pull request.

## License
MoodMetric AI is licensed under the Apache License 2.0. See the LICENSE file for more details.

## Contact
For more information or support, please contact tahafarag111@gmail.com.
