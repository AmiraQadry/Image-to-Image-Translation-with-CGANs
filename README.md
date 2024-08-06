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

### Example Output

During training, the model will output the losses and accuracy of both the generator and discriminator. For example:

```
[Epoch 0/50] [D loss: 0.435820, acc:  45%] [G loss: 1.076018] time: 0:00:28.481640

[Epoch 10/50] [D loss: 0.292950, acc:  31%] [G loss: 0.299010] time: 0:04:44.492710

[Epoch 20/50] [D loss: 0.266746, acc:  52%] [G loss: 0.238130] time: 0:09:04.553434

[Epoch 30/50] [D loss: 0.165246, acc:  79%] [G loss: 0.147497] time: 0:13:22.647565

[Epoch 40/50] [D loss: 0.076854, acc:  93%] [G loss: 0.122627] time: 0:17:42.062404
```

### Training on Cityscapes Dataset

```python
train("cityscapes", epochs=50, batch_size=32, show_interval=10)
```

### Training on edges2shoes Dataset

```python
train("edges2shoes", epochs=50, batch_size=32, show_interval=10)
```

## Results

The model's performance can be visualized during training by generating images at specified intervals. Example generated images can be shown using the `show_images` function defined in the training script.

### Cityscapes Dataset

```
[Epoch 0/50] [D loss: 0.435820, acc:  45%] [G loss: 1.076018] time: 0:00:28.481640

[Epoch 10/50] [D loss: 0.292950, acc:  31%] [G loss: 0.299010] time: 0:04:44.492710

[Epoch 20/50] [D loss: 0.266746, acc:  52%] [G loss: 0.238130] time: 0:09:04.553434

[Epoch 30/50] [D loss: 0.165246, acc:  79%] [G loss: 0.147497] time: 0:13:22.647565

[Epoch 40/50] [D loss: 0.076854, acc:  93%] [G loss: 0.122627] time: 0:17:42.062404
```

### edges2shoes Dataset

```
[Epoch 0/50] [D loss: 0.102226, acc:  88%] [G loss: 12.834969] time: 0:00:42.181149

[Epoch 10/50] [D loss: 0.010180, acc:  99%] [G loss: 0.179482] time: 0:05:04.768773

[Epoch 20/50] [D loss: 0.004425, acc: 100%] [G loss: 0.126131] time: 0:09:28.213779

[Epoch 30/50] [D loss: 0.090228, acc:  88%] [G loss: 0.176383] time: 0:13:51.854099

[Epoch 40/50] [D loss: 0.050035, acc:  98%] [G loss: 0.144893] time: 0:18:18.380364
```
