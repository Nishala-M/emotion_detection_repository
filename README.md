
# Facial Emotion Detection using Mini-XCEPTION

This project demonstrates facial emotion recognition using OpenCV and a pre-trained Mini-XCEPTION model trained on the FER-2013 dataset.

## 📦 Features

- Real-time facial emotion detection from images
- Uses OpenCV's Haar Cascade for face detection
- Supports 7 emotions:
  - Angry
  - Disgust
  - Fear
  - Happy
  - Sad
  - Surprise
  - Neutral

## 🧠 Model

- **Model Used:** Mini-XCEPTION
- **Input Shape:** 64x64 grayscale
- **Source:** [oarriaga/face_classification](https://github.com/oarriaga/face_classification)
- **File:** `fer2013_mini_XCEPTION.102-0.66.hdf5`

## 🚀 Setup (Google Colab)

1. Install dependencies:
   ```python
   !pip install -q keras opencv-python
   ```

2. Download pre-trained model:
   ```python
   !wget -q https://github.com/oarriaga/face_classification/raw/master/trained_models/emotion_models/fer2013_mini_XCEPTION.102-0.66.hdf5 -O emotion_model.h5
   ```

3. Upload an image and run emotion detection:
   ```python
   uploaded = files.upload()
   for filename in uploaded.keys():
       detect_emotion(filename)
   ```

## 🖼️ Example

When an image with faces is uploaded, the script:
- Detects faces
- Predicts emotions for each face
- Displays the image with bounding boxes and emotion labels

## 📁 Files

- `emotion_model.h5`: Pre-trained emotion recognition model
- `your_image.jpg`: Input image uploaded by the user

## 📌 Notes

- Ensure images are clear and faces are visible for accurate detection.
- Works best with frontal face images.
