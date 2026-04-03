# Novel-Methods-For-Skull-Fracture-Detection-and-It-s-3D-Reconstruction
📘 Overview

This project presents “Novel Methods for Skull Fracture Detection and Its 3D Reconstruction”, a deep learning–driven approach to accurately identify skull fractures from CT scan data and visualize them in 3D. It combines Region-Based Convolutional Neural Networks (R-CNN) with YOLOv8 architecture to achieve real-time detection accuracy exceeding 95%, alongside automated 3D skull reconstruction from DICOM images.

The proposed model—Skull R-CNN—addresses the limitations of existing detection systems by integrating morphological skull features, skeleton-based region proposals, and a full-resolution feature network for enhanced precision and reduced false positives. 

## 📦 Download

Download the full project files (code, models, dataset):
👉 [Download from Google Drive]([your-google-drive-link-here](https://drive.google.com/file/d/11I78QCBN7hGicXAWeGRZabli3Ujl0OFK/view?usp=sharing))

🎯 Objectives

Accurate Detection: Develop a robust deep learning model for early detection of skull fractures from CT or MRI scans.

3D Visualization: Reconstruct fractured skulls into 3D models to analyze fracture patterns and assist in treatment planning.

Efficiency: Reduce manual detection time using an automated, high-accuracy deep learning pipeline.

Scalability: Enable real-time detection and visualization with minimal computational overhead.

🧩 Problem Statement

Manual analysis of CT scans for skull fractures is time-consuming and error-prone, especially when fractures occur at multiple sites or have subtle appearances. Traditional algorithms produce high false-positive rates and lack the precision needed for small-object detection.

This project introduces Skull R-CNN, leveraging the Faster R-CNN framework with custom region proposals and full-resolution feature extraction to improve small-object detection and enable fast, reliable diagnosis.

⚙️ Methodology
1. Data Pre-processing

Resizing and normalizing CT/MRI images

Noise reduction and contrast enhancement via histogram equalization

Windowing and cropping to isolate cranial regions

Data augmentation (rotation, scaling, flipping) for training diversity

Accurate annotation for supervised model training

2. Model Architecture
🧠 Skull R-CNN

Incorporates morphological skull features for better region proposals

Full-resolution feature network for precise feature extraction

Region of Interest (ROI) alignment to handle variable image sizes

⚡ YOLOv8 Training

Composite loss function with batch size = 8

Adam optimizer, initial learning rate = 1e-3

Adaptive learning rate reduction on validation loss stagnation

Early stopping after 50 epochs of non-improvement

3. Feature Extraction

CNN-based feature extraction for region proposals

Hierarchical learning from edges → textures → fractures

Automated identification of relevant fracture patterns

4. 3D Reconstruction Workflow

Read DICOM image series using SimpleITK

Threshold segmentation to isolate bone structures

Use Marching Cubes algorithm to create 3D surfaces

Render 3D skull models with Matplotlib visualization

Generate animated GIFs for better visual understanding

🖥️ Implementation
🧾 Tools and Libraries

Python, OpenCV, NumPy, Matplotlib, Seaborn, Pandas

YOLOv8 for object detection

SimpleITK for DICOM handling

Plotly / Matplotlib 3D for visualization

💡 Steps

Import datasets and pre-process CT/DICOM images.

Annotate bounding boxes for training using JSON/YAML format.

Train Skull R-CNN and YOLOv8 models on labeled data.

Validate and evaluate using Precision, Recall, and F1-Score.

Perform 3D reconstruction from detected regions.

Visualize fractures in 3D and generate animations.

📊 Results
Metric	Skull R-CNN	Faster R-CNN	YOLOv8 (Proposed)
Accuracy	92%	88%	95%+
F1 Score	90%	87%	93%
AUC	0.94	0.89	0.98
Time Reduction	40%	-	60% faster
✅ Highlights

Reduced false positives while maintaining high sensitivity.

Enhanced visualization with 3D fracture mapping.

Real-time detection for clinical and research applications.

📁 Project Structure
├── data/
│   ├── train/
│   ├── validation/
│   └── test/
├── models/
│   ├── skull_rcnn/
│   ├── yolov8/
│   └── weights/
├── notebooks/
│   ├── preprocessing.ipynb
│   ├── training.ipynb
│   └── reconstruction.ipynb
├── outputs/
│   ├── detected_images/
│   ├── 3d_reconstruction/
│   └── confusion_matrix.png
├── requirements.txt
├── README.md
└── app/
    ├── detection.py
    ├── reconstruction.py
    ├── templates/
    └── static/

📈 Performance Evaluation

Accuracy: Correctly classified fracture regions from skull CT slices

Confusion Matrix: Visual performance representation (TP, TN, FP, FN)

Precision & Recall: Evaluated per-patient and dataset-wise

3D Histogram Analysis: Visualization of pixel intensity distributions

🧠 Application Interface

Detection Module: Upload a skull CT image → model detects fracture regions.

3D Reconstruction Module: Upload DICOM files → reconstructs and visualizes skull in 3D.

🧬 Comparative Analysis
Criteria	Existing Methods	Proposed Method
Detection Algorithm	Traditional ML / CNN	YOLOv8 + R-CNN Hybrid
Accuracy	< 90%	> 95%
Speed	Slow / Manual	Real-time
3D Visualization	Limited	Fully Automated
False Positives	High	Significantly Reduced
📚 References

The project builds upon and compares multiple research studies including works by Kaiming He (Mask R-CNN), Hong Shao (Automated Skull Fracture Analysis), and Yangling Ma (Bone Fracture Detection in X-Rays) among others (see full reference list in report).

👩‍💻 Contributors

Vaishali Hireraddi
Department of Computer Science & Engineering
BLDEACET, Vijayapura

🚀 Future Enhancements

Integration with hospital PACS systems for real-time diagnosis

Extend detection to multiple cranial fracture types and classifications

Deploy web-based API for remote medical image analysis

Incorporate explainable AI (XAI) modules for interpretability

🏁 Conclusion

The proposed Skull R-CNN + YOLOv8 framework significantly enhances skull fracture detection and visualization accuracy while reducing diagnostic time. It demonstrates the power of combining deep learning with medical imaging for life-saving applications. 
