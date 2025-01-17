Road Sign Detection Model

Overview

This repository contains a machine learning pipeline for detecting road signs using a custom dataset in VOC format. The model leverages YOLOv5 for real-time object detection and supports classes like traffic lights, speed limits, crosswalks, and stop signs. The project includes preprocessing scripts, training configurations, and a notebook for running and evaluating the model.

Features

Road Sign Detection: Identifies road signs in images and videos in real-time.

Custom Dataset: Trained on a dataset of road signs with classes:

Traffic Light

Speed Limit

Crosswalk

Stop

Flexible Configuration: Training and validation splits specified in a YAML file.

Preprocessing Utilities: Includes scripts for data preparation and conversion from VOC to YOLO format.

Files in the Repository

Road sign Detection Model.ipynb

A Jupyter notebook that contains the code to train, evaluate, and test the road sign detection model using YOLOv5.

preprocessingRoadSigns.py

Python script for preprocessing the dataset, including format conversion and data augmentation.

customVOC.yaml

YAML configuration file specifying the dataset paths and class names for YOLOv5 training.

Example:

path: ../data
train:
  - images
val:
  - images

names:
  0: trafficlight
  1: speedlimit
  2: crosswalk
  3: stop

Getting Started

Prerequisites

Python 3.7+

Required Python libraries (install via pip):

pip install -r requirements.txt

The requirements.txt should include dependencies like torch, opencv-python, and yolov5.

Installation

Clone this repository:

git clone https://github.com/yourusername/road-sign-detection.git
cd road-sign-detection

Set up the environment:

python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
pip install -r requirements.txt

Dataset Preparation

Place your dataset in the data directory.

Ensure the directory structure matches the VOC format.

Update the customVOC.yaml file to specify paths to your dataset.

Usage

Preprocess the Dataset

Run the preprocessing script to convert VOC data to YOLO format:

python preprocessingRoadSigns.py

Train the Model

Launch the training script using YOLOv5:

python yolov5/train.py --img 640 --batch 16 --epochs 50 --data customVOC.yaml --weights yolov5s.pt

Monitor the training process via the logs.

Test the Model

Run inference using the trained weights:

python yolov5/detect.py --weights runs/train/exp/weights/best.pt --img 640 --source data/images

Contributing

Contributions are welcome! Please fork the repository, make changes, and submit a pull request.

License

This project is licensed under the MIT License. See the LICENSE file for details.

Acknowledgments

Ultralytics YOLOv5 for the detection framework.

Road sign dataset contributors.

Feel free to reach out with questions or suggestions!

