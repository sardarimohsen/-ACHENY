# -ACHENY
Official repository for ACHENY: A standardized image dataset of Chenopodiaceae plants for deep learning applications. Features high-resolution imagery, curated labels, and benchmarks for botanical classification.

---

# ACHENY: A Standard Chenopodiaceae Image Dataset

[![Paper](https://img.shields.io/badge/Paper-ResearchGate-blue)](https://www.researchgate.net/publication/355225478_ACHENY_A_Standard_Chenopodiaceae_Image_dataset_for_Deep_Learning_Models)
[![Data](https://img.shields.io/badge/Mendeley-Data-orange)](https://data.mendeley.com/datasets/fpfty8nn7j/1)
[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)

**ACHENY** (Autumn Chenopod of Yazd) is a standardized image dataset of Chenopodiaceae plants, specifically curated to advance deep learning research in botanical identification and biodiversity monitoring. 

## 📌 Overview
Identifying species within the Chenopodiaceae family is historically challenging due to high morphological similarities. This dataset provides **27,030 high-resolution images** across **30 species**, captured in real-world desert and semi-desert conditions in the Yazd province of Iran.

### Key Features:
* **Diverse Conditions:** Images were captured under varying sunlight (sunny, cloudy), wind conditions, viewpoints, and camera-to-target distances.
* **Standardized Format:** All images are provided in RGB color and resized to $224 \times 224$ pixels (with $64 \times 64$ versions also available) for immediate use in CNN and Vision Transformer pipelines.
* **Expert Labeling:** Data was collected from multiple bushes per species to ensure high intra-species variety and inter-species distinction.

---

## 📊 Dataset Statistics
The dataset is imbalanced to reflect real-world distributions, containing between **300 and 1,461 images per class**.

| Feature | Value |
| :--- | :--- |
| **Total Images** | 27,030 |
| **Total Species** | 30 |
| **Training Split** | 72% (19,460 images) |
| **Validation Split** | 18% (4,867 images) |
| **Testing Split** | 10% (2,703 images) |

> **Note:** Testing specimens were selected from plant bushes distinct from the training set to ensure the model generalizes to new individuals of the same species.

---

## 🚀 Getting Started

### 1. Download the Data
The full dataset is hosted on **Mendeley Data**. You can download it directly here:
[**Download ACHENY Dataset**](https://data.mendeley.com/datasets/fpfty8nn7j/1)

### 2. Implementation
The images are organized in folders by species name. You can load the dataset in Python using standard libraries:
```python
from torchvision import datasets, transforms

transform = transforms.Compose([
    transforms.Resize((224, 224)),
    transforms.ToTensor(),
])

dataset = datasets.ImageFolder(root='path/to/ACHENY', transform=transform)
```

---

## 📖 Citation
If you use the ACHENY dataset or the related models in your research, please cite our work:

**Paper:** > Heidary-Sharifabad, A., Sardari Zarchi, M., Emadi, S., & Zarei, G. (2021). *ACHENY: A Standard Chenopodiaceae Image dataset for Deep Learning Models*. 

**Dataset:**
```bibtex
@misc{Heidary_Sharifabad_2021, 
  title={ACHENY : A Standard Chenopodiaceae Image dataset for Deep Learning Models}, 
  url={https://data.mendeley.com/datasets/fpfty8nn7j/1}, 
  DOI={10.17632/fpfty8nn7j.1}, 
  publisher={Mendeley}, 
  author={Heidary-Sharifabad, Ahmad and Sardari Zarchi, Mohsen and Emadi, Sima and Zarei, Gholamreza}, 
  year={2021}, 
  month={Aug}
}
```

---

## 👥 Authors
* **Ahmad Heidary-Sharifabad**
* **Mohsen Sardari Zarchi**
* **Sima Emadi**
* **Gholamreza Zarei**

---

### 📄 License
The dataset is licensed under a [Creative Commons Attribution 4.0 International License (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/).
