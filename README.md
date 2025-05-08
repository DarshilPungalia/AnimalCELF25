# Animal Re-identification using Vision Transformers

This repository contains the implementation for an animal re-identification system developed as part of the **AnimalCLEF 2025** challenge, a subtask of **LifeCLEF** organized under **CVPR-FGVC**. The goal is to determine whether a query image corresponds to a known individual from a gallery or represents a new (unknown) individual across diverse species such as loggerhead sea turtles, Eurasian lynxes, and fire salamanders.

## 🧠 Project Overview

- **Task**: Open-set individual re-identification of animals from photographic data.
- **Challenge**: AnimalCLEF 2025 @ CVPR-FGVC & LifeCLEF.
- **Approach**:
  - Utilized Vision Transformer (ViT), EfficientNet, ConvNeXt models from for embedding extraction.
  - Employed cosine similarity to match query images against known gallery embeddings.
  - Applied preprocessing techniques like normalization and class-balanced sampling.
  - Evaluated system performance using clustering metrics and dimensionality reduction (t-SNE).

  | Model             | Backbone           | Input Format     | Performance |
|------------------|--------------------|------------------|----------------|
| ViT (torchvision)     | ViT-B/16            | `PIL.Image`      | Poor        | 
| EfficientNetV2    | EfficientNetV2-L    | `np.ndarray`     | Poor         | 
| ConvNeXt          | ConvNeXt-Tiny       | `np.ndarray`     | Ok         |

## Features

- Supports multi-species embedding extraction and matching.
- Handles open-set recognition (distinguishing known vs. unknown individuals).
- Visualization support for embedding distribution and cluster quality.

## Results

- Effective separation between known and novel individuals across species.
- Embeddings demonstrated meaningful clustering when visualized using t-SNE.

## References

- [CLEF 2025 Labs](https://www.imageclef.org/2025/animal)
- [Dataset](https://www.kaggle.com/competitions/animal-clef-2025/data)

---

> This project was developed for academic research and submission to the **AnimalCLEF 2025** competition, contributing to automated biodiversity monitoring using computer vision and deep learning.

