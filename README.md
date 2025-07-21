# Smart Assistive Glasses for the Visually Impaired

This project presents an integrated AI-powered assistive system designed to support blind and visually impaired individuals in their daily lives. It combines real-time computer vision, offline processing, and mobile connectivity through smart glasses and a companion Flutter application.

---
![App](https://github.com/himaaaaas/Smart-Assistive-Glasses-For-Visually-Impaired/blob/main/assets./face_recognition%20.png?raw=true)

## Project Overview

Millions of people globally and over 3 million in Egypt alone suffer from visual impairment. This system addresses their mobility and independence by combining Raspberry Pi-powered smart glasses with object detection, face recognition, currency recognition, and OCR capabilities.

The system offers real-time **audio feedback** based on the user’s visual surroundings and features a mobile app for remote assistance and text reading. 

---

## 🧠 System Features

### Face Recognition
- Recognizes familiar individuals using Dlib’s 128D face embeddings.
- Trained using a custom dataset for the 5 memebers of the Graduation project group.

### Object Detection
- Utilizes YOLOv5 trained on COCO 2017 dataset (80 classes).
- Real-time detection and spatial awareness (person, car, chair, etc.).
- Operates on Raspberry Pi 5 with a compressed NCNN model.

###  Currency Recognition
- Custom YOLOv11 model trained on Egyptian pound banknotes.
- Accurate denomination detection (e.g., 10, 50, 100 EGP).


### OCR (Text Detection)
- Glasses: EasyOCR supports Arabic and English.
- Mobile App: Google ML Kit performs OCR offline.
- Useful for reading labels, signs, medicine boxes, and receipts.

---

## Mobile App (Flutter)

- Built using Flutter for Android.
- Features:
  - Real-time OCR via camera.
  - Chat interface for reaching out to volunteers.
  - Text-to-speech and speech-to-text for full voice control.
- Clean, accessible UI for visually impaired users.

---

##  Results and Evaluation

| Feature              | Metric                       | Result       |
|----------------------|------------------------------|--------------|
| Face Recognition     | Accuracy                     | ~90%         |
| Object Detection     | mAP@0.5                      | 87.5%        |
| Currency Detection   | mAP@0.5                      | **94.7%**    |
| OCR (EasyOCR)        | WER / CER                    | Low WER (~9%)|
| Audio Response Time  | Glasses + TTS (espeak)       | ~1.0–1.2 s   |

📊 Performance plots, confusion matrix, and demo images are in the [`results/`](./results) folder.

---

## Hardware Architecture

- Raspberry Pi 5 (2.4 GHz Quad-Core ARM Cortex-A76)
- Active Cooler for Pi 5
- USB Webcam
- Analog Joystick Module
- Lithium-Ion Battery Pack for portability

## Demo Video
https://drive.google.com/file/d/1KASD1EkjL27RphxghuvIEV594tcVakKQ/view?usp=drive_link



