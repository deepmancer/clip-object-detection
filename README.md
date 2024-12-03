# 🚀 CLIP Zero-Shot Object Detection 🖼️

<p align="center">
  <img src="https://img.shields.io/badge/PyTorch-%23EE4C2C.svg?style=for-the-badge&logo=PyTorch&logoColor=white" alt="PyTorch">
  <img src="https://img.shields.io/badge/OpenAI-412991.svg?style=for-the-badge&logo=OpenAI&logoColor=white" alt="OpenAI">
  <img src="https://img.shields.io/badge/Python-3670A0?style=for-the-badge&logo=Python&logoColor=ffdd54" alt="Python">
  <img src="https://img.shields.io/badge/Jupyter-F37626.svg?style=for-the-badge&logo=Jupyter&logoColor=white" alt="Jupyter Notebook">
</p>

> **Detect objects in images without training!**

Welcome to the **CLIP Zero-Shot Object Detection** project! This repository demonstrates how to perform zero-shot object detection by integrating OpenAI's **CLIP** (Contrastive Language-Image Pretraining) model with a **Faster R-CNN** for region proposal generation.

---

## 🎯 Quick Start

Set up and run the pipeline in three simple steps:

1. **Clone the Repository**:

   ```bash
   git clone https://github.com/deepmancer/clip-object-detection.git
   cd clip-object-detection
   ```

2. **Install Dependencies**:
  
   ```bash
   pip install -r requirements.txt
   ```

3. **Run the Notebook**:

   ```bash
   jupyter notebook clip_object_detection.ipynb
   ```

---

## 🤔 What is CLIP?

**CLIP** (Contrastive Language–Image Pretraining) is trained on 400 million image-text pairs. It embeds images and text into a shared space where the cosine similarity between embeddings reflects their semantic relationship.

<div align="center">
    <figure>
        <img 
            src="https://raw.githubusercontent.com/deepmancer/clip-object-detection/main/assets/CLIP.png" 
            width="600" 
            alt="CLIP Model Architecture"
        />
        <figcaption>
            CLIP Model Architecture - <a href="https://arxiv.org/abs/2103.00020">Paper</a>
        </figcaption>
    </figure>
</div>

---

## 🔍 Methodology

Our approach combines CLIP and Faster R-CNN for zero-shot object detection:

1. **📦 Region Proposal**: Use Faster R-CNN to identify potential object locations.
2. **🎯 CLIP Embeddings**: Encode image regions and text descriptions into a shared embedding space.
3. **🔍 Similarity Matching**: Compute cosine similarity between text and image embeddings to identify matches.
4. **✨ Results**: Highlight detected objects with their confidence scores.

---

## 📊 Example Results

### Input Image

<p align="center">
  <img src="https://raw.githubusercontent.com/deepmancer/clip-object-detection/main/assets/original_image.png" width="450" alt="Original Image">
</p>

### Region Proposals

Regions proposed by Faster R-CNN's RPN:

<p align="center">
  <img src="https://raw.githubusercontent.com/deepmancer/clip-object-detection/main/assets/regions.png" width="450" alt="Candidate Regions">
</p>

### Detected Objects

Objects detected by CLIP based on textual queries:

<p align="center">
  <img src="https://raw.githubusercontent.com/deepmancer/clip-object-detection/main/assets/clip_result.png" width="450" alt="Detected Objects">
</p>

---

## 📦 Requirements

Ensure the following are installed:

- **PyTorch**: Deep learning framework.
- **Torchvision**: Pre-trained Faster R-CNN.
- **OpenAI CLIP**: [GitHub Repository](https://github.com/openai/CLIP.git).
- Additional dependencies are listed in [requirements.txt](requirements.txt).

---

## 📝 License

This project is licensed under the [MIT License](LICENSE). Feel free to use, modify, and distribute the code.

---

## ⭐ Support the Project

If this project inspires or assists your work, please consider giving it a ⭐ on GitHub! Your support motivates us to continue improving and expanding this repository.
