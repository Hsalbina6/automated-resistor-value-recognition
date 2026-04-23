# Automated Resistor Value Recognition

## Executive Summary
This project develops a computer vision system for automated resistor value recognition. The goal is to reduce manual interpretation errors and improve speed and reliability in identifying resistor values under real-world conditions.

The solution uses a dual-model approach. The first model detects resistor color bands using YOLO and estimates values based on band combinations. The second model classifies the most common resistor values directly. A decision logic layer is used to improve robustness when the two models disagree.

This repository serves as the official project handover. It is structured so that any stakeholder can understand, reproduce, and extend the work without direct supervision.

---

## Business Problem
Manual resistor identification is prone to error, especially under conditions such as poor lighting, rotation, and visual ambiguity. These errors can lead to incorrect circuit assembly, increased debugging time, and reduced system reliability.

An automated system can improve consistency, reduce human error, and support faster engineering workflows.

---

## Proposed Solution
This project implements:

- A YOLO-based model for resistor band detection  
- A classification model for common resistor values  
- A decision logic layer to resolve conflicts between model outputs  

This combined approach improves reliability compared to using a single model.

---

## Repository Structure
- `notebooks/` → Jupyter notebooks for data preparation, training, and evaluation  
- `data/` → Dataset description and access link  
- `outputs/` → Generated figures, predictions, and reports  
- `assets/` → Visuals and reference images  
- `src/` → Supporting Python functions  

---

## How to Run

### 1. Install Dependencies
```bash
pip install -r requirements.txt
