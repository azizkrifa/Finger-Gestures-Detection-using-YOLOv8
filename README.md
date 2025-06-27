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

The dataset is a merged collection of finger gesture images (numbers 0 to 5), created by combining samples from multiple Roboflow datasets (versions v1 to v7).  
You can access the datasets used in this project here:  
👉 [all the datasets link](https://universe.roboflow.com/hands-rirpj/fingers-numbers/dataset/7)


    Images + labels are merged and split into train, val, test using split-folders.

    YOLO format labels (.txt files).

### Classes:

    0: Zero

    1: One

    2: Two

    3: Three

    4: Four

    5: Five

### Directory structure:

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

  ### Training History : 


<img src="https://github.com/user-attachments/assets/29307276-09f6-4567-b09b-30000c99d6e0" width="800" height="600">
<img src="https://github.com/user-attachments/assets/e8c31efb-b3e1-4325-87da-1b50b40e5649" width="800" height="600">


  ### Evaluation Metrics (test set) : 

  ![alt text](Outputs/evalutaion.PNG)
  


  ### Confusion Matrix : 

  📝 Note: Our dataset has 6 classes (0 to 5), but the Ultralytics ConfusionMatrix object includes an extra row and column, making it a 7×7 matrix. This extra class corresponds to the background/no-detection category, which accounts for:
    
-False positives (detections with no matching ground truth)

-False negatives (ground truth objects missed by the model)

   ![alt text](Outputs/Confusion_Matrix.png)


   ### Predictions : 
 <img src="https://github.com/user-attachments/assets/47866d12-480d-434d-b599-557d49648949" width="300" height="300">
<img src="https://github.com/user-attachments/assets/9af89421-d94c-4368-9683-c36329815223" width="300" height="300">
<img src="https://github.com/user-attachments/assets/db5c7fc3-eee4-4f82-8c22-04bdc75eb4b4" width="300" height="300">
<img src="https://github.com/user-attachments/assets/38412b74-45f5-4f48-a77b-4501bfa5d759" width="300" height="300">
<img src="https://github.com/user-attachments/assets/70cb24b7-6e47-4485-b316-860f18c51f3e" width="300" height="300">
<img src="https://github.com/user-attachments/assets/f56f9e36-0e74-4689-a270-df16f8775717" width="300" height="300">





  


  

