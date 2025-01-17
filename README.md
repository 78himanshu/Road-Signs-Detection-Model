
Road Sign Detection Model
=========================

Overview
--------

This repository contains the implementation of a road sign detection model using YOLOv5, PyTorch, and OpenCV (CV2). The model is designed to detect and classify various types of road signs, including traffic lights, speed limit signs, crosswalks, and stop signs. The project utilizes a custom VOC dataset for training and evaluation.

Features
--------

*   **Real-Time Detection**: Leverages OpenCV for live video feed processing.
    
*   **Accurate Predictions**: Trained on a well-labeled dataset using YOLOv5.
    
*   **Custom Dataset**: Built with a tailored dataset for traffic signs.
    
*   **Scalable**: Easily adaptable to include additional classes or data.
    

Getting Started
---------------

### Prerequisites

To run the code, make sure you have the following installed:

*   Python 3.8+
    
*   PyTorch
    
*   OpenCV (cv2)
    
*   YOLOv5 repository cloned
    
*   Other dependencies from requirements.txt (if provided)

### Installation

1.  Clone this repository:
    

git clone https://github.com/78himanshu/road-sign-detection

Dataset
-------

The model is trained on a custom VOC dataset. The dataset includes the following classes:

*   Traffic Light
    
*   Speed Limit
    
*   Crosswalk
    
*   Stop

Preprocessing
-------------

The preprocessingRoadSigns.py script handles:

*   Image resizing and augmentation
    
*   Conversion to YOLO-compatible format
    
*   Dataset splitting into training and validation sets


Training
--------

Train the model using YOLOv5:


*   --img: Image size (320)
    
*   \--batch: Batch size (16)
    
*   \--epochs: Number of training epochs (50)
    
*   \--data: Path to the dataset YAML file (customVOC.yaml)
    
*   \--weights: Pretrained weights file (best.pt)

Results
-------

### Training Results

Screenshots from the training process:

*   **Loss Trends**: Training and validation loss
    
*   **mAP**: Mean Average Precision over epochs
    

### Example Detections

Below are sample detections from the trained model:

*   Detection of traffic lights
    
*   Speed limit signs identified
    
*   Stop signs detected accurately
