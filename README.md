# Image to Image Translation with Conditional GANs (CGANs)
![](https://res.cloudinary.com/daily-now/image/upload/f_auto,q_auto/v1/posts/48508ea7affbe31fccffa234c022ed12?_a=AQAEufR)

This repository contains an implementation of Image to Image Translation using Conditional GANs (CGANs). 
The project is designed to translate images from one domain to another, such as turning edge maps into photos or converting aerial images into maps.

## Table of Contents
- [Introduction](#introduction)
- [Setup](#setup)
- [Usage](#usage)
- [Results](#results)

## Introduction

Conditional GANs (CGANs) are a type of Generative Adversarial Networks (GANs) where both the generator and discriminator receive additional information, such as class labels or data from other modalities. 
This project implements CGANs for tasks such as translating Cityscapes dataset images and edges2shoes dataset images.

## Setup

### Prerequisites

To run this project, you need to have the following libraries installed:
- NumPy
- Pandas
- SciPy
- Matplotlib
- scikit-image
- Keras
- TensorFlow
- ImageIO

You can install these libraries using pip:

```bash
pip install numpy pandas scipy matplotlib scikit-image keras tensorflow imageio
```

### Data

The datasets used in this project are:
- [Cityscapes](https://www.kaggle.com/datasets/vikramtiwari/pix2pix-dataset?select=cityscapes)
- [edges2shoes](https://www.kaggle.com/datasets/vikramtiwari/pix2pix-dataset?select=edges2shoes)

Ensure you have downloaded and extracted these datasets into the appropriate directory structure.

## Usage

To train the CGAN model on the Cityscapes dataset, run:

```python
train("cityscapes", epochs=50, batch_size=32, show_interval=10)
```

To train the CGAN model on the edges2shoes dataset, run:

```python
train("edges2shoes", epochs=50, batch_size=32, show_interval=10)
```

## Results

The model's performance can be visualized during training by generating images at specified intervals. Example generated images can be shown using the `show_images` function defined in the training script.

### Cityscapes Dataset

```
[Epoch 0/50] [D loss: 0.396203, acc:  54%] [G loss: 24.742083] time: 0:00:38.267315

[Epoch 10/50] [D loss: 0.403096, acc:  57%] [G loss: 18.573973] time: 0:04:54.837506

[Epoch 20/50] [D loss: 0.209025, acc:  67%] [G loss: 16.076872] time: 0:09:11.809215

[Epoch 30/50] [D loss: 0.137265, acc:  85%] [G loss: 13.887999] time: 0:13:27.634520

[Epoch 40/50] [D loss: 0.160753, acc:  79%] [G loss: 12.809147] time: 0:17:44.067309
```

### edges2shoes Dataset

```
[Epoch 0/50] [D loss: 0.335585, acc:  42%] [G loss: 22.821291] time: 0:00:30.354340

[Epoch 10/50] [D loss: 0.203647, acc:  70%] [G loss: 13.291032] time: 0:04:49.640040

[Epoch 20/50] [D loss: 0.004425, acc: 100%] [G loss: 0.126131] time: 0:09:28.213779

[Epoch 30/50] [D loss: 0.090228, acc:  88%] [G loss: 0.176383] time: 0:13:51.854099

[Epoch 40/50] [D loss: 0.050035, acc:  98%] [G loss: 0.144893] time: 0:18:18.380364
```
