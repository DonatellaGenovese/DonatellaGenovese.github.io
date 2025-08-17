---
title: "Tutorial: Implementing Explainability Techniques in Captum for Plant Disease Classification"
last_modified_at: 2025-08-17 12:00:00 +0000
categories: Blog
tags:
  - Explainable AI
  - Captum
  - Deep Learning
  - Plant Disease
  - ResNet18
readability: standard
---

This post is a tutorial on implementing explainability techniques using the Captum library to interpret deep learning models applied to plant disease classification.

In this notebook, we leverage a pretrained ResNet18 model to tackle a challenging multiclass classification problem involving 38 classes, each representing a different plant disease (e.g., NamePlantDisease). The goal is to not only achieve accurate classification but also to understand *why* the model makes certain predictions.

### Dataset and Model

The dataset consists of images of plant leaves affected by various diseases. Using transfer learning, the pretrained ResNet18 network is fine-tuned on this dataset to classify the disease type.

### Explainability Techniques Used

To gain insights into the model's decision process, we implement three popular interpretability methods available in Captum:

- **Integrated Gradients**: Computes the importance of each input pixel by integrating gradients along a path from a baseline to the input, highlighting influential features.

- **Grad-CAM (Gradient-weighted Class Activation Mapping)**: Produces heatmaps that show which spatial regions in the image the model focuses on to make its prediction.

- **Occlusion Sensitivity**: Measures the effect of systematically occluding different parts of the input image on the prediction confidence, revealing critical regions.

### Why Explainability Matters

Deep learning models like ResNet18 are powerful but often viewed as "black boxes". Explainability techniques help build trust and validate model behavior, which is especially important in agriculture where decisions affect food security.

### Try It Yourself

For a hands-on experience, check out the full Colab notebook here:  
[Plant Disease Classification with Explainability in Captum](https://colab.research.google.com/drive/1ZfzgMX7Gdl2bQnOOiJMTSZw3_f8kYJno?usp=sharing)

This notebook walks you through the entire process, from loading the data and training the model to applying the explainability methods and visualizing results.

---

Feel free to leave comments or questions if you'd like me to cover more explainability techniques or dive deeper into specific parts of the tutorial!
