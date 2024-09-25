# Real-Time Facial Expression Detection and Labeling with MTCNN

This project processes video to detect faces, enhance them, and allows for manual labeling of facial expressions. Using MTCNN for face detection and OpenCV for image processing, the system enables the user to create a labeled dataset for facial expression recognition.

Key Features:
- Real-time face detection and enhancement
- User-defined manual labeling of seven emotions: anger, disgust, fear, happiness, neutral, sadness, and surprise
- Automatic saving of detected faces into specific labeled folders
- Processes video frames at regular intervals, customizable for different datasets

This is a useful tool for AI researchers and developers looking to build custom datasets for emotion detection.

--

### `README.md` File:

# Real-Time Facial Expression Detection and Labeling with MTCNN

This project provides an efficient solution for detecting faces in video frames, enhancing their quality, and enabling user-defined labeling for facial expressions. The labeled data is stored in predefined folders, making it ready for use in machine learning and deep learning models focused on emotion recognition.

## Features
- **Face Detection:** Uses MTCNN to detect faces from video frames at 10-second intervals.
- **Image Processing:** Denoises and enhances detected faces using OpenCV techniques (Non-Local Means Denoising and histogram equalization).
- **User Interaction:** Allows manual labeling of detected faces into seven emotion categories:
  - Anger
  - Disgust
  - Fear
  - Happiness
  - Neutral
  - Sadness
  - Surprise
- **Data Storage:** Automatically saves labeled faces to folders, with each face image named uniquely using random numbers.
- **Video Processing:** Processes video frames in real-time and continues until manually stopped by the user.

## Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/real-time-facial-expression-labeling.git
   cd real-time-facial-expression-labeling
   ```
2. Install the required packages:
   ```bash
   pip install mtcnn opencv-python numpy
   ```

3. Make sure you're using Google Colab or a similar environment that supports `cv2_imshow` for image display.

## How It Works
1. **Input Video:** The code processes a video file frame-by-frame using OpenCV's `VideoCapture`.
2. **Face Detection:** Every 10 seconds, MTCNN detects faces in the frame, and the detected faces are cropped and enhanced.
3. **User-Defined Labeling:** The user is shown the enhanced face and asked to label it by selecting an appropriate facial expression.
4. **Saving Faces:** Labeled faces are resized to 224x224 pixels and saved in pre-organized folders according to their assigned emotion labels.

## Code Walkthrough

1. **Pre-trained Label Setup:**
   A set of predefined emotion labels (`anger`, `disgust`, etc.) is used to create corresponding folders for data storage.

2. **Face Detection with MTCNN:**
   - MTCNN is initialized to detect faces in each frame.
   - Detected faces are denoised and enhanced before being displayed to the user for labeling.

3. **User Labeling:**
   The user manually selects the appropriate label for each detected face from a displayed list of options.

4. **Saving Data:**
   Detected and labeled faces are saved in corresponding folders under the main output directory.

## Usage Example
- Upload a video to the system (e.g., class lecture videos or surveillance footage).
- The program will detect faces, ask you to label them, and automatically store the labeled faces in corresponding folders.
  
```python
# Initialize video capture
cap = cv2.VideoCapture("/path/to/your/video.mp4")
```

- Stop the video processing by pressing 'q'.

## Dependencies
- Python 3.x
- OpenCV
- MTCNN
- NumPy

## Future Improvements
- Automate labeling using a pre-trained facial expression recognition model.
- Add support for batch processing of multiple video files.
- Enhance the UI for more intuitive labeling.


## Contact
For any questions or suggestions, feel free to reach out to me at [shaheeqraza1214@gmail.com](mailto:shaheeqraza1214@gmail.com).

