# 👕 Fashion Product Images Dataset — Preview & Download

<img width="1100" height="550" alt="dataset-preview" src="https://storage.googleapis.com/kagglesdsdata/datasets/139630/329006/fashion-dataset/images/10009.jpg?X-Goog-Algorithm=GOOG4-RSA-SHA256&X-Goog-Credential=databundle-worker-v2%40kaggle-161607.iam.gserviceaccount.com%2F20260206%2Fauto%2Fstorage%2Fgoog4_request&X-Goog-Date=20260206T052024Z&X-Goog-Expires=345600&X-Goog-SignedHeaders=host&X-Goog-Signature=4db7406c3075cfd429f7a4825a8539b3bba07951d45041c893378818f51710c3838d10890ad78bfaa621ddab1d64c8fe0278451bac5b35e88d092bfd0c3ade4300fc9fbe0a0eae1c9faa45641ebdc75510c1c9fb5d2d8a6f0dc26251ce0beb5cf56607b9e6a9472cd70ef0e975a4272307bdfdff44eab334e97e8447782c0dfe0bb5fe28b7be3f311df73f96ed7ca69a6430db710caa69d269345d680f1b1f2de4879880cd0287c158c9003d3585c7430bac56d8e6d16454c6d0ce11b6b3add72c6bb7ef02eb01e54f8db3a79255b68538dbe2f5443a7c035d7fec5792e8edea396048111fe2cdbcc5c0bb0195c23ae777f035a14911327c53f46c6fd70c06f3" />

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

