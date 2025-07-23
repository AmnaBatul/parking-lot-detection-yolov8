# Parking Space Detection with YOLOv8

This project focuses on detecting and classifying individual parking spots as *occupied* or *empty* using the YOLOv8 object detection framework. The goal is to automate parking occupancy monitoring in real-time using aerial or surveillance imagery, supporting smart city and parking management applications.

## Implementation Details:

### Dataset
The model is trained on the [PKLot dataset](https://universe.roboflow.com/brad-dwyer/pklot-1tros), containing labeled images of parking lots with bounding boxes for occupied and empty parking spaces. The dataset is imported directly via the Roboflow API and organized in YOLOv8 format.

### Architecture
The YOLOv8x model is used, which predicts bounding boxes around parking spaces and classifies each box into one of the two categories:
* `space-empty`
* `space-occupied`

### Preprocessing and Augmentation
Input images are resized to 640x640. Data augmentation is applied during training including horizontal flipping, rotation, brightness, contrast, hue, saturation, and value shifts, random scaling, translation, and shear.

### Training Details
* Base Model: YOLOv8x pretrained on COCO
* Epochs: 50
* Batch Size: 16
* Image Size: 640x640
* Optimizer & Scheduler: Default YOLOv8 setup
* Augmentations: Enabled via training parameters

### Evaluation Metrics
Model evaluation is done using standard object detection metrics:
* Precision
* Recall
* mAP@0.5
* mAP@0.5:0.95

## Results:

| Metric         | Value |
|----------------|-------|
| Precision      | 0.999 |
| Recall         | 0.992 |
| mAP@0.5        | 0.994 |
| mAP@0.5:0.95   | 0.993 |


### Contact
If you have any questions, feedback, or collaboration ideas, feel free to reach out:
* 📧 Email: amnabatul2@gmail.com 
* 🌐 GitHub: [AmnaBatul](https://github.com/AmnaBatul)
