# Satellite Maps Conversion GAN (Pix2Pix)

This project implements a **Satellite Maps Conversion GAN** using a Pix2Pix approach. This GAN-based architecture is designed to convert satellite images ("input") into detailed map routes ("output"), following the conditional adversarial network model from Isola et al.'s Pix2Pix paper.

## Table of Contents
- [Project Overview](#project-overview)
- [Features](#features)
- [Model Architecture](#model-architecture)

## Project Overview
This project trains a generative model that converts aerial satellite imagery into map-style representations. The model architecture is based on a U-Net generator with a PatchGAN discriminator, designed to evaluate the realism of generated images. This approach is highly applicable to geographic information systems (GIS), urban planning, and automated map generation.

## Features
- **Conditional GAN**: Employs conditional adversarial learning to ensure output maps align closely with input satellite images.
- **U-Net Generator**: Uses a modified U-Net with optional dropout and batch normalization layers.
- **PatchGAN Discriminator**: Implements a PatchGAN discriminator to evaluate image quality at a patch level, improving detail and local coherence.
- **Pre-trained Checkpoint**: Includes a pre-trained Pix2Pix checkpoint to expedite model training.

## Model Architecture
The Pix2Pix model includes:
1. **U-Net Generator**: The generator network, based on a U-Net architecture, is designed to produce high-resolution, detailed outputs.
2. **PatchGAN Discriminator**: The PatchGAN discriminator outputs a matrix that evaluates the realism of generated images at the patch level, refining the model's output quality.

### Key Components
- **Loss Functions**: Combines adversarial loss with L1 reconstruction loss, balancing realism with fidelity to the input image.
- **Learning Objectives**: Shift the generator’s focus from purely reconstructing input images to producing realistic map-like outputs.

