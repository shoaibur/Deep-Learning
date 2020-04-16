# Convolutional Neural Networks
Outline
* Introduction
  * MLP vs. CNN
    * MLPs convert images into vectors, so spatial information is lost, while CNNs preserve the spatial information.
    * MLPs use only fully connected layers and accept only vectors as the inputs, while CNNs use sparsely connected layers and accept matrix data as the inputs.
  * Why do CNNs works?
  * Application of CNNs
    * Computer vision - Image classification, image segmentation
* Image processing
  * Convolutional kernel
  * Edge detectors
  * Blurring
* CNN layers
  * Convolutional layers: Conv layers make the output array deeper in the depth- or z-direction. Total depth of the output is equal to the number of filters used in the convolution. Several concepts are important to understand a conv layer, e.g.,
    * Stride
    * Padding
    * Activation
    * Number of parameters in a conv layer
    <img src="https://render.githubusercontent.com/render/math?math=e^{i \pi} = -1">
    * Size of output from a conv layer
  * Pooling layers
  * Fully connected layers
* Capsule network
* Data augmentation
  * Translation
  * Rotation
  * Flipping
