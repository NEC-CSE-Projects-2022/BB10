# 👕 Smart Apparel Narrator — Deep Learning-Based Captioning for Images and Videos

Repository for the **Smart Apparel Narrator**, a deep learning framework that automatically generates **natural language captions for apparel images and videos** using computer vision and sequence modeling.

---

## 📌 Summary

### Two main functions:

1. 🖼 Image Captioning  
   → Generate descriptive captions for apparel images

2. 🎥 Video Captioning  
   → Generate continuous frame-by-frame narration for apparel videos

---

## 🔑 Key Components

- ConvNeXt-Large → Visual feature extraction (encoder)
- LSTM Decoder → Sequential caption generation
- YOLOv8 → Apparel detection & region cropping (optional)
- BLEU Metrics → Caption quality evaluation
- TensorFlow / Keras / PyTorch → Deep learning frameworks
- OpenCV → Image & video preprocessing

---

## 📂 Repository Contents

- CAMERA_READY_PAPER.pdf  
  → Final research paper describing methodology and results  

- BB10_ABSTRACT.pdf  
  → Project abstract and overview  

- BB10_CONF.pptx  
  → Conference presentation  

- BB10_COLLEGE_REVIEW.pptx  
  → Review presentation  

- BB10_PROJECT_DOCUMENT.pdf  
  → Complete documentation (design, implementation, experiments)

---

## 🧠 Quick System Description

### Input (Image)
User uploads apparel image  
→ Preprocessing  
→ ConvNeXt extracts features  
→ LSTM generates caption  
→ Text description output

### Input (Video)
User uploads video  
→ Frame extraction  
→ Feature alignment  
→ Caption per frame  
→ Smooth narration output

---

## ⚙️ Workflow

Image / Video  
→ Preprocessing  
→ ConvNeXt Encoder (Feature Extraction)  
→ LSTM Decoder (Caption Generation)  
→ Output Caption

---

## 🗂 Dataset Used

- Fashion Apparel Dataset (26 categories)
- 1000+ annotated images & clips
- Manually curated captions

Used for:
- Apparel captioning
- Fashion understanding
- E-commerce automation

---

## 🧰 Models & Tools

- ConvNeXt-Large (CNN encoder)
- LSTM (sequence decoder)
- YOLOv8 (object detection)
- TensorFlow / PyTorch
- OpenCV
- NumPy
- Pandas
- NLTK (BLEU evaluation)
- Matplotlib

---

## 💻 Environment & Hardware

### Software
- Python 3.x
- Google Colab / Jupyter
- Browser: Chrome
- OS: Windows 7 or later

### Hardware
- Intel Core i5 or above
- RAM: 8GB+
- GPU: NVIDIA T4 (Colab)

---

## 📊 Evaluation & Performance

### Metrics
- BLEU-1
- BLEU-2
- BLEU-3
- BLEU-4

### Reported Results
- BLEU-1: 0.946
- BLEU-2: 0.932
- BLEU-3: 0.924
- BLEU-4: 0.917

### Highlights
- High caption accuracy
- Human-like descriptions
- Stable training convergence
- Smooth video narration
- Real-time capable

---

## 🚀 Installation

### Clone repo
```bash
git clone <repo-url>
cd <repo>
```

### Create virtual environment
```bash
python -m venv .venv
source .venv/bin/activate
```

### Install dependencies
```bash
pip install -r requirements.txt
```

---

## ▶ Usage Examples

### Image Captioning
```bash
python caption_image.py --image path/to/image.jpg
```

### Video Captioning
```bash
python caption_video.py --video path/to/video.mp4
```

---

## 🔬 Research Contributions

- ConvNeXt + LSTM hybrid architecture
- Frame-level feature alignment for videos
- Fashion-specific dataset
- Balanced BLEU evaluation
- Real-time deployment ready

---

## 📈 Applications

- E-commerce product description automation
- Assistive narration for visually impaired users
- Fashion catalog management
- Smart retail analytics
- Video content understanding

---

## 🔮 Future Work

- Transformer-based captioning
- Attention mechanisms
- Larger datasets
- Real-time optimization
- Mobile/edge deployment
- Multilingual captions

---

## 👥 Team

### 22471A05A0 — Kanumuri Narendra
System architecture, ConvNeXt–LSTM pipeline, training & integration

### 22471A05B1 — Nallamekala Vignesh
Dataset preprocessing, tokenization, evaluation, analysis

### 22471A05B8 — Peddipaka Udaykiran
Video processing, OpenCV pipeline, optimization, deployment

---

## 🎓 Guide
Marella Venkata Rao, M.Tech

---

## 📧 Contact
narendrakanumurib@gmail.com

---

## 📜 License
Academic & Research Use Only

