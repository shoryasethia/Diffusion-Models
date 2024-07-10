# Diffusion-Models
![Overall Logic](https://github.com/shoryasethia/Diffusion-Models/blob/main/temp/WhatsApp%20Image%202024-07-10%20at%2013.23.56_3df28bfb.jpg)

## Training and Sampling Algorithm
![Algorithms](https://github.com/shoryasethia/Diffusion-Models/blob/main/temp/WhatsApp%20Image%202024-07-10%20at%2015.03.29_b3fe2b52.jpg)

### To reach a certain time-step `t`, we don't need to interate our original image `t` times
> Main Equation

![Main Equation](https://github.com/shoryasethia/Diffusion-Models/blob/main/temp/WhatsApp%20Image%202024-07-10%20at%2000.02.54_5201edc2.jpg)

> Proof

![Proof](https://github.com/shoryasethia/Diffusion-Models/blob/main/temp/WhatsApp%20Image%202024-07-10%20at%2000.08.56_1ad660d7.jpg)

## Implementations
| Model | Description | Results/Observations | Code |
|-------|-------------|----------------------|----------|
| [.h5](https://drive.google.com/file/d/1Y1otfe0gdCFcu7x1hQBDj0cWKvqSIfjU/view?usp=drive_link) | U-Net based diffusion model using tensorflow for CIFAR10, `time step = 500`, `lr = 0.0004`, `betas range 0.0002 to 0.04`, `epochs = 70` | Images are denoised, but not like CIFAR10 | [.ipynb](https://github.com/shoryasethia/Diffusion-Models/blob/main/U-Net-Diffusion-Cifar10-2.ipynb) |
| [.h5](https://drive.google.com/file/d/1TpPXjLBEqkWUoYQrLTbLwrk-WUoJXPuz/view?usp=sharing) | U-Net based diffusion model using tensorflow for CIFAR10, `time step = 1000`, `lr = 0.0001`, `betas range 0.0001 to 0.02`, `epochs = 70` | Better results than above model | [.ipynb](https://github.com/shoryasethia/Diffusion-Models/blob/main/U-Net-Diffusion-Cifar10-1.ipynb) |
| - | U-Net based diffusion model using tensorflow fro CIFAR10, but started reverse diffusion or denoising from time steps 50, 10, 5. `time step = 500`, `lr = 0.0004`, `betas range 0.0002 to 0.04`, `epochs = 60` | <!-- Original image with responsive scaling --><img src="https://github.com/shoryasethia/Diffusion-Models/blob/main/temp/noisy-cifar10.png" style="max-width:100%; height:auto;"> | [.ipynb](https://github.com/shoryasethia/Diffusion-Models/blob/main/U-Net-Diffusion-NoisyCifar10.ipynb) |
