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

## How to Run the Project

1. **Install Requirements**
   ```bash
   pip install -r CODE/requirements.txt

    ```
### 2. Open the Notebook
Open `CODE/Specialist_Model (2).ipynb`.
* **Recommended environment:** Google Colab

### 3. Load Dataset and Model
Use the instructions inside `data/external_links/Dataset_and_Model_Access.txt`.

### 4. Run YOLO Training or Prediction
The notebook includes the full YOLO workflow for training, evaluation, prediction, and saving model outputs.

---

## Streamlit Deployment
A deployed app version of the project is available. Links are provided here: `streamlit/links.txt`

This file includes:
* Live Streamlit app link
* Separate Streamlit repository link
* Short description of the deployed app

---

## OWLET AI Performance Evaluation
The `OWLET/` folder contains the AI assistant performance review materials:
* `OWLET_AI_Performance_Review.pdf`
* `OWLET_Code.ipynb` (Python code used to generate the report and visuals)

---

## Presentation Slides
The final project presentation is included as: `Presentation_Slides.pdf`

---

## Key Results
The **Specialist Model** showed strong performance in recognizing common resistor values. However, because the dataset was relatively small, results should be interpreted with caution.

The **Generalist Model** was explored but was less reliable because it required every individual color band to be detected correctly. Small errors in lighting, blur, shadows, or band order could lead to an incorrect final resistance value.

---

## Project Limitations
* Dataset size was limited
* Lighting and background variation affected predictions
* Generalist color-band detection was highly sensitive
* More data would improve model generalization
* Real-world deployment requires more testing across resistor types and image conditions

---

## Code Quality and Reproducibility

All notebooks in this repository have been cleaned and structured to ensure full reproducibility and clarity for any stakeholder.

- Experimental and scratchpad cells have been removed  
- Broken or unused code has been eliminated  
- Excessive logs and debugging outputs have been removed  
- The workflow is organized into clear, logical steps  

The dataset and model are accessed through external links with provided setup instructions, enabling the project to be fully reproduced in a new environment.

This repository is structured to function as a complete professional handover, allowing any user to understand, reproduce, and extend the project without direct supervision.

---

## Future Improvements
* Expand the dataset with more resistor values and conditions
* Improve the Generalist Model for color-band detection
* Add stronger image quality checks before prediction
* Improve the Streamlit interface with a guide box for positioning
* Test the model on images collected by other users

---

## Author
**Hassan Alshaikh** Master of Engineering Management and Leadership  
Rice University

