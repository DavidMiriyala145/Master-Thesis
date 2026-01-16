# 🧠 Advanced Colorectal Polyp Detection  
### A Comparative Deep Learning Study of Modern Architectures

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Deep Learning](https://img.shields.io/badge/Deep%20Learning-CNN-red)
![YOLO](https://img.shields.io/badge/YOLO-v5%20to%20v12-green)
![Faster R-CNN](https://img.shields.io/badge/Faster%20R--CNN-Two--Stage-orange)
![Medical AI](https://img.shields.io/badge/Medical%20Imaging-AI-critical)
![Status](https://img.shields.io/badge/Status-Research%20Completed-success)
![License](https://img.shields.io/badge/License-Academic-lightgrey)

---

## 📌 Overview

This repository presents the implementation and comparative evaluation of **state-of-the-art deep learning object detection models** for **colorectal polyp detection** in colonoscopy images.

The work is based on my **Master’s Thesis**:

> **Advanced Colorectal Polyp Detection: A Comparative Deep Learning Study of Modern Architectures**  
> *Master’s Program in Mechanical and Electro-Mechanical Engineering*  
> *Ming Chi University of Technology*  
> *November 2025*

---

## 🎯 Motivation

Colorectal cancer (CRC) is one of the leading causes of cancer-related mortality worldwide.  
Since **colorectal polyps** are primary precursors of CRC, **early and accurate detection** is critical.

Traditional colonoscopy suffers from:
- Operator dependency  
- Fatigue-related missed detections  
- Difficulty detecting small, flat, or low-contrast polyps  

This project explores how **modern deep learning detectors** can improve detection accuracy and reliability in real-time clinical settings.

---

## 📂 Dataset

- **Dataset Used:** Kvasir-SEG  
- **Images:** 1,000 original colonoscopy images  
- **Final Dataset Size:** 2,399 images (after augmentation)  
- **Annotations:** Bounding boxes created using **Roboflow**

### 🔄 Data Augmentation
Applied to improve robustness and generalization:
- Horizontal flipping  
- Saturation adjustment (±25%)  
- Exposure adjustment (±10%)  
- Auto-orientation  
- Resize to **640 × 640**

### 📊 Dataset Split
| Split | Images | Percentage |
|-----|------|------------|
| Training | 2099 | 87.5% |
| Validation | 200 | 8.2% |
| Testing | 100 | 4.3% |

---

## 🧪 Models Evaluated

A total of **7 object detection models** were implemented and compared:

| Model | Type |
|------|------|
| Faster R-CNN | Two-Stage Detector |
| YOLOv5 | Single-Stage |
| YOLOv8 | Anchor-Free |
| YOLOv9 | GELAN + PGI |
| YOLOv10 | Re-parameterized |
| YOLOv11 | Transformer-CNN Hybrid |
| YOLOv12 | Modular & Scalable |

---

## ⚙️ Experimental Setup

- **Platform:** Google Colab  
- **Image Size:** 640 × 640  
- **Epochs:** 50  
- **Batch Size:** 16  
- **Optimizers:**
  - Faster R-CNN & YOLOv5 → SGD  
  - YOLOv8–YOLOv12 → AdamW  
- **Hardware:**  
  - Intel® Core™ i9-12900K  
  - 32 GB RAM  
  - Windows 11 Pro (64-bit)

---

## 📈 Evaluation Metrics

To ensure reliable medical evaluation, the following metrics were used:

- Precision  
- Recall  
- F1-Score  
- mAP@0.5  
- mAP@[0.5:0.95]  
- Confusion Matrix  
- Precision-Recall Curve  
- Statistical Validation:
  - **95% Confidence Interval**
  - **Two-Proportion Z-Test (p < 0.05)**

---

## 🏆 Key Results

- **YOLOv11 achieved the best overall performance**
  - Precision > **90%**
  - Stable recall
  - mAP@0.5 > **90%**
- Faster R-CNN showed strong localization but lower recall
- Modern YOLO versions consistently outperformed earlier models
- Statistical Z-test confirmed YOLOv11’s superiority with **significant confidence**

---

## 📌 Conclusion

This study demonstrates that **modern YOLO architectures**, particularly **YOLOv11**, provide:
- High accuracy
- Real-time inference capability
- Robust detection under challenging medical imaging conditions

The results strongly support the adoption of **YOLO-based AI systems** for **computer-aided colorectal cancer screening**.

---

## 🚀 Future Work

- Real-time video-based polyp detection  
- Cross-dataset generalization testing  
- Integration into live colonoscopy systems  
- Lightweight deployment on edge/embedded devices  

---

## 👨‍🎓 Author

**M. David Honesty Babu**  
Graduate Student  
Ming Chi University of Technology  

---

## 📜 License

This repository is intended for **academic and research purposes only**.  
For clinical or commercial usage, proper validation and approvals are required.

---

⭐ *If you find this research useful, consider giving the repository a star!*
