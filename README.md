# TGS-SaltNet
Kaggle | 21st place solution for TGS Salt Identification Challenge

## General
Kaggle competition [TGS Salt Identification Challenge](https://www.kaggle.com/c/tgs-salt-identification-challenge)
 The code demonstrates usage of different important techniques using [fast.ai](http://www.fast.ai/) and [PyTorch](https://pytorch.org/).
 
1. Use ResNet model as an encoder for UNet. 
 Resnet model as backbone give better results with Unet as compared to vanilla Unet model. 

2. Add intermediate layers like [BAM](http://bmvc2018.org/contents/papers/0092.pdf),[Squeeze & Excitation](https://arxiv.org/abs/1803.02579) blocks in a ResNet34 model which can be easily replicated for other network architectures.

 “Bottleneck Attention Module” (BAM), a simple and efficient attention module that can be used in any CNNs. Given a 3D feature
map, BAM produces a 3D attention map to emphasize important elements. In BAM, we decompose the process of inferring a 3D attention map in two streams, so that the computational and parametric overhead are significantly reduced. As the channels of feature maps can be regarded as feature detectors, the two branches (spatial and channel) explicitly learn ‘what’ and ‘where’ to focus on.

Squeeze-and-Excitation Networks (SENets) introduce a building block for CNNs that improves channel interdependencies at almost no computational cost. Main idea is add parameters to each channel of a convolutional block so that the network can adaptively adjust the weighting of each feature map

3. Show how to add [Deep supervision](https://www.kaggle.com/c/tgs-salt-identification-challenge/discussion/65933) to the network, and calculate loss and combine loss at different scale. 

## Main software used

1. fastai - 0.7
2. pytorch - 0.4
3. python - 3.6

## Hardware required

The code was tested with TitanX GPU/1080ti.

## Author: Vishnu Subramanian



