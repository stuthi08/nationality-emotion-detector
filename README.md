
# Nationality and Emotion Detection Tool

This project is a real-time face analysis system that predicts **nationality**, **emotion**, **age**, and **dress color** based on a facial image. It uses deep learning models, computer vision, and a GUI for user interaction.

## 📌 Features

- **Nationality Detection** using a CNN trained on the FairFace dataset.
- **Emotion Detection** via a CNN trained on the FER-2013 dataset.
- **Conditional Predictions**:
  - Indian: Emotion, Age, Dress Color
  - US: Emotion, Age
  - African: Emotion, Dress Color
  - Other: Emotion, Nationality only
- **Age Prediction** using a regression head from the nationality model.
- **Dress Color Detection** using YOLOv8 for person detection and KMeans for clustering colors.
- **GUI** built with Tkinter supporting image upload and webcam.

## 📁 Folder Structure

```plaintext
task_2/
│
├── nationality_det/
│   ├── train/
│   ├── val/
│   ├── fairface_label_train.xlsx
│   ├── fairface_label_val.xlsx
│   └── nationality-det.ipynb
│
├── dress_color_utils.py           # KMeans clustering for clothing color
├── emotion_detection_model.h5     # FER-2013-based emotion model
├── emotion-detection.ipynb        # Emotion model code
├── gender_encoder.pkl             # Gender label encoder
├── gui.py                         # Tkinter GUI
├── haarcascade_frontalface_default.xml
├── mobilenet_v2_weights_tf_dim_ordering_tf_kernels_1.0_224_no_top.h5
├── nationality_encoder.pkl
├── nationality_model.keras        # Main CNN model for nationality/age
├── yolov8n.pt                     # YOLOv8 model for torso detection
├── report.pdf                     # Final report
└── README.md                      # This file
