# 👕 Team 22471A05 — Smart Apparel Narrator

A deep learning–based system for **automatic caption generation of apparel images and videos** using **ConvNeXt-Large + LSTM architectures**.  
The project focuses on building a **robust, scalable, and deployment-ready fashion captioning pipeline** for e-commerce automation, accessibility support, and intelligent retail analytics.

---

# 👥 Team Info

### 22471A05A0 — Kanumuri Narendra
🔗 LinkedIn: https://www.linkedin.com/in/narendra-kanumuri-6b4649276/  
**Work Done:** Designed the overall system architecture and implemented the ConvNeXt–LSTM captioning pipeline. Developed image/video preprocessing, feature extraction, caption generation, and end-to-end model training.

---

### 22471A05B1 — Nallamekala Vignesh
🔗 LinkedIn: https://www.linkedin.com/in/nallamekala-vignesh-9b992a361/  
**Work Done:** Performed dataset collection, cleaning, and preprocessing. Handled caption text processing, tokenization, padding, and conducted model evaluation using BLEU metrics and performance analysis.

---

### 22471A05B8 — Peddipaka Udaykiran
🔗 LinkedIn: https://www.linkedin.com/in/uday-kiran-65bb88282/  
**Work Done:** Implemented video frame extraction using OpenCV, integrated feature extraction and inference pipeline, optimized training workflow, and supported deployment and visualization modules.

---

# 📌 Abstract

This paper presents a deep learning-based framework named **Smart Apparel Narrator**, designed to automatically generate meaningful captions for fashion apparel in both images and videos. The system integrates a **ConvNeXt-Large encoder** for extracting detailed apparel features and an **LSTM decoder** for coherent caption generation.

For video sequences, the model applies **frame-level feature alignment** to capture dynamic apparel movements and maintain temporal consistency.

A filtered dataset containing **1,000+ annotated apparel images and clips across 26 fashion categories** was used for experimentation. The proposed method achieved strong balanced BLEU scores:

- BLEU-1: 0.946  
- BLEU-2: 0.932  
- BLEU-3: 0.924  
- BLEU-4: 0.917  

The framework supports:
- Automated e-commerce tagging  
- Assistive narration for visually impaired users  
- Fashion video analysis  
- Digital catalog management  

---

# 📄 Paper Reference (Inspiration)

👉 **Image and Video Captioning for Apparels Using Deep Learning**  
Authors: Govind Agarwal, Kritika Jindal, Abishi Chowdhury, Vishal K. Singh, Amrit Pal  
https://ieeexplore.ieee.org/document/10636169

---

# 🚀 Our Improvements Over Existing Paper

### ❌ Removes frame-independent captioning
Generates context-aware captions instead of independent frame predictions.

### 📦 Larger & cleaner dataset
Uses 1000+ curated images vs 863 base images → better generalization.

### 🔄 Frame-level feature alignment
Maintains temporal consistency and reduces caption flickering.

### 🧠 ConvNeXt-Large encoder
Captures fine-grained fashion details (texture, fabric, pattern, color).

### ✍️ Improved linguistic fluency
Cleaner captions with better grammar and longer meaningful sentences.

### 📊 Balanced BLEU evaluation
0.946 / 0.932 / 0.924 / 0.917  
Ensures sentence-level coherence instead of unigram-only accuracy.

---

# 🧩 About the Project

This project implements a **deep learning–based apparel captioning system** capable of automatically generating **natural language descriptions for clothing images and videos**.

### Applications
- E-commerce automation  
- Accessibility support  
- Fashion video narration  
- Smart retail analytics  

---

# 🔁 Workflow

Input Image / Video  
→ Preprocessing  
→ ConvNeXt (Feature Extraction)  
→ LSTM (Caption Generation)  
→ Output Caption  

---

# 📊 Dataset Used

👉 **Fashion Product Images Dataset (Kaggle)**  
https://www.kaggle.com/datasets/paramaggarwal/fashion-product-images-dataset  

### Dataset Details
- ~44,000+ real-world apparel images  
- Multiple fashion categories  
- Rich metadata (gender, type, color, usage)  
- Suitable for captioning and classification tasks  

---

# 🧰 Dependencies Used

- 🐍 Python  
- 👁️ OpenCV  
- 🔥 TensorFlow / Keras  
- 🧠 ConvNeXt-Large  
- 🔁 LSTM  
- 📊 NumPy  
- 📁 Pandas  
- 📝 Tokenizer  
- 📉 NLTK (BLEU)  
- 🎨 Matplotlib  
- 💻 Google Colab / Jupyter  

---

# 🔍 EDA & Preprocessing

- Images converted to RGB format  
- Resized to 299×299 / 512×512  
- Corrupted/duplicate images removed  
- Dataset balance checked  
- Captions cleaned & tokenized  
- Padding applied  
- ConvNeXt feature extraction  
- Video frames processed individually  

---

# 🧪 Model Training Info

- ConvNeXt generates feature embeddings  
- LSTM performs sequential caption generation  
- Cross-Entropy loss  
- Adam optimizer  
- Teacher forcing  
- 30 training epochs  
- BLEU-1 to BLEU-4 evaluation  

---

# 🧾 Model Testing / Evaluation

### Metrics Used
- BLEU-1  
- BLEU-2  
- BLEU-3  
- BLEU-4  

### Compared With
- CNN–LSTM baseline  
- Attention-based models  
- Transformer models  

---

# 🏆 Results

### Apparel Captioning
- BLEU-1: 0.946  
- BLEU-2: 0.932  
- BLEU-3: 0.924  
- BLEU-4: 0.917  

### Highlights
- Smooth video narration  
- Reduced caption flickering  
- ~150 ms/frame inference  
- Human-like descriptions  
- Suitable for real-time deployment  

---

# ⚠️ Limitations & Future Work

### Limitations
- High GPU requirements  
- Slight latency for long videos  
- Performance may drop in complex scenes  

### Future Enhancements
- Real-time optimization  
- Larger datasets  
- Transformer/attention models  
- Web/mobile deployment  
- Multilingual captions  
- Text-to-speech integration  

---

# 🌍 Deployment Info

- Python backend  
- ConvNeXt + LSTM inference  
- CUDA GPU acceleration  
- OpenCV video processing  
- Flask / FastAPI deployment  
- Batch image/video support  

---

# ✨ Project By
👨‍💻 Narendra Kanumuri
👨‍💻 Nallamekala Vignesh
👨‍💻 Peddipaka Udaykiran
🎓 Smart Apparel Narrator — Deep Learning-Based Apparel Captioning System
