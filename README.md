# **Original Pose Re-Generation from fake pose using GAN with UNET architecture**

Our project aims to generate new pose image from an existing pose image. Several models have been developed with improvements over time to best generate this pattern. The prominent ones like GAN's and UNET's have remarkable results. In our project we first intend to use a GAN network to generate a new pose and then use this newly generated image recreate back the original pose. We compare the results of the original pose image and the recreated image to identify how accurately can we recreate the original pose from the fake pose. In our first phase of the project we train our GAN model on Youtube pose dataset based on this paper: https://arxiv.org/abs/1804.07739  We use Tensor Flow for our codes.

The generated fake poses from the first phase will then be used in our second phase where we generate back the original pose. 

## **Phase 1** : Fake pose generation using GAN and Youtube Pose Dataset

We use the following papers to better understand the GAN network architecture: 

**1. GAN**: 
```
Paper Link:
1. https://paperswithcode.com/paper/deepfacelab-a-simple-flexible-and-extensible
2. https://arxiv.org/pdf/1908.05932.pdf
Code Link:
1. https://github.com/IanSullivan/DeepFakeTorch
2. https://github.com/YuvalNirkin/fsgan
```
**2. DCGAN**:
```
Paper Link:
1. https://arxiv.org/abs/1511.06434
Code Link:
1. https://github.com/eriklindernoren/PyTorch-GAN
```
**3. WGAN**:
```
Paper Link:
1. https://www.alexirpan.com/2017/02/22/wasserstein-gan.html
2. https://arxiv.org/abs/1701.07875
3. https://arxiv.org/abs/1704.00028
Code Link:
1. https://github.com/eriklindernoren/PyTorch-GAN
2. https://github.com/eriklindernoren/PyTorch-GAN
```

**4. Cycle GAN**:
```
Paper Link:
1. https://arxiv.org/abs/1703.10593
Code Link:
1. https://github.com/junyanz/pytorch-CycleGAN-and-pix2pix
```

We have included only 3 image folders from the Youtube image dataset in our repository due to size constraint, and the evaluation results in the report are based on these images. You may download the whole dataset using the link here: https://www.robots.ox.ac.uk/~vgg/data/pose/ 

We use the UNET architecture in our Generator model using the following four modules:

1. Source Image Segmentation
2. Spatial Transformation
3. Foreground Synthesis
4. Background Synthesis

