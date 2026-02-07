
# Team Number – Project Title

👥 Team Info
- 22471A05A0 — Kanumuri Narendra ( [LinkedIn](https://www.linkedin.com/in/narendra-kanumuri-6b4649276/) )
Work Done: Designed the overall system architecture and implemented the ConvNeXt–LSTM captioning pipeline. Developed image/video preprocessing, feature extraction, caption generation, and end-to-end model training.

- 22471A05B1 — Nallamekala Vignesh ( [LinkedIn](https://www.linkedin.com/in/nallamekala-vignesh-9b992a361/) )
Work Done: Performed dataset collection, cleaning, and preprocessing. Handled caption text processing, tokenization, padding, and conducted model evaluation using BLEU metrics and performance analysis.

- 22471A05B8 —  Peddipaka Udaykiran ( [LinkedIn](https://www.linkedin.com/in/uday-kiran-65bb88282/) )
Work Done: Implemented video frame extraction using OpenCV, integrated feature extraction and inference pipeline, optimized training workflow, and supported deployment and visualization modules.


---

## Abstract
This paper presents a deep learning-based frame
work named Smart Apparel Narrator, designed to automatically
generate meaningful captions for fashion apparel in both images
and videos. The system integrates a ConvNeXt-Large encoder
for extracting detailed apparel features and an LSTM decoder
for coherent caption generation. For video sequences, the model
applies frame-level feature alignment to capture dynamic apparel
movements. A filtered dataset containing over 1,000 annotated
apparel images and clips across 26 fashion categories was used
for experimentation. The proposed method achieved a BLEU-1
score of 0.946, outperforming standard CNN–LSTM captioning
baselines and demonstrating high descriptive accuracy. This
framework offers significant potential for automated e-commerce
tagging, assistive narration for visually impaired users, and
fashion video analysis. Future extensions include attention-based
captioning and transformer architectures for enhanced context
retention. The Smart Apparel Narrator framework closes the
loop between computer vision and fashion understanding by
allowing machines to annotate clothes with human-like accuracy.
Different from conventional captioning systems designed for
common scenes, however, this method is solely concentrating
on fashion features like texture, pattern, material, and design
properties. The performance of the model showcases its flexibility
towards various apparel types while ensuring language fluency.
Through effective feature learning and context alignment, it
can produce context-aware and descriptive captions. It can
enable personalized fashion advice, digital catalog management,
and accessibility solutions. The study shows that combining
deep vision models with sequential text generation can enable
substantial improvement in user engagement with visual retail
information.

---

## Paper Reference (Inspiration)
👉 **[Paper Title Image and Video Captioning for
Apparels Using Deep Learning
  – Author Names GOVIND AGARWAL,KRITIKA JINDAL,ABISHI CHOWDHURY,VISHAL K. SINGH,AMRIT PAL
 ](https://ieeexplore.ieee.org/document/10636169)**



## Our Improvement Over Existing Paper
❌ Removes frame-independent captioning

Unlike the existing Image and Video Captioning for Apparels Using Deep Learning system, which captions each detected object/frame independently after YOLO-based detection, our model avoids isolated predictions. Instead, it generates context-aware captions, improving coherence across frames and reducing inconsistent descriptions.
📦 Larger & cleaner dataset

The previous work used 863 base apparel images (with augmentation).
Our system uses 1000+ carefully filtered and annotated images and video clips, providing:

better diversity

reduced noise

stronger generalization

improved real-world performance
🔄 Adds frame-level feature alignment (video continuity)

Instead of treating video frames separately, we introduce frame-level feature alignment:

preserves temporal consistency

reduces caption flickering

produces smooth narration for moving apparel

This results in stable and natural video descriptions.
🧠 Uses stronger visual encoder (ConvNeXt-Large specialization)

We employ ConvNeXt-Large as a dedicated encoder to capture:

texture

fabric

pattern

color

design details

This enables fine-grained fashion understanding, not just object detection.
✍️ Improves linguistic fluency

Enhanced caption preprocessing + tokenization + sequence learning:

cleaner vocabulary

better grammar

fewer repetitive words

longer meaningful sentences

Captions become human-like and descriptive, instead of short labels.
Balanced evaluation (not just unigram accuracy)

The existing model focuses mainly on high BLEU-1.
Our system achieves balanced BLEU-1 to BLEU-4:

0.946 / 0.932 / 0.924 / 0.917


This shows:

better multi-word consistency

stronger sentence structure

improved contextual correctness


---
##🧩 About the Project

This project implements a deep learning–based apparel captioning system capable of automatically generating natural language descriptions for clothing images and videos within a single framework.

Users can upload an image to get a descriptive caption or provide a video to receive continuous frame-by-frame narration.

The system is useful for applications such as e-commerce product description automation, accessibility support for visually impaired users, fashion video understanding, and smart retail analytics.
🔁 Workflow
Input Image / Video → Preprocessing → ConvNeXt (Feature Extraction) → LSTM (Caption Generation) → Output Caption

Input is taken either as an image or video.

Images/frames are resized, normalized, and cleaned during preprocessing.

ConvNeXt-Large extracts deep visual features from apparel.

LSTM decoder generates captions word-by-word using learned language context.

Output is returned as a descriptive text caption.


---

##📊 Dataset Used
👉 **[Dataset Name:Fashion Product Images Dataset](Dataset URL:https://www.kaggle.com/datasets/paramaggarwal/fashion-product-images-dataset)**

🗂 Dataset Details
🟢 Fashion Product Images Dataset

Contains ~44,000+ real-world fashion product images along with detailed metadata.
It provides a large and balanced benchmark for training and evaluating apparel captioning, classification, and retrieval systems

##🧰 Dependencies Used
🐍 Python – Core programming language used for system development and training
👁️ OpenCV – Image loading, resizing, preprocessing, and video frame extraction
🔥 TensorFlow / Keras – Deep learning framework for building and training the captioning model
🧠 ConvNeXt-Large – Visual feature extraction from apparel images
🔁 LSTM – Sequential caption generation from image features
📊 NumPy – Numerical computation and feature vector operations
📁 Pandas – Dataset handling, CSV processing, and metadata cleaning
📝 Tokenizer – Text cleaning, word indexing, and sequence padding
📉 NLTK (BLEU) – Caption quality evaluation using BLEU-1 to BLEU-4 metrics
🎨 Matplotlib – Training loss and performance visualization
💻 Google Colab / Jupyter – Training and experimentation environment

##🔍 EDA & Preprocessing
🖼️ All images are converted to RGB format to maintain uniformity across the dataset
📏 Images are resized to 299×299 / 512×512 pixels to ensure compatibility with the CNN encoder
🧹 Corrupted, missing, and duplicate image files are removed during data cleaning
📊 Dataset distribution is analyzed to check category balance and reduce class imbalance
🏷️ Captions are cleaned by removing punctuation, converting to lowercase, and adding start/end tokens
🔢 Text is tokenized and padded to convert words into numerical sequences for LSTM training
🧠 ConvNeXt-Large extracts deep visual feature vectors instead of using raw images directly
🎥 Videos are split into frames and each frame is preprocessed individually for caption generation

##🧪 Model Training Info
🧠 ConvNeXt-Large generates deep visual feature embeddings from apparel images for semantic understanding
🔁 LSTM decoder learns sequential language patterns to generate captions word-by-word
📏 Images are resized and normalized before training to ensure stable and faster convergence
📝 Tokenized captions are padded to fixed-length sequences for efficient batch training
🎯 Cross-Entropy Loss measures the difference between predicted and actual words during caption generation
⚡ Adam optimizer updates model weights efficiently for faster and smoother learning
🔄 Teacher Forcing is used to guide the decoder with correct previous words during training for improved accuracy
📊 BLEU-1 to BLEU-4 metrics evaluate caption quality and sentence-level coherence
🎥 Video frames are processed individually and captions are generated continuously for smooth narration

##🧾 Model Testing / Evaluation
📏 Metrics Used:
📊 BLEU-1 – Measures single-word (unigram) caption accuracy
📊 BLEU-2 – Evaluates two-word phrase consistency
📊 BLEU-3 – Checks longer phrase coherence
📊 BLEU-4 – Measures full sentence fluency and contextual correctness
🆚 Compared With:
🔹 CNN–LSTM baseline (Show & Tell model)
🔹 Attention-based captioning models
🔹 Transformer-based captioning approaches
📈 Evaluation Process
🖼️ Tested on unseen apparel images and videos to measure generalization
🎥 Frame-by-frame evaluation ensures smooth and consistent video narration
🧠 Generated captions are compared with ground-truth captions using BLEU scores
⚖️ Performance demonstrates improved semantic understanding and balanced sentence-level accuracy



##🏆 Results
✅ Apparel Image Captioning
🎯 BLEU-1 Score: 0.946
🥇 BLEU-2 Score: 0.932
📊 BLEU-3 Score: 0.924
🏅 BLEU-4 Score: 0.917
✅ Video Captioning
🎥 Smooth frame-by-frame narration with reduced caption flickering
⚡ ~150 ms average processing time per frame for detection + caption generation
🧠 Maintains temporal consistency across consecutive frames
📈 Performance Highlights
✍️ Generates human-like, descriptive apparel captions (color, texture, pattern, design)
📦 Better generalization using larger and cleaner dataset
🚀 Suitable for real-time e-commerce and assistive applications
🆚 Outperforms traditional CNN–LSTM and attention-based captioning baselines in overall caption fluency and multi-word consistency

##⚠️ Limitations & Future Work
💻 Requires high GPU resources for training and real-time video caption generation
📉 Caption quality may reduce for very complex scenes with multiple overlapping apparel items
🎥 Frame-by-frame processing can increase latency for long or high-resolution videos
🗂 Dataset size is moderate; larger datasets could further improve generalization
🌐 Future Enhancements Include:
⚡ Real-time captioning optimization for faster inference
📦 Training on larger and more diverse fashion datasets
🧠 Integration of attention/transformer-based captioning models for better context understanding
🖥 Development of a web/mobile interface for user-friendly deployment
🌍 Multilingual caption generation for broader accessibility
♿ Text-to-speech integration for visually impaired users

##🌍 Deployment Info
🖥 Implemented using a Python-based backend for model training and inference
🧠 ConvNeXt-Large + LSTM models deployed for real-time apparel caption generation
⚡ GPU acceleration (CUDA-enabled systems) used for faster feature extraction and caption prediction
🎥 OpenCV handles real-time image and video frame processing
🌐 Can be deployed using Flask or FastAPI for web-based captioning services
📦 Supports batch image/video uploads for scalable e-commerce or retail applications
✨ Project By:
👨‍💻 Narendra Kanumuri
🎓 Smart Apparel Narrator – Deep Learning-Based Apparel Image & Video Captioning System
