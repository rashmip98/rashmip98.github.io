---
layout: post
title:  Image Super Resolution Using GANs
tag: project
---

Image super-resolution (SR) is the process of estimating a high resolution image from its low resolution counterpart by attempting to recover the missing information when upsampling the image. In this project, high resolution images were recovered with the utilization of Generative Adversarial Networks. The experiments conducted in the project focus on improving the perceptual quality of the images obtained from the baseline model of ESRGAN. 

The fundamental stability of the GAN was improved by incorporating spectral normalisation, weight norm, avoiding sparse gradients to streamline the training process. The visual and perceptual quality of the images was improved by incorporating the following changes:
- The perceptual loss is improved by incorporating the Multi-Scale Discriminative Feature (MDF) loss function
- The baseline model of ESRGAN utilized only bicubic interpolation downsampling as its degradation method to generate low resolution images for training. In addition to this, Gaussian Blur along with bicubic downsampling was used as a more realistic degeneration technique
– The baseline model again implemented a normal bicubic interpolation method for upsampling within the Generator. Instead, PyTorch’s PixelShuffle was used which is essentially a sub-pixel convolution layer which learns an array of upscaling filters to upscale the final LR feature maps into the HR output
– The architecture of the Generator was improved by increasing the number of ”Residual In Residual Dense Blocks” in the Generator CNN
– The architecture of the Discriminator was improved by increasing the number of linear layers.

View the code -> [GitHub](https://github.com/rashmip98/Image-Super-Resolution-Using-Modified-ESRGAN)

Read the report -> [Google Drive](https://drive.google.com/file/d/1rx0-YSg8xh8GbWJXlbv239dbunERvgus/view)
