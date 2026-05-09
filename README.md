


🫁 Chest X-ray Disease Detection using Deep Learning (NIH Dataset)
📌 Project Overview

dataset:https://www.kaggle.com/datasets/nih-chest-xrays/data/



This project is a multi-label deep learning system for detecting thoracic diseases from chest X-ray images using the NIH Chest X-ray dataset. The model predicts multiple conditions such as Atelectasis, Effusion, Cardiomegaly, Mass, and Nodule from a single X-ray image.

🧠 Problem Statement

Chest X-ray diagnosis is:

time-consuming
prone to human error
highly dependent on radiologist expertise

This project explores how deep learning can assist radiologists by providing automated multi-label predictions.

⚙️ Tech Stack
Python 🐍
PyTorch 🔥
Torchvision
NumPy
Matplotlib
Scikit-learn
NIH Chest X-ray Dataset
🏗️ Model Architecture
CNN-based deep learning model (or DenseNet/ResNet if used)
Multi-label classification setup
Activation: Sigmoid
Loss Function: BCEWithLogitsLoss
📊 Training Results
Training Performance
Epoch 1–10
Loss: ~0.167
Accuracy: ~94.8%
Validation Performance
Validation Accuracy: 94.78%
Validation Loss: 0.1685
⚠️ Important Observation

Despite high accuracy, the model shows:

Low macro F1-score (~0.10–0.28)
Poor performance on rare disease classes
Strong dataset imbalance effect
📌 Key Insight:

Accuracy is misleading due to class imbalance. Macro-F1 reveals true performance gaps across disease classes.

📉 Classification Report Summary
Majority class dominates predictions
Rare diseases have near-zero recall
Model biased toward common findings
🧪 Sample Prediction Output
Cardiomegaly: 39.18%
Effusion: 29.96%
Atelectasis: 28.73%
🧠 Key Learnings
NIH dataset is highly imbalanced
Accuracy alone is NOT sufficient for medical AI
Multi-label classification requires:
Sigmoid activation
Threshold tuning
Evaluation should prioritize:
F1-score
AUROC
Per-class metrics
🚀 Future Improvements
Add Class Imbalance Handling (pos_weight / focal loss)
Integrate DenseNet121 (medical-grade architecture)
Add Grad-CAM explainability
Build FastAPI inference backend
Deploy Next.js medical dashboard UI
📷 Sample Pipeline
X-ray Image → CNN Model → Sigmoid → Disease Probabilities → Thresholding → Final Report
👨‍💻 Author

Built as an AI/ML engineering project focusing on:

Medical Imaging AI
Deep Learning Systems
Real-world dataset challenges
