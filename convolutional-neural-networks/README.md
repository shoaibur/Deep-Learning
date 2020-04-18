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
      * k = number of filters
      * F = kernel size
      * Din = depth of the input data, i.e., the output from the previous layer
      * Number of weights in a conv layer = F * F * Din
      * Number of parameters in a conv layer = F * F * Din * k + k
      * +k indicate one bias parameter for each filter.
    * Size of output from a conv layer
      * Depth is always equal to the number of filters, k
      * Spatial dimension = (Win + 2P - F) / S + 1, where, Win = (x or y) dimension of the input data to the layer, P = padding, S = stride.
  * Pooling layers
    * Max pooling
    * Average pooling
  * Fully connected layers
* Capsule network
* Data augmentation: This allows us to represent invariances of the input images, for example.
  * Scale invariance - small vs. big images
  * Rotation invariance - rotation of image by an angle, horizontal/vertial flipping etc.
  * Translation invariance - left vs. right, top vs. bottom positions of the images
