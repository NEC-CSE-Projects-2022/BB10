# 👕 BB10 Smart Apparel Narrator — Frontend Overview

A clear, professional README for the frontend of the **Smart Apparel Narrator** project.  
This document describes the project structure, how to run the app locally, the **AI models used**, and the **input image/video preprocessing & validation** performed before caption generation.

---

## Table of contents

- Project Structure
- How to run (Frontend)
- Folder & file explanations
- Models used
- Input validation (Apparel image/video validation)
- Frontend Screenshots
- Notes

---

## Project Structure

- **Source Code**
  - **app.py** — Flask server entrypoint (routes, caption inference, preprocessing, uploads)
  - **requirements.txt** — Python dependencies

- **Templates & UI**
  - **templates/** — HTML templates (home, upload, results, history, etc.)
  - **static/** — CSS/JS assets and uploaded media

- **Models & Data**
  - **models/** — trained captioning model weights (`fashion_caption_model.pth`)
  - **Datasets/** — training/testing images & metadata

- **Screenshots**
  - **images/** — frontend screenshots used in this README

---

## How to run (Frontend)

### 1) Create and activate a virtual environment

```bash
python -m venv .venv
.venv\Scripts\activate
```

---

### 2) Install dependencies

```bash
pip install -r requirements.txt
```

---

### 3) Start the app

```bash
python app.py
```

Open the address printed by Flask (commonly):

```
http://127.0.0.1:5000
```

---

## Folder & file explanations

### templates/
- Contains all HTML pages rendered by Flask.
- Pages include:
  - Home
  - Upload Image
  - Upload Video
  - Caption Results
  - History / Gallery

### static/
- Contains styling and client-side scripts.
- `static/uploads/` stores uploaded images/videos temporarily.

### models/
- Contains trained model weights:
  - `fashion_caption_model.pth`

### images/
- Stores UI screenshots displayed in this README.

---

## Models used

The backend uses a deep learning captioning pipeline with the following components:

### 🧠 ConvNeXt-Large (Encoder)
- Extracts deep visual features from apparel images
- Captures texture, color, fabric, and design details

### 🔁 LSTM Decoder
- Generates captions word-by-word
- Produces natural language descriptions

### 📹 Video Frame Processing (OpenCV)
- Splits videos into frames
- Applies captioning on each frame
- Ensures smooth narration

### 📊 BLEU Metrics
- Evaluates caption quality (BLEU-1 to BLEU-4)

---

## Input validation (Apparel image/video validation)

Before running inference, the system validates uploaded media to ensure meaningful caption generation.

Validation includes:

### For Images
- File type check (jpg/png/jpeg)
- Minimum resolution check
- RGB conversion
- Corrupted image detection
- Apparel presence verification (basic heuristics)

### For Videos
- Valid format (mp4/avi/mov)
- Frame extraction success
- Duration limit checks
- Frame quality filtering

If validation fails:
- User receives a clear error message
- Captioning is not executed

---

## System Workflow

```
User Upload (Image/Video)
        ↓
Preprocessing & Validation
        ↓
ConvNeXt Feature Extraction
        ↓
LSTM Caption Generation
        ↓
Final Text Caption Output
```

---

## Features

- Image caption generation
- Video frame-by-frame narration
- Real-time inference
- Multiple uploads support
- Clean web interface
- GPU acceleration (Colab/local CUDA)

---

## Frontend Screenshots

Below are the screenshots currently in `images/`.  
Each image can be added to visually demonstrate the interface.

| 1 | 2 |
|---|---|
| Home page | Upload page |

| 3 | 4 |
|---|---|
| Caption result | Video narration result |

Suggested captions:
- **1** — Welcome/Home page
- **2** — Upload image/video page
- **3** — Generated caption display
- **4** — Video frame narration view

---

## Notes

- Designed for academic/research purposes
- Requires GPU for faster inference
- Model file is large → hosted externally (Google Drive)
- Do not commit large weights to GitHub

---

## Maintainer

Kanumuri Narendra  
📧 narendrakanumurib@gmail.com

---

## License

Academic & Research Use Only

