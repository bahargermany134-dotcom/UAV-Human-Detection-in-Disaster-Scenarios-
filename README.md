# Human Detection in UAV Disaster Imagery with YOLOv8  

زقث cc
**Date:** November 2025  

---

## 1. Dataset  

| Item | Value |
|------|-------|
| **Total images** | **10 215** |
| **Scenarios** | Fire / smoke, Flood, Collapsed building, Traffic accident |
| **Annotations** | > **360 000** YOLO-style bounding boxes (`class_id center_x center_y w h`) |
| **Split** | Train: **6 129** images  •  Val: **2 043** images |

All images are high-resolution UAV captures.  

---

## 2. Method  

* **Model:** `yolov8n` (Ultralytics) – lightweight, fast inference  
* **Training environment:** Google Colab + Tesla T4 GPU  
* **Hyper-parameters:**  
  ```yaml
  epochs: 25
  imgsz: 640
  batch: 16
  augment: true   # mosaic, hflip, HSV, scale
  optimizer: AdamW (lr = 0.002)
