# 🔍 CLIP Object Detection

Unleash the power of CLIP, a groundbreaking vision-language model by OpenAI, to perform zero-shot object detection! CLIP can match images with text descriptions by understanding both visual and textual concepts, making it a versatile tool for a wide range of computer vision applications without needing traditional training datasets.

## 📋 Requirements

To dive into the magic of CLIP-based object detection, make sure you have the following installed:

- **Python 3**: The backbone of your environment.
- **PyTorch**: Essential for deep learning computations.
- **Matplotlib**: For visualizing your results.
- **CLIP**: The model itself ([CLIP GitHub Repository](https://github.com/openai/CLIP.git)).
- **NumPy**: For numerical operations.

## 🚀 What is CLIP?

CLIP (Contrastive Language–Image Pre-training) is a neural network trained on a massive dataset of 400 million image-text pairs. By learning to predict the correct text for images and vice versa, CLIP effectively bridges the gap between visual and textual understanding. This self-supervised model excels in various image-language tasks, including classification and object detection, without the need for labeled training data.

<h3 align="center">CLIP in Action</h3>
<p align="center">
  <img src="images/CLIP.png" width="600" alt="CLIP Model">
</p>

## 🔍 Methodology

1. **Region Proposal**: Start with Faster R-CNN’s Region Proposal Network (RPN) to identify potential areas of interest in the image.
2. **Embedding**: Use CLIP to encode both the proposed regions and textual queries into high-dimensional embeddings.
3. **Comparison**: Average multiple phrasings of each query to get a robust representation. Then, compute cosine similarity between the regional embeddings and the averaged query embeddings.
4. **Detection**: Identify the regions that most closely align with the textual descriptions for accurate object detection.

## 🖼️ Results

**Original Image:**

<h3 align="center">Original Image</h3>
<p align="center">
  <img src="images/original_image.png" width="450" alt="Original Image">
</p>

**Candidate Regions:**

These are the regions identified by Faster R-CNN from the original image.

<h3 align="center">Candidate Regions</h3>
<p align="center">
  <img src="images/regions.png" width="450" alt="Candidate Regions">
</p>

**Detected Objects:**

Here’s what CLIP detected in the image.

<h3 align="center">Objects Detected By CLIP</h3>
<p align="center">
  <img src="images/clip_result.png" width="450" alt="Detected Objects">
</p>

Explore the potential of CLIP for zero-shot object detection and see how it performs without needing extensive training data. Happy detecting! 🕵️‍♂️
