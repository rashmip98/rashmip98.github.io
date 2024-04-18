---
layout: post
title:  Playground Repo of Diffusion Models
tag: project
---

Diffusion models are a recent generative modeling technique. This repository has some of the basic diffusion models in easy-to-use colab files as well as a file which plays with the various variations and applications for diffusion models.

#### DDPM 
An implementation of the [paper](https://arxiv.org/abs/2006.11239) with some slight changes for easier training.

View the code -> [GitHub](https://github.com/rashmip98/AllThingsDiffusion/tree/main/DDPM)

#### Latent Diffusion & Stable Diffusion
In [latent diffusion](https://arxiv.org/abs/2112.10752), the image is reduced to a lower-dimensionality latent with an autoencoder and the noise is added in the latent space. [Stable Diffusion](https://github.com/CompVis/stable-diffusion) is based on latent diffusion with text conditionings from the text encoder [CLIP](https://arxiv.org/abs/2103.00020v1).

#### Task Specific Playground
- Image in-painting
- Image editing
- Semantic segmentation, object detection
