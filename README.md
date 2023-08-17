# CLIP Object Detection

CLIP is a versatile vision-language model trained to associate images with text descriptions using contrastive learning. This notebook demonstrates CLIP's capabilities for zero-shot object detection by using a pretrained model to recognize objects without training on categorized image datasets. The model's understanding of visual concepts and language enables real-world computer vision applications.

## Requirements
To run the scripts in this repository, you will need to have the following dependencies installed:

- Python 3
- PyTorch
- Matplotlib
- [Clip](https://github.com/openai/CLIP.git)
- NumPy

## CLIP
CLIP is a neural network trained on a 400 million image-text pairs dataset to learn visual concepts and their textual representations through contrastive learning. By predicting the correct text for a given image and vice versa, CLIP builds connections between visual and language concepts without the need for labeling or categorization. This self-supervised approach produces a general-purpose model that excels at image-language tasks like classification and object detection.


<h3 align="center">CLIP</h3>
<p align="center">
  <img src="images/CLIP.png" width="600">
</p>

## Methodology

Object candidate regions are first extracted from the input images using a Faster R-CNN model's pretrained Region Proposal Network. This rapidly identifies potential regions of interest. CLIP then encodes these proposed regions and textual object queries into high-dimensional embeddings suitable for comparison. Multiple phrasings of each query are averaged to obtain a robust representation. Finally, cosine similarity between regional embeddings and averaged query embeddings identifies the most semantically aligned regions for each specified object class.

## Results
Below is the original image:

<h3 align="center">CLIP</h3>
<p align="center">
  <img src="images/clip_result.png" width="600">
</p>

Below are the boxes that faster rcnn extracted from the original image:
<h3 align="center">CLIP</h3>
<p align="center">
  <img src="images/clip_result.png" width="600">
</p>
