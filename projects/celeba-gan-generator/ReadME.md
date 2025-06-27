# CelebA GAN (Generative Adversarial Network)

This project uses a DCGAN (Deep Convolutional GAN) architecture trained on the CelebA dataset to generate realistic-looking celebrity faces from random noise. It leverages PyTorch, a convolutional generator and discriminator, and image transformation techniques to model the distribution of human facial features.

## Overview
The model consists of two competing networks:
- **Generator**: Takes in a latent vector (random noise) and tries to generate a realistic image.
- **Discriminator**: Takes in an image and tries to determine if it's real (from the dataset) or fake (generated).

Through training, the generator learns to create increasingly realistic faces that can fool the discriminator.

## Key Concepts
- **GANs (Generative Adversarial Networks)** — a minimax game between two neural networks.
- **Latent Space Sampling** — random noise as input for image generation.
- **Image Normalization** — all images are normalized to `[-1, 1]` to match the `tanh` output of the generator.
- **DCGAN Architecture** — uses `ConvTranspose2D` in the generator and `Conv2D` in the discriminator, with BatchNorm and LeakyReLU.

## Dataset
- **Source**: [CelebA Faces](https://www.kaggle.com/datasets/jessicali9530/celeba-dataset)
- **Contents**: Over 200,000 celebrity images of size `218x178`, aligned and cropped.
- **Download Method**: The dataset is automatically pulled using `kagglehub` and used from `img_align_celeba`.

## Training Details
| Parameter       | Value         |
|----------------|---------------|
| Epochs         | 15            |
| Batch Size     | 128           |
| Image Size     | 64x64         |
| Latent Dim     | 100           |
| Optimizer      | Adam          |
| Learning Rate  | 0.0002        |
| Generator Loss | BCELoss       |
| Discriminator  | BCELoss       |
| Device         | CUDA / CPU (Used GPU memory)    |

## Architecture
### Generator
- Linear → ConvTranspose2D layers
- BatchNorm + ReLU activations
- Final `tanh` activation to output normalized image
### Discriminator
- Conv2D layers
- LeakyReLU activations
- Final sigmoid output for binary classification (real vs. fake)

## Sample Outputs
Images are generated after every epoch using a fixed noise vector (`z`). As training progresses, the images become more realistic. Example output: (6th epoch)

![image_alt](https://github.com/15ethane-codes/ML-portfolio/blob/main/Screenshot%20(2).jpg?raw=true)

## Improvements

- Increase epochs (up to 50+) for sharper detail
- Use more advanced GAN variants (StyleGAN, WGAN-GP)
- Add facial attribute conditioning (e.g., smile, gender)
- Explore spectral normalization and gradient penalties
