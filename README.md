## Project Overview
This is a project made for a further understanding about YOLOv8 and model quantization in vehicle detection problem.  

The reason for choosing YOLOv8:
- It is designed for tasks like classification, object detection, and image segmentation, YOLOv8 outshines its predecessor, YOLOv7, in both precision and speed. 
- By utilizing Darknet53 as its backbone, it employs more feature maps and efficient convolutional neural networks, resulting in higher mAP and fps. 
- YOLOv8 introduces an innovative anchor-free detection head, enabling pixel-wise bounding box estimations akin to image segmentation techniques, and incorporates a new loss function. This culmination of features achieves a mean Average Precision of 53.7% on the COCO benchmark dataset, marking YOLOv8 as a state-of-the-art model in object detection.
## 1. Install
CUDA version used in this project: 11.8

To install specified version of torch with CUDA, you must install from  `requirements_torch.txt` before install from `requirements.txt`

Training process is done in `training_model.ipynb`

## 2. Load the model
The model is located at `runs/detect/train6/weights/`.  
They are exported to both `onnx` and `pt` formats.

## 3. Result
Metrics after training:
| **Metric** | **Value** |
|------------|-----------|
| precision  | 0.927     |
| recall     | 0.923     |
| mAP50      | 0.971     |
| mAP50-95   | 0.737     |

After quantization, the model's size reduced from 11MB to 3MB

A example of inference can be shown as below
![Alt text](output.png "a title")

