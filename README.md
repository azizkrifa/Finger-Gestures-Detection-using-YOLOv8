# Finger-Gestures-Detection-using-YOLOv8
This project implements a YOLOv8-based model to detect finger gesture numbers (0-5) using a custom dataset. The goal is to create a lightweight and accurate detector that can recognize hand signs for applications in HCI (Human-Computer Interaction), sign language, and gesture control systems.

## 🚀 Installation

1️⃣ Clone the repository:
```bash
git clone https://github.com/azizkrifa/finger-gestures-detection_using-YOLOv8.git
cd finger-gestures-detection_using-YOLOv8
```

2️⃣ Install dependencies:
```bash
pip install -r requirements.txt
```

## 📂 Dataset

The dataset is a merged collection of finger gesture images (numbers 0 to 5) sourced from Roboflow.

    Images + labels are merged and split into train, val, test using split-folders.

    YOLO format labels (.txt files).

# Classes:

    0: Zero

    1: One

    2: Two

    3: Three

    4: Four

    5: Five

# Directory structure:

    Datasets/
    └── fingers_dataset(split)/
        ├── train/
        │    ├── images/
        │    └── labels/
        ├── val/
        │    ├── images/
        │    └── labels/
        ├── test/
        │    ├── images/
        │    └── labels/
        └── data.yaml


## 🏋️‍♂️ Training Details

    -Model: YOLOv8 nano (yolov8n.pt)

    -Input size: 416×416

    -Epochs: 50

    -Batch size: 32

    -Checkpoints: best model + per-epoch models saved

## 📊 Results / Metrics

  The model achieves good mAP and precision on validation and test sets ( >> 90% ) .

  # Training History : 

  ![alt text](<Training History.png>)

  # Evaluation Metrics (test set) : 

  ![alt text](evalutaion.PNG)


  # Confusion Matrix : 

  ![alt text](Confusion_Matrix.png)

  Note : Our dataset has 6 Classes from 0----5 but Ultralytics ConfusionMatrix adds an extra row/col ( extra class ) for “background” or “no detection” (false positives / false negatives). !!


  

