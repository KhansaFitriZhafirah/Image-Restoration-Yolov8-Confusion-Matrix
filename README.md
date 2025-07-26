# 🖼️ Restoring Image Quality Using Filtering Methods and Evaluating with YOLOv8 Confusion Matrix

This repository contains the final project for the **Digital Image Processing** course at IPB University. This project explores various image restoration techniques (mean, median, Gaussian filters) applied to noisy images, followed by image classification performance evaluation using YOLOv8 and confusion matrix analysis.

---

## 📌 Project Overview

- **Goal**: To apply different types of noise to images (Gaussian, Salt & Pepper, Rayleigh), restore them using filtering techniques, and evaluate image classification accuracy using YOLOv8.
- **Approach**:
  1. Add artificial noise to clean images.
  2. Apply restoration filters (mean, median, Gaussian).
  3. Train YOLOv8 classification model on both original and restored datasets.
  4. Evaluate using confusion matrix metrics: Accuracy, Precision, Recall, F1-Score.

---

## 🧪 Methodology

### 🖼️ 1. Image Degradation
- Types of noise added:
  - Gaussian Noise
  - Salt & Pepper Noise
  - Rayleigh Noise

### 🧹 2. Filtering Techniques for Restoration
- **Mean Filter**
- **Median Filter**
- **Gaussian Filter**

### 🤖 3. Object Detection with YOLOv8
- YOLOv8 classification model trained on:
  - Original images
  - Noisy images
  - Restored images
- Evaluation metrics derived from confusion matrix:
  - Accuracy, Precision, Recall, F1-Score

---

## 📊 Results Summary

The evaluation was conducted across three types of image conditions:
1. **Original (clean) images**
2. **Noisy images** with various types of noise
3. **Restored images** using different filtering techniques

The YOLOv8 **image classification model** was trained to classify images into three categories: _Good_, _Moderate_, and _Poor_.

| Dataset Condition         | Accuracy | Precision | Recall | F1-Score |
|---------------------------|----------|-----------|--------|----------|
| Original (clean)          | 91.25%   | 0.91      | 0.91   | 0.91     |
| Noisy (Gaussian)          | 68.20%   | 0.67      | 0.68   | 0.67     |
| Restored (Gaussian Filter)| 84.15%   | 0.83      | 0.84   | 0.83     |
| Noisy (Salt & Pepper)     | 65.10%   | 0.64      | 0.65   | 0.64     |
| Restored (Median Filter)  | **88.50%** | **0.88**  | **0.89** | **0.88** |
| Noisy (Rayleigh)          | 69.00%   | 0.68      | 0.69   | 0.68     |
| Restored (Mean Filter)    | 79.40%   | 0.78      | 0.79   | 0.78     |

### 🔍 Key Findings
- 🟩 The **Median filter applied to Salt & Pepper noise** yielded the highest restoration performance, achieving **88.50% classification accuracy**, closely approaching the original clean dataset's performance of **91.25%**.
- 🧠 Restoration filters **significantly improved classification performance**, with up to **20% gain in accuracy** compared to noisy images without restoration.
- ⚠️ The worst performance was observed on Rayleigh-noised images without restoration, highlighting the importance of using the right filter based on the noise type.

---

## 🛠️ Tools & Technologies

- Python, OpenCV, NumPy, Matplotlib
- Ultralytics YOLOv8
- Google Colab / Jupyter Notebook


