# Crowd Anomaly Detection using CNN Autoencoder & ConvLSTM

> **Book Chapter Publication:** *Crowd Anomaly Detection using CNN Autoencoder and ConvLSTM* is currently **under publication**.

An AI-powered Crowd Anomaly Detection system that leverages **Computer Vision**, **Deep Learning**, and **Unsupervised Learning** to automatically identify abnormal crowd behavior in surveillance videos.

Instead of relying on manually labeled anomaly data, the system learns **normal crowd behavior** and detects anomalies by measuring deviations in spatial appearance and temporal motion patterns.

---

## Overview

Crowd management has become an increasingly important challenge in public places such as:

- Railway Stations
- Metro Stations
- Stadiums
- Shopping Malls
- Airports
- Religious Gatherings
- Public Events

Traditional surveillance systems require continuous human monitoring, making them inefficient for detecting sudden abnormal crowd behavior.

This project introduces an intelligent surveillance solution capable of automatically detecting unusual crowd activities such as:

- Panic situations
- Sudden running
- Chaotic movement
- Overcrowding
- Irregular motion patterns

using Deep Learning-based anomaly detection.

---

# Key Features

- CNN Autoencoder for spatial anomaly detection
- ConvLSTM for temporal sequence learning
- Optical Flow-based motion estimation
- Hybrid spatial + motion feature fusion
- Unsupervised anomaly detection
- Reconstruction error-based anomaly scoring
- Temporal anomaly modeling
- Frame sequence processing
- Video preprocessing pipeline
- Threshold-based anomaly classification
- Visualization of anomaly scores
- Modular deep learning architecture
- Easily extensible for future research

---

# System Architecture

The complete pipeline consists of multiple modules working together.

```
Input Video
      │
      ▼
Frame Extraction
      │
      ▼
Image Preprocessing
      │
      ├──────────────┐
      ▼              ▼
CNN Autoencoder   Optical Flow
      │              │
      └──────┬───────┘
             ▼
      Feature Fusion
             │
             ▼
       ConvLSTM Module
             │
             ▼
      Anomaly Scoring
             │
             ▼
 Thresholding & Detection
             │
             ▼
Visualization
```

---

# Working Pipeline

### 1. Video Input

The system accepts surveillance videos or recorded CCTV footage.

---

### 2. Frame Extraction

Videos are converted into individual frames for further processing.

---

### 3. Image Preprocessing

The extracted frames are:

- Resized
- Normalized
- Cleaned
- Prepared for model input

---

### 4. Spatial Feature Learning

A CNN-based Autoencoder learns the appearance of normal crowd scenes.

The encoder compresses image information into a latent representation while the decoder reconstructs the original frame.

Abnormal scenes generate higher reconstruction errors.

---

### 5. Motion Estimation

Optical Flow is used to analyze movement between consecutive frames.

This captures:

- Crowd movement
- Motion intensity
- Sudden directional changes
- Dynamic crowd behavior

---

### 6. Temporal Learning

Instead of analyzing individual frames independently, consecutive frame sequences are passed into a ConvLSTM network.

ConvLSTM captures:

- Temporal dependencies
- Motion evolution
- Sequential crowd behavior

allowing more reliable anomaly detection.

---

### 7. Feature Fusion

The outputs from

- CNN Autoencoder
- Optical Flow
- ConvLSTM

are combined to generate a final anomaly score.

---

### 8. Anomaly Detection

If the anomaly score exceeds a predefined threshold, the frame sequence is classified as abnormal.

Examples include:

- Panic
- Stampede-like behavior
- Crowd disorder
- Unusual motion

---

# Model Components

## CNN Autoencoder

Purpose:

- Learn normal crowd appearance
- Reconstruct input frames
- Detect spatial anomalies using reconstruction error

---

## Optical Flow

Purpose:

- Estimate pixel motion
- Detect sudden crowd movement
- Capture motion magnitude

---

## ConvLSTM

Purpose:

- Learn temporal dependencies
- Understand crowd behavior across multiple frames
- Improve anomaly detection accuracy

---

## Hybrid Fusion

Combines

- Spatial Features
- Motion Features
- Temporal Features

to generate a more robust anomaly score than using any single model individually.

---

# Technologies Used

- Python
- TensorFlow / PyTorch
- OpenCV
- NumPy
- Matplotlib
- CNN
- ConvLSTM
- Optical Flow
- Deep Learning
- Computer Vision

---

# Machine Learning Approach

**Learning Type**

Unsupervised Learning

The model is trained only on **normal crowd behavior**.

Since abnormal events are rare and difficult to label, anomalies are detected through deviations from learned normal patterns.

---

# Project Highlights

- Unsupervised crowd anomaly detection
- Deep learning-based surveillance analysis
- Spatio-temporal feature extraction
- Motion-aware anomaly detection
- CNN Autoencoder implementation
- ConvLSTM sequence modeling
- Optical Flow integration
- Hybrid feature fusion
- Automated anomaly scoring
- Visualization of detected anomalies

---

# Potential Applications

- Smart City Surveillance
- Airport Security
- Railway Stations
- Metro Stations
- Stadium Monitoring
- Shopping Malls
- Traffic Surveillance
- Public Event Monitoring
- Campus Security
- Emergency Crowd Management

---

# Future Improvements

- Real-time inference
- YOLO-based person localization
- Transformer-based temporal modeling
- Attention mechanisms
- Multi-camera anomaly detection
- Edge AI deployment
- Alert notification system
- Web dashboard for monitoring
- Live CCTV integration
- Model optimization for embedded devices

---

# Project Structure

```
Crowd-Anomaly-Detection/
│
├── dataset/
├── models/
├── preprocessing/
├── optical_flow/
├── training/
├── inference/
├── utils/
├── outputs/
├── notebooks/
├── requirements.txt
└── README.md
```

> Folder names may vary depending on the implementation.

---

# Results

The proposed hybrid architecture combines:

- CNN Autoencoder
- Optical Flow
- ConvLSTM

to improve anomaly detection by learning both spatial appearance and temporal crowd dynamics.

Compared to standalone approaches, the hybrid framework provides:

- Better temporal understanding
- Reduced false detections
- More stable anomaly scores
- Improved robustness under varying crowd conditions

---

# Research Contribution

This work explores a hybrid deep learning framework for unsupervised crowd anomaly detection by integrating:

- Spatial Feature Learning
- Motion Estimation
- Temporal Sequence Modeling

to build an intelligent surveillance system capable of identifying abnormal crowd behavior without requiring labeled anomaly data.

---

# Authors

- Shlok Pastagia
- Avi Jain
- Yash Patel 
- Ishan Sharma
- Khush N Patel
- Sachin Meena

---

# Acknowledgements

This project was developed as part of the **Engineering Project in Community Service (EPICS)** at **VIT Bhopal University**.

Special thanks to our project supervisor for continuous guidance and support throughout the project.

---

# License

This project is intended for academic and research purposes.
