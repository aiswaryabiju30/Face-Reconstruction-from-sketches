# Face Reconstruction from Sketches

## Overview
This project converts hand-drawn face sketches into realistic human face images using deep learning.

A Pix2Pix (Conditional GAN) model is trained on paired sketch–photo images.  
GFPGAN is used as a post-processing step to enhance facial details and image quality.

## Dataset
- **Dataset:** CUFS (Chinese University of Hong Kong Face Sketch Dataset)
- **Total Images:** 188 paired images
  - Train: 88
  - Test: 100
- Each sketch image has a corresponding real face image.

## Model Used
- **Model:** Pix2Pix (Conditional GAN)
- **Generator:** U-Net architecture
- **Discriminator:** PatchGAN
- **Loss Function:** Adversarial Loss + L1 Loss
- **Enhancement:** GFPGAN for improving sharpness and realism

## Training Details
- Epochs: 11
- Batch Size: 16
- Optimizer: Adam
- Learning Rate: 0.0002

## Evaluation Metrics
- SSIM: 0.86
- PSNR: 30.93
- MSE: 52.92
- L2 Norm: 57893.46

## Results
- The model successfully reconstructs realistic face images from sketches.
- GFPGAN improves facial clarity and fine details.
- Results improve with better preprocessing and more training data.

## Project Structure
- `training/` : Model training, testing, evaluation notebooks
- `backend/` : Backend logic for model inference
- `frontend/` : Web interface for user interaction

## Clone the Repository
```bash
git clone https://github.com/aiswaryabiju30/Face-Reconstruction-from-sketches.git

