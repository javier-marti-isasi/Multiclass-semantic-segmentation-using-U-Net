# Multiclass semantic segmentation using U-Net
Multiclass semantic segmentation using U-Net in TensorFlow 2 / Keras. 

## Directory Structure

**All the code files and folders follow the following structure in ipynb file.**

```
├── images_256_256_256.tif
├── masks_256_256_256.tif
├── patches
│   ├── images
│   └── masks
└── model.hdf5
```

## Introduction

The line of research is motivated by the need to accurately segment 4 regions from images about XRM (tomography) scan of a sandstone cylinder of size about 2 mm diameter. To solve this problem, we will use binary semantic segmentation using U-Net in TensorFlow 2 / Keras.

It is used U-Net model, which is trained on this <a href="https://drive.google.com/file/d/1HWtBaSa-LTyAMgf2uaz1T9o1sTWDBajU/view" target="_blank">Sandstone Dataset</a>. It is used two tif files that include 256 images of 256 x 256: <a href="https://github.com/javier-marti-isasi/Multiclass-semantic-segmentation-using-U-Net/raw/main/data/images_256_256_256.tif" target="_blank">images_256_256_256.tif</a> and <a href="https://github.com/javier-marti-isasi/Multiclass-semantic-segmentation-using-U-Net/raw/main/data/masks_256_256_256.tif" target="_blank">masks_256_256_256.tif</a>.

The 4 regions of the images consist of air/void (dark regions), quartz (light grey), clay (darker grey with texture), and pyrite (bright pixels). Clay and quartz are minority classes but since quartz appears in bright, it is easier to segment. Please read the <a href="https://drive.google.com/file/d/1HWtBaSa-LTyAMgf2uaz1T9o1sTWDBajU/view?usp=sharing" target="_blank">Readme document</a> for more information.

U-Net is a semantic segmentation technique originally proposed for medical imaging segmentation. U-Net was introduced in the paper, <a href="https://arxiv.org/abs/1505.04597" target="_blank">U-Net: Convolutional Networks for Biomedical Image Segmentation</a>. The model architecture is fairly simple: an encoder (for downsampling) and a decoder (for upsampling) with skip connections.

![unet](https://user-images.githubusercontent.com/73080100/184484154-958f202c-8d9e-412f-bc9d-c1ece98b1064.jpg)

The gray arrows indicate the skip connections that concatenate the encoder feature map with the decoder, which helps the backward flow of gradients for improved training.


## Instructions

Please, follow the instruction in the provided notebook.


## Results

With just 256 images of 256x256 and 50 epochs of training, it achieves a Mean Intersection over union (IoU) of 0.88 in the unseen test partition.


## Predicted segmentation examples

![descarga](https://user-images.githubusercontent.com/73080100/184492701-b47a9265-015f-4e5c-93e0-7a13ba54d7d6.jpg)
![descarga (3)](https://user-images.githubusercontent.com/73080100/184492709-51e15d74-ae03-4956-b553-83af43492dc8.jpg)
![descarga (1)](https://user-images.githubusercontent.com/73080100/184492716-89bbb7a0-c52e-4781-b46f-e014978f0256.jpg)



