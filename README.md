search-and-rescue-ml
Search and Rescue using Machine Learning applies ML techniques to analyze satellite and drone imagery from the SARD2 dataset, aiming to detect human presence or distress signals in remote areas to support faster and more efficient rescue operations.

This project uses a YOLOv10n object detection model to help identify people, boats, and debris in aerial images during search and rescue missions. The model is trained on the SARD2 dataset from Kaggle.

About the Project

Goal: Automatically detect key objects in aerial images to support search and rescue operations.
- Model Used: YOLOv10n (a fast and lightweight object detection model)
- Dataset: [SARD2 from Kaggle](https://www.kaggle.com/datasets/nikolasgegenava/sard-2-search-and-rescue-dataset-extra-classes)

How It Works

1. The model is trained to detect classes like:
   - Person
   - Boat
   - Debris
2. You can run it on new images to locate these objects with bounding boxes.
3. The trained model gives fast and accurate results.

How to Run the Project

1. Clone the Repository

```
git clone https://github.com/Vara-Anjan-B/search-and-rescue-ml.git
cd search-and-rescue-ml
````

2. Install Dependencies

```
pip install -r requirements.txt
```

3. Train the Model (optional – already trained for 100 epochs)

```
python src/train.py
```

4. Run Inference (detect objects in test images)

```
python src/predict.py
```

---

📁 Project Structure
```
search-and-rescue-ml/
├── data/             # Sample images and labels
├── models/           # Trained YOLOv10n model
├── yolov10/          # YOLOv10 source code
├── README.md         # This file
├── requirements.txt  # Python packages needed
└── .gitignore        # Files to ignore
```

---

## 🖼️ Sample Results

| Original Image        | Detection Output       |
| --------------------- | ---------------------- |




![gss1495_jpg rf b30ada643d64c788f4784de2343c55fa](https://github.com/user-attachments/assets/34f82261-d751-4f19-9e32-5cddcd56ba52)

![image](https://github.com/user-attachments/assets/d92e35c1-34d6-4611-a43e-e6b6e043971e)


---

Model Performance

* **Trained for:** 100 epochs
* **Image size:** 640 × 640
* **Best model saved to:** `models/best.pt`

| Metric    | Score   |
| --------- | ------- |
| mAP\@0.5  | 0.795 % |
| Precision | 0.901 % |
| Recall    | 0.865 % |


Acknowledgements

* [YOLOv10 GitHub Repository](https://github.com/WongKinYiu/yolov10)
* [SARD2 Dataset on Kaggle]([https://www.kaggle.com/datasets/...](https://www.kaggle.com/datasets/nikolasgegenava/sard-2-search-and-rescue-dataset-extra-classes)


