# 👕 Fashion Product Images Dataset — Preview & Download

<img width="1100" height="550" alt="dataset-preview" src="https://storage.googleapis.com/kagglesdsdata/datasets/139630/329006/fashion-dataset/images/10008.jpg?X-Goog-Algorithm=GOOG4-RSA-SHA256&X-Goog-Credential=databundle-worker-v2%40kaggle-161607.iam.gserviceaccount.com%2F20260206%2Fauto%2Fstorage%2Fgoog4_request&X-Goog-Date=20260206T052024Z&X-Goog-Expires=345600&X-Goog-SignedHeaders=host&X-Goog-Signature=5bb69f6383537566eece4c5258e1eb3259db192b8f5484d74c8cf9de9571c054dc98c0e83bb709144b2da13674d821167b93d5f51750114d03843369524fb79217d3b5b93e8c3181670a3f21a359b1c9500c0ed72f1cc4fd656a0cc202b9140a82f6888ba4830b914668bc28385270139a529feda3fe62692e907994f6929ab76ffd3c0d92d342735cd9288aabd60a0c4c80b9626ab60fd00182b638837cd813b5b59a572762afe125760a5eec7e8ff9fec717ce3bf193dbc591ac6ee20fdd7fb769847e7e340b2b099d79fcf85d822b1d0b852fc7975b217e53efb0b776db1209e734fc8fa7e4ddf07b522655ac44f7c6831b95508eac9034d5346d06e0ed10"/>

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

