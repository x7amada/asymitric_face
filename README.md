# Facial Asymmetry Detection using Deep Learning (CNN)

## Overview
This project focuses on detecting facial asymmetry for medical diagnosis, particularly conditions such as facial paralysis (e.g., Bell’s palsy).  
Using deep learning techniques, multiple Convolutional Neural Network (CNN) architectures were implemented and compared to identify the most effective model.

---

## Objectives
- Detect facial asymmetry using image-based deep learning models  
- Compare multiple CNN architectures to find the best-performing model  
- Analyze which facial regions contribute most to asymmetry detection  

---

## Methodology
- Implemented and compared **4 different CNN-based models**
- Used **MTCNN** for face detection and preprocessing  
- Created multiple datasets:
  - Full face dataset  
  - Upper face dataset  
  - Lower face dataset  
- Trained models using **Google Colab (GPU)**  
- Optimized training using:
  - Adam optimizer  
  - CrossEntropyLoss  
  - Data augmentation (rotation, flipping)  

---

## Dataset
- Total images: **2825 facial images** :contentReference[oaicite:0]{index=0}  
- Two dataset types:
  - **Binary classification (2 classes):**
    - Symmetrical (1005 images)  
    - Asymmetrical (1820 images)  
  - **Multi-class classification (6 classes):**
    - Normal  
    - Near Normal  
    - Mild Dysfunction  
    - Moderate Dysfunction  
    - Severe Flaccid  
    - Complete Flaccid  

- Train/Test split: **80% / 20%**

---

## Models Compared
1. Four-layer CNN (Tanoy Debnath)  
2. InceptionResNetV2  
3. Custom CNN (Abir Fathallah)  
4. CNN with K-Fold training (Chindy Aulia Sari)  

---

## Results
-  Best model: **Four-layer CNN**
-  Achieved accuracy: **~96%** :contentReference[oaicite:1]{index=1}  

### Face Region Comparison:
- Full face: **96.46% accuracy**  
- Lower face: **67% accuracy**  
- Upper face: **56% accuracy**  

 Conclusion: **Full face provides the most reliable features for asymmetry detection**

---

##  Tech Stack
- Python  
- PyTorch / Deep Learning libraries  
- OpenCV  
- MTCNN (face detection)  
- Google Colab (GPU training)  

---

##  How to Run
```bash
# Clone repository
git clone https://github.com/yourusername/facial-asymmetry-detection

# Install dependencies
pip install -r requirements.txt

# Run training
python train.py
