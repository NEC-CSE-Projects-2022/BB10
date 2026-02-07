# 👕 Fashion Product Images Dataset — Preview & Download

<img width="1100" height="550" alt="dataset-preview" src="https://ibb.co/994Z5ZdR" />

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

