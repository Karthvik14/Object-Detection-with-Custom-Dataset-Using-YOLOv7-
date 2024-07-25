# Detecting Soccer Players with YOLOv7: Ball Possession Classification

## Project Overview

This project involves building a custom object detection model using the YOLOv7 architecture to detect soccer players and classify whether they have possession of the ball. The dataset consists of approximately 1000 annotated images, and the model can process both images and videos.

## Project Files

- **main.ipynb**: The main Jupyter notebook containing all code and steps for data preparation, model training, and evaluation.
- **Annotated Data**: The annotated images with labels indicating whether the player has the ball or not.

## Google Drive Link

All necessary files, including the dataset and trained model weights, can be accessed here: [Google Drive Folder](https://drive.google.com/drive/folders/16ZFEZA8w8cTLzVBk2xyIykT7Te2G745Y?usp=drive_link)

## Steps to Reproduce

### Step 1: Connect to Google Colab GPU

1. Navigate to `Edit` -> `Notebook settings`.
2. Select `GPU` from the hardware accelerator drop-down.

### Step 2: Mount Google Drive

```python
from google.colab import drive
drive.mount("/content/gdrive")
```

### Step 3: Change Directory to Project Folder
```
%cd /content/gdrive/MyDrive
```
### Step 4: Create Project Directory
```
import os
if not os.path.isdir("ML_project"):
    os.makedirs("ML_project")
%cd ML_project
```
### Step 5: Clone YOLOv7 Repository
```
!git clone https://github.com/WongKinYiu/yolov7
%cd yolov7
```
### Step 6: Install Required Packages
```
!pip install -r requirements.txt
```
### Step 7: Download Pre-Trained YOLOv7 Weights
```
!wget https://github.com/WongKinYiu/yolov7/releases/download/v0.1/yolov7.pt
```
## Training the Model
The notebook main.ipynb contains the code to train the YOLOv7 model on the soccer player dataset. Ensure that the dataset is correctly structured and located in the appropriate directory within your Google Drive.

## Results
After training, the model can accurately detect players with and without the ball in both images and videos. Example results, including detected photos and videos, are located at runs/detect/.

## Acknowledgements
- The YOLOv7 repository: https://github.com/WongKinYiu/yolov7
- Google Colab for providing free GPU access.
