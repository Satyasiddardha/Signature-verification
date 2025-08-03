# Signature Verification System

This project is a Flask-based web application that uses computer vision and machine learning techniques to **verify the authenticity of a signature**. It compares an original signature image against a potentially forged one using **Histogram of Oriented Gradients (HOG)** features and **cosine similarity**.

---

## Features

- Upload original and suspected forged signature images via a simple web interface.
- Automatic preprocessing: grayscale conversion, resizing, and denoising.
- Feature extraction using HOG.
- Signature similarity comparison using cosine similarity metric.
- Real-time decision on whether the signature is genuine or possibly forged.

---

## How It Works

1. **Image Preprocessing**  
   Converts the uploaded images to grayscale, resizes to a fixed dimension, and applies Gaussian blur to reduce noise.

2. **Feature Extraction**  
   Uses `skimage.feature.hog` to extract features that represent the texture and structure of the signature.

3. **Similarity Check**  
   Computes cosine similarity between feature vectors of both signatures. If the similarity exceeds a threshold (0.9), the signature is considered genuine.

---

## Tech Stack

- **Backend:** Python, Flask  
- **Computer Vision:** OpenCV, scikit-image  
- **Machine Learning:** scikit-learn (cosine similarity)  
- **Frontend:** HTML, JavaScript (with base64 encoded image sending)

---

