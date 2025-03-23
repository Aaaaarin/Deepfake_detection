# Deepfake_detection

A PyTorch-based deep learning pipeline to detect deepfake images. This project leverages custom data pipelines, advanced data augmentation, and a custom CNN architecture inspired by residual networks to effectively distinguish between real and manipulated images.

---

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Results](#results)
- [Future Work](#future-work)
- [License](#license)
- [Contact](#contact)

---

## Overview

Deepfake detection is critical for verifying the authenticity of media content in today's digital age. This project implements a robust solution using PyTorch, featuring:
- A custom dataset class to load and preprocess real and fake images.
- Aggressive data augmentation techniques using `torchvision.transforms.v2` to enhance model generalization.
- A custom CNN architecture, **DeepfakeNet**, inspired by ResNet with bottleneck blocks to extract deep features efficiently.
- A training pipeline utilizing GPU acceleration for faster model convergence.

---

## Features

- **Custom Dataset Pipeline:** 
  - Loads images from separate directories for real and deepfake samples.
  - Applies both basic resizing and advanced augmentations (e.g., random flips, affine transforms, color jitter).

- **Efficient Model Architecture:**
  - Implements bottleneck residual blocks for a deep yet computationally efficient CNN.
  - Uses adaptive average pooling and residual connections for enhanced performance.

- **Training and Evaluation:**
  - Uses an 80/20 train-validation split.
  - Employs the Adam optimizer and Mean Squared Error (MSE) loss.
  - Tracks training progress using `tqdm` for real-time feedback.
  
- **Device Optimization:**
  - Automatically utilizes GPU if available.

---

## Installation

1. **Clone the Repository:**

   ```bash
   git clone https://github.com/Bhavnoor-Coders-1010/DeepFakeBCS.git deepfake
   cd deepfake
