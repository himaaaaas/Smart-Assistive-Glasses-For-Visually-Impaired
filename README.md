# Smart Assistive Glasses for the Visually Impaired

This project presents an integrated AI-powered assistive system designed to support blind and visually impaired individuals in their daily lives. It combines real-time computer vision, offline processing, and mobile connectivity through smart glasses and a companion Flutter application.

---

## Project Overview

Millions of people globally and over 3 million in Egypt alone suffer from visual impairment. This system addresses their mobility and independence by combining Raspberry Pi-powered smart glasses with object detection, face recognition, currency recognition, and OCR capabilities.

The system offers real-time **audio feedback** based on the user’s visual surroundings and features a mobile app for remote assistance and text reading. 

---

## 🧠 System Features

### 🧍‍♂️ Face Recognition
- Recognizes familiar individuals using Dlib’s 128D face embeddings.
- Works entirely offline and responds with audio using `espeak`.
- Trained using a group dataset with individual folders per person.

### 📦 Object Detection
- Utilizes YOLOv5 trained on COCO 2017 dataset (80 classes).
- Real-time detection and spatial awareness (person, car, chair, etc.).
- Operates on Raspberry Pi 5 with a compressed NCNN model.

### 💰 Currency Recognition
- Custom YOLOv11 model trained on Egyptian pound banknotes.
- Accurate denomination detection (e.g., 10, 50, 100 EGP).
- Provides fast voice feedback (~1.2 seconds/frame).

### 🔠 OCR (Text Detection)
- Glasses: EasyOCR supports Arabic and English.
- Mobile App: Google ML Kit performs OCR offline.
- Useful for reading labels, signs, medicine boxes, and receipts.

---

## 📱 Mobile App (Flutter)

- Built using Flutter for Android.
- Features:
  - Real-time OCR via camera.
  - Chat interface for reaching out to volunteers.
  - Text-to-speech and speech-to-text for full voice control.
- Clean, accessible UI for visually impaired users.

---

## 🧪 Results and Evaluation

| Feature              | Metric                       | Result       |
|----------------------|------------------------------|--------------|
| Face Recognition     | Accuracy                     | ~90%         |
| Object Detection     | mAP@0.5                      | 87.5%        |
| Currency Detection   | mAP@0.5                      | **94.7%**    |
| OCR (EasyOCR)        | WER / CER                    | Low WER (~9%)|
| Audio Response Time  | Glasses + TTS (espeak)       | ~1.0–1.2 s   |

📊 Performance plots, confusion matrix, and demo images are in the [`results/`](./results) folder.

---

## 🧰 Hardware Architecture

- 📷 Raspberry Pi 5 (2.4 GHz Quad-Core ARM Cortex-A76)
- 🌀 Active Cooler for Pi 5
- 📸 Kisonli Full HD USB Webcam
- 🎮 Analog Joystick Module
- 🔋 Lithium-Ion Battery Pack for portability
- 🦾 Arduino Uno with 3x HC-SR04 Ultrasonic Sensors (for Smart Cane)
- 🎛️ Custom 3D Printed Enclosure (Glasses, Cane, and Pi case)

---

## 🖼️ Visuals & Documentation

- 📄 [Poster Presentation (PDF)](./docs/poster.pdf)
- 🧠 [System Architecture Diagram](./docs/system_architecture.png)
- 🔁 [Currency Model Confusion Matrix](./results/confusion_matrix.png)
- 📊 [Precision/Recall Curve](./results/precision_recall_curve.png)
- 🎥 [Smart Glasses Demo](./results/smart_glasses_demo.gif)

---

## 📂 Folder Structure

