
# 🌊 Underwater Object Detection

This repository provides an **annotated dataset** and a **Jupyter Notebook** for training and evaluating YOLOv8 on underwater object detection tasks. The dataset includes marine species such as **fish, jellyfish, penguins, puffins, sharks, starfish, and stingrays**, making it suitable for **computer vision** and **marine conservation research**.

---

## 📂 Contents

```
📦 aqua-detection-dataset   
 ┣ 📜 underwater_object_detection.ipynb   # Training & evaluation notebook  
 ┣ 📜 requirements.txt         # Dependencies  
 ┣ 📜 README.md                # Documentation  
 ┗ 📂 results/                 # Training logs & sample outputs
```

---

## 📦 Requirements

Create a `requirements.txt` with:

```txt
ultralytics==8.0.200
kagglehub
matplotlib
opencv-python
```

Install all requirements:

```bash
pip install -r requirements.txt
```

---

## 🚀 Usage

### 1️⃣ Clone Repository

```bash
git clone https://github.com/your-username/underwater-object-detection.git
cd underwater-object-detection
```

### 2️⃣ Run Notebook

Open the Jupyter Notebook:

```bash
jupyter notebook underwater_object_detection.ipynb
```

Or use **Google Colab** for GPU acceleration.

### 3️⃣ Train YOLOv8

Inside the notebook:

```python
from ultralytics import YOLO
model = YOLO("yolov8n.pt")
model.train(data="dataset/data.yaml", epochs=50, imgsz=640, name="underwater_train")
```

---

## 📊 Results

YOLOv8n trained for **88 epochs** on this dataset achieved:

| Class     | Precision | Recall | mAP@50 | mAP@50-95 |
| --------- | --------- | ------ | ------ | --------- |
| Fish      | 0.87      | 0.71   | 0.79   | 0.45      |
| Jellyfish | 0.85      | 0.87   | 0.90   | 0.51      |
| Penguin   | 0.71      | 0.74   | 0.72   | 0.33      |
| Puffin    | 0.67      | 0.58   | 0.59   | 0.29      |
| Shark     | 0.73      | 0.65   | 0.70   | 0.47      |
| Starfish  | 0.83      | 0.75   | 0.82   | 0.63      |
| Stingray  | 0.76      | 0.70   | 0.80   | 0.56      |

**Overall mAP@50 ≈ 0.79**
**Overall mAP@50-95 ≈ 0.46**

📌 Example Detection:

![Sample Result](results/sample_output.jpg)

---

## 📜 License

This dataset is intended for **research and educational purposes only**. Check the original [Kaggle dataset license](https://www.kaggle.com/datasets/slavkoprytula/aquarium-data-cots) before commercial use.

---

## 🙌 Acknowledgements

* Dataset: [Aquarium Data - COTS](https://www.kaggle.com/datasets/slavkoprytula/aquarium-data-cots)
* Object Detection: [Ultralytics YOLOv8](https://github.com/ultralytics/ultralytics)


