# Helmet and Number Plate Detection using YOLOv3 and OpenCV

## Overview
This project uses **YOLOv3** and **OpenCV** to detect motorcycles, helmets, and number plates in real-time. It also utilizes a CNN model to classify whether a rider is wearing a helmet or not. The system processes a video file, identifies riders, checks for helmet usage, and highlights detected number plates.

## Features
- **YOLOv3-based object detection**: Detects motorcycles and number plates.
- **CNN-based helmet classification**: Determines if a rider is wearing a helmet.
- **Real-time video processing**: Analyzes frames from a video feed.
- **Bounding boxes & labels**: Draws colored boxes around detected objects.
- **CUDA/MPS support**: Uses GPU acceleration for improved performance.

## Dependencies
Ensure you have the following dependencies installed:
```bash
pip install opencv-python numpy imutils tensorflow
```

## Installation
1. Clone this repository:
   ```bash
   git clone https://github.com/your-repo/helmet-detection.git
   cd helmet-detection
   ```

2. Download the necessary YOLOv3 model files:
   - `yolov3-custom_7000.weights`
   - `yolov3-custom.cfg`

3. Place your trained helmet classification model (`helmet-nonhelmet_cnn.h5`) in the project directory.

4. Ensure you have a video file (`video.mp4`) to process.

## Usage
Run the following command to start detection:
```bash
python detect.py
```

## File Structure
```
helmet-detection/
│-- yolov3-custom_7000.weights
│-- yolov3-custom.cfg
│-- helmet-nonhelmet_cnn.h5
│-- video.mp4
│-- detect.py
│-- README.md
```

## Model Details
- **YOLOv3**: Detects motorcycles and number plates.
- **CNN Classifier**: Classifies cropped head regions as helmet or no-helmet.
- **Thresholds**:
  - Detection confidence > 0.3
  - Non-Maximum Suppression (NMS) threshold = 0.4

## Output
- Saves processed video as `output.avi`.
- Displays real-time detection results with bounding boxes.

## Notes
- Ensure that CUDA is enabled for GPU acceleration.
- You can fine-tune YOLOv3 by training on a custom dataset.
- Modify `detect.py` to adjust detection confidence thresholds.

## License
This project is licensed under the MIT License.

