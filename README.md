# Automated Resistor Value Recognition

## Executive Summary
This project develops an AI-based system for automated resistor value recognition. The goal is to help students and users quickly identify resistor values from images instead of manually reading color bands, which can be tedious, time-consuming, and error-prone.

The project uses a YOLO-based computer vision workflow to detect and classify resistors. The main working model is the **Specialist Model**, which classifies whole resistors based on common resistor values. A second concept, the **Generalist Model**, was explored to detect individual color bands, but it was more sensitive to lighting, shadows, blur, and band-ordering errors.

This repository serves as the professional handover for the project. It includes the code, model access, dataset access, deployment links, presentation slides, and OWLET AI performance evaluation materials.

---

## Business Problem
Reading resistor color codes manually can slow down students during circuits labs and projects. Small visual differences, lighting conditions, and human error can lead to incorrect resistance values.

This project addresses the question:
**Can computer vision automate resistor value recognition from images and make the process faster and more reliable for students?**

---

## Proposed Solution
The solution uses a YOLO object detection model trained on resistor images captured under different conditions, including variations in:
- Lighting and shadows
- Reflections and backgrounds
- Orientation
- Multiple resistors in one image

The project focuses on building a practical AI workflow that can take an image of a resistor and return the predicted resistor value.

---

## Repository Structure
```text
.
├── CODE/
│   ├── Specialist_Model (2).ipynb
│   └── requirements.txt
│
├── data/
│   └── external_links/
│       └── Dataset_and_Model_Access.txt
│
├── streamlit/
│   └── links.txt
│
├── OWLET/
│   ├── OWLET_AI_Performance_Review.pdf
│   └── OWLET_Code.ipynb
│
├── Presentation_Slides.pdf
└── README.md

```
## Main Code
The main notebook is located in: `CODE/Specialist_Model (2).ipynb`

This notebook includes:
* Dataset loading
* YOLO setup
* Training workflow
* Validation and evaluation
* Prediction on new images
* Model export and reuse steps

## Dataset and Model Access
The dataset and trained model are not stored directly in this repository because of file size limits. Access links are provided here: `data/external_links/Dataset_and_Model_Access.txt`

This file includes:
* Google Drive dataset link
* Google Drive trained model link
* `gdown` setup code
* Model loading instructions




