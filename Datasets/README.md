# 👕 Fashion Product Images Dataset — Preview & Download

<img width="1100" height="550" alt="dataset-preview" src="https://storage.googleapis.com/kagglesdsdata/datasets/139630/329006/fashion-dataset/images/10011.jpg?X-Goog-Algorithm=GOOG4-RSA-SHA256&X-Goog-Credential=databundle-worker-v2%40kaggle-161607.iam.gserviceaccount.com%2F20260206%2Fauto%2Fstorage%2Fgoog4_request&X-Goog-Date=20260206T052024Z&X-Goog-Expires=345600&X-Goog-SignedHeaders=host&X-Goog-Signature=111a5990b1047a188cb500b19df0f0316192a1f42e08a10244d27a2c36eea28a91ac9df35c374eff57a92c7be93853182dcc0148cbe48c850ec34ddbb7574bb64620388b299bdbb40c155d210bc6623e72a5d71dcf0f311746c7a060f83526672d6599bf531e9c25bfa76a03ae79c250cad6ed6323e8b2ab01cff7d339e767f4407c19a940a4286bb946d0a9fdf23f978b7525f897b0385ae002ba415efa9ac4f8f82fa46efdd8e8d1b27491c4c2800c591a7801345d3a3914dbdc7aed37f6674b05169993d53e2615fdd5b4ed0e0e9347c458e9cc5237cc4b1d1ab43de7111f51669dbb80e736a86011b7f4e2f26f189fea4d80a10446b7121019440ec5692b" />

> Professional dataset README for the apparel image dataset used in this project.  
> This file documents where to download the dataset, its structure, usage examples, acknowledgement, and citation information.

---

## 🔎 Overview

- Name: Fashion Product Images Dataset
- Size: ~44,000+ images
- Categories: Apparel, Footwear, Accessories, Personal Care
- Metadata: Product name, gender, category, color, season, usage
- Source: Kaggle (see Download section)
- Used for: Apparel captioning, classification, retrieval, recommendation systems

---

## 🔗 Download

### 📥 Kaggle (Official)
https://www.kaggle.com/datasets/paramaggarwal/fashion-product-images-dataset

### Kaggle CLI
```bash
kaggle datasets download -d paramaggarwal/fashion-product-images-dataset
```

### Extract
```bash
unzip fashion-product-images-dataset.zip
```

---

## 📦 Dataset Contents & Structure

Recommended folder structure:

```
Datasets/
│
├── images/
│   ├── 10000.jpg
│   ├── 10001.jpg
│   ├── 10002.jpg
│   └── ...
│
├── styles.csv
│
└── README.md
```

### Files Description

### images/
- Contains all product images
- RGB JPG format
- Mixed resolutions

### styles.csv
Contains metadata for each product:

- id
- gender
- masterCategory
- subCategory
- articleType
- baseColour
- season
- year
- usage
- productDisplayName

---

## ℹ️ About the Data

### Context
This dataset contains real-world fashion product images commonly used in:
- Image classification
- Visual search
- Product recommendation
- Apparel captioning

### Content
- High-quality RGB images
- Professional e-commerce photography
- Rich product metadata

### Inspiration
Designed for fashion AI and computer vision research.

### Acknowledgements
- Dataset provided by Kaggle contributors
- Original source: Fashion Product Images Dataset (Param Aggarwal)

---

## ⚙️ Usage Examples

### 🐍 PyTorch (ImageFolder)

```python
from torchvision import transforms
from torchvision.datasets import ImageFolder
from torch.utils.data import DataLoader

transform = transforms.Compose([
    transforms.Resize((224, 224)),
    transforms.ToTensor()
])

dataset = ImageFolder('Datasets/images', transform=transform)
loader = DataLoader(dataset, batch_size=32, shuffle=True)
```

---

### 🐍 TensorFlow / Keras

```python
import tensorflow as tf

dataset = tf.keras.preprocessing.image_dataset_from_directory(
    "Datasets/images",
    image_size=(224,224),
    batch_size=32
)
```

---

### 🐍 Load Metadata with Pandas

```python
import pandas as pd

df = pd.read_csv("Datasets/styles.csv")
print(df.head())
```

---

## 🎯 Recommended Preprocessing

- Convert images → RGB
- Resize to 224×224 / 299×299 / 512×512
- Normalize pixel values
- Remove corrupted images
- Clean metadata
- Generate captions from productDisplayName

---

## 📌 Applications

- Apparel Image Captioning
- Product Classification
- Fashion Retrieval Systems
- Recommendation Engines
- E-commerce Automation

---

## 📜 Citation

If you use this dataset, please cite:

```
Fashion Product Images Dataset – Kaggle
https://www.kaggle.com/datasets/paramaggarwal/fashion-product-images-dataset
```

---

## ✅ Notes

- Intended for academic/research purposes
- Follow Kaggle license terms
- Ensure ethical use of data

