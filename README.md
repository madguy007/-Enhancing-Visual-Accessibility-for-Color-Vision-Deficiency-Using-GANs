# Enhancing Visual Accessibility for Color Vision Deficiency Using GANs

## Overview
This project aims to improve visual accessibility for individuals with **Color Vision Deficiency (CVD)** by leveraging **Generative Adversarial Networks (GANs)** for image recoloring. The model learns an **image-to-image translation (A → B)** that enhances contrast, brightness, and color separability, enabling better perception of visually confusing colors such as red–green combinations.

The work combines classical recoloring techniques with GAN-based learning to generate perceptually improved images and scalable datasets for accessibility-focused applications.

---

## Problem Statement
Individuals with Color Vision Deficiency often struggle to distinguish between certain color pairs due to limitations in color perception. Traditional recoloring algorithms are limited in scalability and generalization. This project explores whether GANs can learn effective recoloring transformations that improve visual clarity while preserving image structure.

---

## Approach
- Simulated color vision deficiency images
- Generated recolored target images using image processing techniques
- Trained a GAN model to learn the **Image A → Image B** mapping
- Used the trained generator to produce enhanced images for unseen inputs

---

## Dataset
The dataset consists of paired images for GAN-based image-to-image translation:

- **Image A**: Original or simulated CVD images  
- **Image B**: Recolored images with enhanced contrast and brightness  

Due to size constraints, the **full training and testing datasets (1000+ images)** are hosted on Google Drive.

### Dataset Access (Google Drive)
- **Training Dataset**:  
  👉 https://drive.google.com/drive/folders/16Xgsomlo6ouXVVFrXYyRqm_RhRWgfOiB?usp=sharing
- **Testing Dataset**:  
  👉 https://drive.google.com/drive/folders/1Gj_lsywt4VjM5JFlne10-7utOYqgzgjv?usp=sharing

A small subset of images is included in `data/sample/` to demonstrate the dataset structure.

For details, see `data/README.md`.

---

## Repository Structure

```
data/          # Sample data and dataset instructions
src/           # GAN training and inference code
models/        # GAN model directory
outputs/       # Generated GAN outputs (samples)
report/        # Project report and result PDFs
docs/          # Model and methodology documentation
```


---

## How to Run

### 1. Install Dependencies
```bash
pip install -r requirements.txt

python src/train_gan.py

python src/generate_output.py

```
## Results
The trained GAN model generates recolored images that enhance contrast and
color separability for individuals with Color Vision Deficiency.

- Output images are saved in the `outputs/gan_results/` directory
- Visual comparisons of original vs recolored images are provided
- Detailed qualitative analysis is available in the project report PDFs
