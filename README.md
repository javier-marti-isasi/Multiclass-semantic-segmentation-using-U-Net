# Multiclass-semantic-segmentation-using-U-Net
Multiclass semantic segmentation using U-Net in TensorFlow 2 / Keras. 

## Directory Structure

**All the code files and folders follow the following structure in ipynb file.**

```
├── training.tif
├── testing.tif
├── training_groundtruth.tif
├── testing_groundtruth.tif
├── patches
│   ├── images
│   └── masks
└── model.hdf5
```

## Introduction

The line of research is motivated by the need to accurately segment mitochondria from images. To solve this problem, we will use binary semantic segmentation using U-Net in TensorFlow 2 / Keras.

It is used U-Net model, which is trained on this <a href="https://www.epfl.ch/labs/cvlab/data/data-em/" target="_blank">Electron Microscopy Dataset</a>. Mitochondria is annotated in two sub-volumes. Each sub-volume consists of 165 slices of 1024x768. 

U-Net is a semantic segmentation technique originally proposed for medical imaging segmentation. U-Net was introduced in the paper, <a href="https://arxiv.org/abs/1505.04597" target="_blank">U-Net: Convolutional Networks for Biomedical Image Segmentation</a>. The model architecture is fairly simple: an encoder (for downsampling) and a decoder (for upsampling) with skip connections.

![unet](https://user-images.githubusercontent.com/73080100/184484154-958f202c-8d9e-412f-bc9d-c1ece98b1064.jpg)

The gray arrows indicate the skip connections that concatenate the encoder feature map with the decoder, which helps the backward flow of gradients for improved training.


## Instructions

Please, follow the instruction in the provided notebook.


## Results

With just 330 images of 1024x768, it achieves a Mean Intersection over union (IoU) of 0.955639 in the unseen test partition.


## Predicted segmentation examples

![descarga](https://user-images.githubusercontent.com/73080100/184480994-c8e2ecea-9c2e-46af-a38e-85a9ea0b3637.jpg)
![descarga (1)](https://user-images.githubusercontent.com/73080100/184481024-63fed445-7f8b-43bd-a7fe-ccab3a9b28d2.jpg)
![descarga (2)](https://user-images.githubusercontent.com/73080100/184481033-f9a585aa-46fc-43a5-b0b1-f969b02866f7.jpg)




