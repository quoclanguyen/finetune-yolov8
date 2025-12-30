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

