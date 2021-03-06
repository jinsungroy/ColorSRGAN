# Infrared image colorization based on an unbalanced DCGAN #

## 1. Requirments
* NVIDIA GTX1080 11GB
* Ubuntu 16.04 LTS
* Python Version = 3.xx
* Backend: Tensorflow 1.7
* Keras, Tensorflow

## 2. Model
### 2.1 GAN
![GAN](./readme/model.PNG)

### 2.2 Generator
![GENERATOR](./readme/model_generator.PNG)

### 2.3 Discriminator
![DISCRIMINATOR](./readme/model_discriminator.png)

## 3. Performance
* 64x64 to 256x256 size image
* (A) : bilinear interpolation + Colorization
* (B) : bicubic interpolation + Colorization
* (C) : FSRCNN super-resolution + Colorization
* (D) : Unbalanced DCGAN

### 3.1 Inference GPU
* NVIDIA GTX1080 11GB
* Keras (backend tensorflow)

Time(msec)|(A)|(B)|(C)|(D)
:---:|:---:|:---:|:---:|:---:
Inference|5.035|7.127|4.110|5.260

### 3.2 Inference CPU
* Intel core i7-7500U(TODO)

Time(msec)|(A)|(B)|(C)|(D)
:---:|:---:|:---:|:---:|:---:
Inference| | | |150.059

## 4. Result
64x64x1 infrared image to 256x256x3 RGB image
### 4.1 NIR (Near infrared) images
![NIR](./readme/result_nir.PNG)

### 4.2 FIR (Far infrared) images
![FIR](./readme/result_fir.PNG)


