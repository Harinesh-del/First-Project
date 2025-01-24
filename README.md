# Age and Gender Detection System

This project implements a real-time age and gender detection system using OpenCV's deep learning module (DNN). It leverages pre-trained deep learning models to analyze live webcam video feeds and predict the gender and approximate age group of detected individuals. The results are displayed on the video feed with bounding boxes around faces and corresponding labels.

## Features

- **Face Detection**: Uses a pre-trained face detection model to identify and localize faces in a video frame.
- **Age Prediction**: Classifies detected faces into one of eight predefined age ranges: 
  - `(0-2)`
  - `(4-6)`
  - `(8-12)`
  - `(15-20)`
  - `(25-32)`
  - `(38-43)`
  - `(48-53)`
  - `(60-100)`
- **Gender Prediction**: Identifies the gender as either `Male` or `Female`.
- **Real-Time Operation**: Processes live video input from a webcam and overlays predictions directly on the video feed.
- **Data Export**: Stores predicted age and gender information in an Excel file (`gender_age_data.xlsx`) for further analysis.

## Models and Frameworks

This project uses the following pre-trained models:
1. **Face Detection Model**:
   - Model: `opencv_face_detector_uint8.pb`
   - Configuration: `opencv_face_detector.pbtxt`
2. **Age Prediction Model**:
   - Model: `age_net.caffemodel`
   - Configuration: `age_deploy.prototxt`
3. **Gender Prediction Model**:
   - Model: `gender_net.caffemodel`
   - Configuration: `gender_deploy.prototxt`

All models are processed using the OpenCV DNN module to ensure high-speed inference.

## How to Run

1. Clone the repository and navigate to the project directory.
2. Ensure that all model files (`.pb`, `.pbtxt`, `.caffemodel`, `.prototxt`) are downloaded and the file paths in the script are correctly set.
3. Install the required Python libraries:
   ```bash
   pip install opencv-python pandas
   ```
4. Run the script:
   ```bash
   python Age_And_Gender.py
   ```
5. Use the webcam feed to test the application. Press `q` to exit the application.

## Output

- A live video feed with bounding boxes around detected faces, displaying gender and age predictions.
- An Excel file (`gender_age_data.xlsx`) containing a log of all detected genders and age groups.
