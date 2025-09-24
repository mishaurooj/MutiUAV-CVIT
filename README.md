# MultiUAV Dataset and Models

This repository contains the dataset and model implementations for **MultiUAV Detection**, designed for multiclass UAV classification and detection using deep learning techniques.

---

## 📂 Dataset
We use the **MultiUAV Dataset** hosted on [Roboflow Universe](https://universe.roboflow.com/noor-djz41/multiuav/dataset/4).  
The dataset includes:
- **Classes**: Multi-rotor, Single-rotor, Fixed-wing UAVs  
- **Images**: 11,733 total images  
- **Splits**:
  - 93% training
  - 3% validation
  - 4% testing

**Preprocessing and Augmentations:**
- Resizing  
- Saturation and exposure adjustment  
- Annotation with bounding boxes  

---

## 🧑‍💻 Available Notebooks
This repository also includes Jupyter Notebooks for model training and experimentation:

- `CVIT_PANet_head_multiUAV.ipynb` – PANet head experiment  
- `CVIT_BiFPN_head_multiUAV.ipynb` – BiFPN head experiment  
- `CVIT_FPN_head_multiUAV.ipynb` – FPN head experiment  
- `YOLOv5s-transformer_multiUAV.ipynb` – YOLOv5 with transformer backbone  
- `YOLOv5s-GViTv1_multiUAV.ipynb` – YOLOv5s with GViT v1 backbone  
- `YOLOv3-GViT_multiUAV.ipynb` – YOLOv3 with GViT backbone  

These notebooks implement different backbone and head modifications to improve UAV detection performance.

---

## 🚀 Training
Example training commands:

```bash
# Train YOLOv5 with custom dataset
python train.py --data data.yaml --cfg yolov5s.yaml --weights yolov5s.pt --epochs 50

# Train YOLOv7 with custom dataset
python train.py --data data.yaml --cfg yolov7.yaml --weights yolov7.pt --epochs 50
```

---

## 📊 Results
Baseline results reported on this dataset (example values, to be updated with your experiments):

| Model                   | Precision | Recall | mAP@0.5 | F1-score |
|--------------------------|-----------|--------|---------|----------|
| YOLOv5s-Transformer      | 93%       | 92%    | 95%     | 92%      |
| YOLOv5s-GViTv1           | 94%       | 93%    | 95.5%   | 92.5%    |
| YOLOv3-GViT              | 91%       | 90%    | 93%     | 91%      |

---
## 📌 License
This repository is for **academic use only**.  
Please cite the dataset and related papers when using it.
