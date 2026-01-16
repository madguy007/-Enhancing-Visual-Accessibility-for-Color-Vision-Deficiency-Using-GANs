# GAN Model Description: Image A → Image B Translation

## Objective
The goal of this model is to enhance visual accessibility for individuals with Color Vision Deficiency (CVD) by learning an image-to-image translation that improves color contrast and perceptual clarity.

The model maps:
- **Image A**: Original or simulated color vision deficient images
- **Image B**: Recolored images with enhanced contrast and brightness

---

## Model Overview
A Generative Adversarial Network (GAN) is used to learn the transformation from Image A to Image B. The GAN consists of two main components:

- **Generator**: Learns to translate Image A into a visually enhanced Image B
- **Discriminator**: Distinguishes between real recolored images and generated outputs

Through adversarial training, the generator progressively improves its ability to produce perceptually meaningful recolored images.

---

## GAN Architecture
The project follows an image-to-image translation paradigm similar to **pix2pix / CycleGAN-style architectures**, where spatial structure is preserved while color information is modified.

Key characteristics:
- Convolutional encoder–decoder generator
- Patch-based discriminator for local realism
- Adversarial loss combined with reconstruction loss

---

## Training Process
1. Input images (A) and target images (B) are resized and normalized
2. The generator produces a recolored version of Image A
3. The discriminator evaluates real vs generated Image B
4. Loss functions guide optimization of both networks
5. Training continues until stable and visually improved results are obtained

---

## Inference / Output Generation
After training:
- The generator alone is used for inference
- New input images are passed through the trained generator
- Output images exhibit improved contrast and color separability for CVD users

Inference is implemented in `generate_output.py`.

---

## Evaluation
Evaluation is primarily qualitative and includes:
- Visual comparison of original vs recolored images
- Pixel-wise difference analysis between algorithmic and GAN-based outputs
- Inspection of contrast and brightness improvements

Final results are documented in:
- `report/Project_Report.pdf`
- `report/Flower_Results.pdf`

---

## Limitations
- Model performance depends on dataset diversity
- Color naturalness may vary across images
- Current implementation focuses on still images only

---

## Future Improvements
- Support for additional CVD types
- Extension to video recoloring
- Improved perceptual loss functions
