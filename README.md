# Accident Prevention System - Night Time Animal Detection

**Project Type:** Final Year Research Project

**Project ID:** 25-26J-340

**Research Component:** Detecting animals in night conditions to enhance road safety and prevent accidents.

**Repository:** [https://github.com/IT22312976/25-26j--340.git](https://github.com/IT22312976/25-26j--340.git)

---

## 📌 Project Overview

Most road accidents during the night occur because drivers cannot see animals crossing the road in time to react. This research component focuses on developing a high-accuracy detection system using **Night Vision/Thermal imagery** and the **YOLOv8** architecture to identify various animal species in low-visibility conditions, providing an early warning system for the driver.

## 🚀 Features

* **Real-time Animal Detection:** Optimized for low-light and night-time environment processing.
* **Multi-Class Identification:** Detects 17 different animal species including Wild Boars, Tigers, Deer, and domestic animals.
* **High Precision:** Trained on a specialized night-time dataset to minimize false positives from shadows or vegetation.
* **Driver Alert System:** Designed to be integrated into vehicle dashboards for "Right Safety."

## 📊 Dataset Details

The model was trained and validated using a comprehensive dataset specifically curated for night-time conditions.

* **Total Images:** 9692 images.
* **Training Set:** 6778 images.
* **Validation Set:** 1948 images.
* **Testing Set:** 965 images.
* **Classes (17 Species):** Sable, Weasel, AmurTiger, MuskDeer, LeopardCat, RaccoonDog, Hare, Leopard, RedFox, SikaDeer, RoeDeer, Badger, WildBoar, Cow, BlackBear, Y-T-Marten, Dog.

## 🛠️ Technology Stack

* **Deep Learning Framework:** PyTorch
* **Model Architecture:** YOLOv8 (Nano)
* **Language:** Python 3.12+
* **Image Processing:** OpenCV, PIL
* **Deployment:** FastAPI / Flask (Backend Server)

## 📈 Research Results

The model demonstrated strong performance in identifying animals in pitch-black and low-contrast environments:

* **mAP50:** 0.929 (92.9%)
* **Precision:** 0.891
* **Recall:** 0.875
* **Inference Speed:** ~2.2ms per image (on Tesla T4 GPU)

## 📂 Project Structure

```text
├── night_time_animal_identification.ipynb  # Training and Evaluation Notebook
├── best_animal_detector.pt                # Trained YOLOv8 weights
├── data/
│   ├── train/                             # Training images and labels
│   ├── valid/                             # Validation images and labels
│   └── test/                              # Test images and labels
├── requirements.txt                       # Python dependencies
└── README.md                              # Project Documentation

```

## ⚙️ Installation & Usage

1. **Clone the Repository:**
```bash
git clone https://github.com/IT22312976/25-26j--340.git
cd 25-26j--340

```


2. **Install Dependencies:**
```bash
pip install ultralytics opencv-python torch

```


3. **Run Inference:**
```python
from ultralytics import YOLO
model = YOLO('best_animal_detector.pt')
results = model.predict(source='night_road_video.mp4', show=True)

```

## 👥 Research Team

* **Student Name:** Vithyasaji Sritharan
* **Student ID:** IT22312976
* **University:** Sri Lanka Institute of Information Technology (SLIIT)
* **Academic Year:** 2025/2026
