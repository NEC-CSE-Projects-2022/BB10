
# Team Number – Project Title

## Team Info
- 22471A05A0 — Kanumuri Narendra ( [LinkedIn](https://www.linkedin.com/in/narendra-kanumuri-6b4649276/) )
_Work Done: xxxxxxxxxx_

- 22471A05B1 — Nallamekala Vignesh ( [LinkedIn](https://www.linkedin.com/in/nallamekala-vignesh-9b992a361/) )
_Work Done: xxxxxxxxxx_

- 22471A05B8 —  Peddipaka Udaykiran ( [LinkedIn](https://www.linkedin.com/in/uday-kiran-65bb88282/) )
_Work Done: xxxxxxxxxx_


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


---

## Our Improvement Over Existing Paper
Although the existing study Image and Video Captioning for Apparels Using Deep Learning demonstrated strong performance using a ConvNeXtLarge–LSTM framework with YOLO-based object detection and achieved a high BLEU-1 score of 0.983, it primarily emphasized object-level detection and independent frame-wise caption generation 

Image_and_Video_Captioning_for_…

.
The proposed Smart Apparel Narrator extends this foundation and introduces several methodological and practical enhancements for improved semantic understanding and narration quality.

First, the proposed work increases dataset robustness by utilizing over 1,000 curated and annotated apparel images and video clips, compared to 863 base images in the existing system. This improves diversity and generalization across multiple fashion categories .

Second, while the existing model captions frames independently after YOLO detection, our approach introduces frame-level feature alignment, ensuring temporal continuity and reducing caption flickering in videos. This enables smoother and more consistent narration for dynamic apparel movements.

Third, the existing framework mainly focuses on object presence and detection accuracy, whereas the proposed system emphasizes fine-grained fashion semantics, including texture, fabric, pattern, color, and design attributes. This leads to more descriptive and human-like captions rather than simple object labels.

Fourth, we improve linguistic quality and contextual coherence through enhanced caption preprocessing, structured tokenization, and optimized sequence learning. Instead of optimizing only unigram precision, our model achieves balanced BLEU-1 to BLEU-4 scores (0.946, 0.932, 0.924, 0.917), indicating stronger multi-word consistency and sentence-level fluency 

2025387542

.

Finally, the proposed system is designed with practical deployment readiness, supporting automated e-commerce tagging, assistive narration for visually impaired users, and scalable video indexing, thereby broadening real-world applicability beyond experimental evaluation.

Overall, the Smart Apparel Narrator advances the prior work by transitioning from detection-focused captioning to context-aware, temporally consistent, and semantically rich fashion narration, while maintaining competitive quantitative performance.

---

## About the Project
Give a simple explanation of:
- What your project does
  Your project automatically generates text descriptions (captions) for apparel/clothing images and videos using Deep Learning.
- Why it is useful
  This project solves real-world fashion industry problems:
  1.E-commerce automation
  2.Accessibility
  3.Video understanding
  4.Smart retail systems
- General project workflow (input → processing → model → output)
  start → blue → cotton → shirt → end


---

## Dataset Used
👉 **[Dataset Name:Fashion Product Images Dataset](Dataset URL:https://www.kaggle.com/datasets/paramaggarwal/fashion-product-images-dataset)**

**Dataset Details:**
Fashion Product Images Dataset — Details

The Fashion Product Images Dataset on Kaggle is a large, real-world dataset of apparel product images and metadata, collected to support fashion-related machine learning tasks such as classification, visual search, and recommendation systems
Key Features:

Number of Items: ~44,000+ fashion products.

Images: High-resolution, professionally shot product images.

Image Files: Each product typically has one or more images.

Categories: Products span multiple fashion categories such as:

Apparel (tops, shirts, dresses)

Footwear

Accessories (bags, watches, belts)

Personal care items

Metadata Attributes:

Each product entry includes rich descriptive metadata, such as:

Product name / display name

Gender target (e.g., men, women)

Master category (e.g., Apparel, Footwear)

Sub category (e.g., T-shirts, Sneakers)

Article type (e.g., Jeans, Jackets)

Base color

Season / Year

Usage context (e.g., casual, formal)

Structure & Format:

Typically distributed as image folders and CSV metadata files (e.g., styles.csv) linking each styleID to its image and attributes.

Suitable for:

Computer vision tasks (CNN/LSTM models)

Image captioning training

Product classification or tagging

Visual recommendation systems

---

## Dependencies Used
Language:Python
DL Framework:TensorFlow/Keras or PyTorch
Vision:OpenCV, PIL
Models:ConvNeXt-Large, LSTM
Data:NumPy, Pandas
NLP:Tokenizer, Padding
Evaluation:BLEU (NLTK)
Dataset:Fashion Product Images (Kaggle)
---

## EDA & Preprocessing
EDA means checking and understanding the dataset before training the model.

What we did:

Count total images

Check clothing categories (shirts, jeans, dresses, etc.)

Remove non-apparel items

Remove missing or corrupted images

Check class balance

Verify captions/labels

Why?

👉 To make sure the dataset is clean, correct, and useful

Image Preprocessing
Steps:
1. Resize

Make all images same size (299×299 or 512×512)

2. Normalize

Convert pixel values to 0–1 range

3. Feature Extraction

Use ConvNeXt-Large CNN

Convert image → feature vector

Why?

👉 Helps the model learn faster and better

Caption/Text Preprocessing
Steps:
1. Clean text

Lowercase

Remove punctuation

Remove extra spaces

2. Add special tokens

Example:

startseq blue cotton shirt endseq

3. Tokenize

Convert words → numbers

4. Padding

Make all sentences same length

Why?

👉 Makes captions ready for LSTM training


Video Preprocessing (if video input):

Extract frames from video

Resize each frame

Generate captions for every frame

Raw Images/Video
      ↓
Clean data
      ↓
Resize + Normalize
      ↓
Extract features (CNN)
      ↓
Clean captions
      ↓
Tokenize + Pad
      ↓
Ready for model training


---

## Model Training Info


---

## Model Testing / Evaluation
xxxxxxxxxx

---

## Results
xxxxxxxxxx

---

## Limitations & Future Work
xxxxxxxxxx

---

## Deployment Info
xxxxxxxxxx

---
