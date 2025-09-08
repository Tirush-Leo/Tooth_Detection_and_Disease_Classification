# 🦷 Tooth Disease Detection & Classification

## 📌 Project Overview
This repository contains the ongoing research project on **automated tooth detection, enumeration, and disease classification** using **deep learning**. 

![Pectoral_Muscle_Removal](https://drive.google.com/uc?export=download&id=1_ressZQ8XhVIXI7g6FPKejYzmkpjPOJa)


⚠️ **Important note:**  
The code and results are **not included at this stage** because the research paper is still being written. Once the paper is completed and submitted to a conference, the full implementation and results will be uploaded here.

---

## 🔬 Technical Framework

### 1. Tooth Detection (Quadrant & Enumeration)
- **Model:** YOLO-based object detector  
- **Tasks:**
  - Detect four quadrants of the dental arch (Q1–Q4)  
  - Enumerate individual teeth (using FDI / Universal numbering system)  
- **Input:** Panoramic / periapical dental radiographs  
- **Output:** Bounding boxes for quadrants and each tooth  

### 2. Disease Classification
- **Model:** ResNet-50 backbone pretrained on **RadImageNet** (1.35M medical images)  
- **Fine-tuning:** Progressive unfreezing with AdamW, cosine LR scheduling, and label smoothing  
- **Target Classes (example):**
  - Healthy  
  - Caries  
  - Pulpitis  
  - Periodontitis  
  - Calcification  

### 3. Integrated Pipeline
1. **YOLO stage** → Detects quadrants & enumerates teeth  
2. **Cropping** → Extracts tooth regions  
3. **Classifier stage** → RadImageNet model predicts disease label  
4. **Output** → JSON/CSV with quadrant, tooth ID, bounding box, and disease prediction  

---

## ⚙️ Advanced Techniques
- Mixed precision (AMP) training  
- Exponential Moving Average (EMA) of weights  
- Strong data augmentations (Mosaic, MixUp, HSV jitter, flips, random crops)  
- Label smoothing & Focal loss for class imbalance  
- Cosine learning rate scheduling with warmup  
- Early stopping and checkpointing  

---

## 📂 Repository Plan
- 📄 **Research Paper (in progress):** Being written for conference submission  
- 💻 **Code & Models:** To be uploaded after paper submission  
- 📊 **Results & Analysis:** Will be added post-publication  

---

🚨 **Note:**  
Code and results are not included here because the research paper is **still in progress**. Everything will be made available after submission.
